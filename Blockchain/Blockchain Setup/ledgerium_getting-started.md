# One-Click Setup

`script.sh` is a unix bash file that downloads and deploys one Ledgerium node (consists of Geth, Constellation/Tessera, and GovernanceUI Docker containers) in a single click. 

[Download script.sh](https://github.com/ledgerium/ledgeriumsetup)


# Manual Setup
We use Ledgerium Tools to generates a ready-to-run Docker file for deploying N nodes with IBFT consensus

## Prerequisities 
### NodeJS
Confirm you have NodeJS installed by typing `node -v`, output should look like:

```
v11.1.0
```

[Download NodeJS](https://nodejs.org/en/)

### Docker
Confirm you have Docker installed by typing `docker -v`, output should look like:
```
Docker version 18.09.2, build 6247962
```
[Download Docker](https://www.docker.com/get-started)


## Getting started   

1. Download the ledgeriumtools repository
```
git clone https://github.com/ledgerium/ledgeriumtools.git
```
2. Navigate into the `ledgeriumtools` directory
```
cd ledgeriumtools
```
3. Open `initialparams.json` in a text editor and make changes if required, e.g:
```
{
	"mode": "full",
	"externalIPAddress": "125.254.27.14",
	"nodeName": "msc",
	"domainName": "localhost"
}
```
* `mode:` Change mode type (full/addon)
    * If mode type is full, this application will create a ledgeriumnetwork folder outside ledgeriumtools which has static-nodes and externalised genesis files.
    * If mode type is addon, get latest ledgeriumnetwork files from github and paste those files under ledgeriumtools/output/tmp

* `externalIPAddress:` To host a node for a network that can be connected to by anyone outside your local network

* `nodeName:` Hostname of the machine where nodes will be hosted.

* `domainName:` Domain name of the external IP Address. domainName is needed for every node to which any client wants to send transactions or do “geth attach”


4. Run the initalisation file
```
node index.js
```
5. When promted, enter the number (n) of nodes you want to run
* The `mnemonics` and `password `translate to the `node keys` and `password`
* The number of nodes brought up is equal to the number of keys/menmonics provided in the file i.e. `n keys` signifies `n nodes` with the respective keys as coinbase/etherbase
* Keep in mind `mnemomics must be unique`
```
> Number of Mnemonics : 
 4
```  
6. Enter Mnemonics and Passwords as prompted, e.g:
```
> Enter Mnemonic 0 :
 node1
> Enter Password 0 :
 password1
> Enter Mnemonic 1 :
 node2
> Enter Password 1 :
 password2
> Enter Mnemonic 2 :
 node3
> Enter Password 2 :
 password3
> Enter Mnemonic 3 :
 node4
> Enter Password 3 :
 password4
```
7. A docker compose file will be generated in `./output` and ready to be launched, change to the `output` directory
```
cd output
```
8. Run docker
```
docker-compose up -d
```
To shut down the containers run
```
docker-compose down
```

## Note
* Don't use the -v option to bring down the nodes as the current blockchain data will be lost
* For subsequent runs make sure the tmp dir created in output folder is deleted

# Deconstructing the docker-compose.yml file

A genereated docker compose file will consist of 3 image containers per node. These are as follows:

1. Ledgerium Core

    Purpose: This is the actual validator node


    Ports required:

    `30303` Network listening port

    `8545` HTTP-RPC server listening port

    `9000` WS-RPC server listening port

2. Constellation or Tessera

    Purpose: Quorum Transaction Manager - implementation of peer-to-peer encrypted message exchange for transaction privacy

    Ports required:

    `10000` 
    
3. Governance App

    Purpose: Goveranance App contains smart contracts to manage admin and individual validators to come on platform

    Ports required:

    `3545` 

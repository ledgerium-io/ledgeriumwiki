# Ledgerium Tools

Generates a ready-to-run Docker file for deploying N nodes with IBFT consensus

# Prerequisities 
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


# Getting started   

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

# Blockchain Paramters

Blocks are mined in `5 seconds` intervals

Gas price is set at `1 GWEI`

## Geth Command

For each validator node in `docker-compose.yml`, you will see this geth command getting executed

```
geth --rpc --rpcaddr '0.0.0.0' --rpccorsdomain '*' --datadir '/eth'
        --rpcapi 'db,eth,net,web3,istanbul,personal,admin,debug,txpool' --ws
        --wsorigins '*' --wsapi 'db,eth,net,web3,personal,admin,debug,txpool'
        --wsaddr '0.0.0.0' --networkid 2018 --targetgaslimit 9007199254740000
        --debug --metrics --syncmode 'full' --verbosity 6
        --emitcheckpoints --mine --minerthreads 1 --syncmode full
        --rpcvhosts=localhost --identity "validator-0" --nodekeyhex
        "83a5803e698a3642d5309f119643f6a729c7c51fac00fdffac31983cb5275bb5"
        --etherbase "f232a4bf183cf17d09bea23e19ceff58ad9dbfed" --port "30303"
        --ethstats
        "validator-0:bb98a0b6442334d0cdf8a31b267892c1@172.19.240.9:3000"
        --rpcport 8545 --wsport 9000
```

The command is broken down as follows

`geth` The go-ethereum command line interface -> geth [options] command [command options] [arguments...]

`--rpc` Enable the HTTP-RPC server

`--rpcaddr '0.0.0.0'` HTTP-RPC server listening interface

`--rpccorsdomain '*'` Comma separated list of domains from which to accept cross origin requests (browser enforced)

`--datadir '/eth'` Data directory for the databases and keystore

`--rpcapi 'db,eth,net,web3,istanbul,personal,admin,debug,txpool'` API's offered over the HTTP-RPC interface

`--ws` Enable the WS-RPC server

`--wsorigins '*'` Origins from which to accept websockets requests

`--wsapi 'db,eth,net,web3,personal,admin,debug,txpool'` API's offered over the WS-RPC interface

`--wsaddr '0.0.0.0'` WS-RPC server listening interface

`--networkid 2018` Network identifier

`--targetgaslimit 9007199254740000` Target gas limit sets the artificial target gas floor for the blocks to mine

`--debug` Prepends log messages with call-site location (file and line number)

`--metrics` Enable metrics collection and reporting

`--syncmode 'full'` Blockchain sync mode ("fast", "full", or "light")

`--verbosity 6` Logging verbosity: 0=silent, 1=error, 2=warn, 3=info, 4=debug, 5=detail

`--mine` Enable mining

`--minerthreads 1`  Number of CPU threads to use for mining

`--syncmode full` Blockchain sync mode ("fast", "full", or "light")

`--rpcvhosts=localhost` Comma separated list of virtual hostnames from which to accept requests (server enforced)

`--identity "validator-0"` Custom node name

`--nodekeyhex "83a5803e698a3642d5309f119643f6a729c7c51fac00fdffac31983cb5275bb5"` P2P node key as hex (for testing)

`--etherbase "f232a4bf183cf17d09bea23e19ceff58ad9dbfed"` Public address for block mining rewards

`--port "30303"` Network listening port 

`--ethstats "validator-0:bb98a0b6442334d0cdf8a31b267892c1@172.19.240.9:3000"` Reporting URL of a ethstats service

`--rpcport 8545` HTTP-RPC server listening port

`--wsport 9000` WS-RPC server listening port
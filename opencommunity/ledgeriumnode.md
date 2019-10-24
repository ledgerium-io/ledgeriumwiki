## [Ledgerium Node](https://docs.ledgerium.io/docs/ledgerium-masternode)
This is a  guide to setting up a Ledgerium node on a fresh Linux machine The blockchain ecosystem is a combination of multiple technologies that come together.

## One-click Installer

ledgerium_setup.sh is a Unix bash file that downloads and deploys one Ledgerium node in a single click.
``` 
 //recommended steps
 mkdir ledgerium
 cd ledgerium
 git clone https://github.com/ledgerium-io/ledgeriumsetup.git
 cd ledgeriumsetup
 ./install_dependencies.sh
 ```
 Once the dependencies are done installing go ahead and run the node.
 ```
 ledgerium_setup.sh 
```
This script prompts the user for mnemonics seed for the Ledgerium node.

A __mnemonic phrase__ or __mnemonic seed__ is a set of typically either 12 or 24 words taken from [BIP 32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki) English Wordlist, which can be used to derive an infinite number of wallets. 

### Confirming Ledgerium Network is up and running correctly

We can see if the setup ran correctly by going to [Block Explorer](https://testnet.ledgerium.net:2000). The newly added validator should be showing up in the list of active validators/block producers. Initially, the validator will synch with the network and download the entire public state of the blockchain and once ready, you can see the last block will be in synch with the rest of the network.
### Docker Commands

A few Docker commands are useful for managing Ledgerium Docker container on your machine.
Once, you are inside file path `ledgerium/ledgerium tools/output`, run the below commands.

```
docker container ps -a //List all existing containers (running and not running).

-- output below ---
CONTAINER ID        IMAGE                                             COMMAND                   CREATED             STATUS              PORTS                                                                                 NAMES
47df5e135bbb        ledgeriumengineering/governance_app_ui_img:v1.0   "/bin/sh -c 'set -u\n…"   42 seconds ago      Up 31 seconds       0.0.0.0:3545->3003/tcp                                                                output_governance-ui-ubuntu-s-4vcpu-8gb-sgp1-test-01_1
af992f1b6eae        ledgeriumengineering/ledgeriumcore:blockrewards   "/bin/sh -c 'while […"    43 seconds ago      Up 41 seconds       0.0.0.0:8545->8545/tcp, 0.0.0.0:9000->9000/tcp, 0.0.0.0:30303->30303/tcp, 30303/udp   output_validator-ubuntu-s-4vcpu-8gb-sgp1-test-01_1
1083ed5ececb        ledgeriumengineering/tessera:v1.1                 "/bin/sh -c 'DATE=`d…"    45 seconds ago      Up 42 seconds       0.0.0.0:10000->10000/tcp, 0.0.0.0:10100->10100/tcp                                    output_tessera-ubuntu-s-4vcpu-8gb-sgp1-test-01_1
```
More information on this [here](https://docs.ledgerium.io/docs/ledgerium-masternode)
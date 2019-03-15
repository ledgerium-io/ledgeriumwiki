# Blockchain Parameters

Ledgerium Blockchain is configured with `5 seconds` intervals block mining time and Gas price is set at `1 GWEI`

## Geth Command

For each validator node in `docker-compose.yml`, you will see this geth command getting executed

```
Geth Commands
geth --rpc --rpcaddr '0.0.0.0' --rpccorsdomain '*' --datadir '/eth'
        --rpcapi 'db,eth,net,web3,istanbul,personal,admin,debug,txpool' 
        --ws --wsorigins '*' --wsapi 'db,eth,net,web3,personal,admin,debug,txpool'
        --wsaddr '0.0.0.0' --networkid 2018 --targetgaslimit 9007199254740000
        --debug --metrics --syncmode 'full' --verbosity 6 --mine --minerthreads 1 
        --syncmode full --rpcvhosts=localhost --identity "validator-0" --nodekeyhex
        "83a5803e698a3642d5309f119643f6a729c7c51fac00fdffac31983cb5275bb5" --ethstats
        --etherbase "f232a4bf183cf17d09bea23e19ceff58ad9dbfed" --port "30303"
        "validator-0:bb98a0b6442334d0cdf8a31b267892c1@172.19.240.9:3000"
        --rpcport 8545 --wsport 9000
```

The command is broken down as follows

**`geth`** The go-ethereum command line interface -> geth [options] command [command options] [arguments...]

**`--rpc`** -- Enable the HTTP-RPC server

**`--rpcaddr '0.0.0.0'`** -- HTTP-RPC server listening interface

**`--rpccorsdomain '*'`**  -- Comma separated list of domains from which to accept cross origin requests (browser enforced)

**`--datadir '/eth'`** -- Data directory for the databases and keystore

**`--rpcapi 'db,eth,net,web3,istanbul,personal,admin,debug,txpool'`** -- API's offered over the HTTP-RPC interface

**`--ws`**  -- Enable the WS-RPC server

**`--wsorigins '*'`**  -- Origins from which to accept websockets requests

**`--wsapi 'db,eth,net,web3,personal,admin,debug,txpool'`**  -- API's offered over the WS-RPC interface

**`--wsaddr '0.0.0.0'`**  -- WS-RPC server listening interface

**`--networkid 2018`**  -- Network identifier

**`--targetgaslimit 9007199254740000`**  -- Target gas limit sets the artificial target gas floor for the blocks to mine

**`--debug`**  -- Prepends log messages with call-site location (file and line number)

**`--metrics`** -- Enable metrics collection and reporting

**`--syncmode 'full'`**  -- Blockchain sync mode ("fast", "full", or "light")

**`--verbosity 6`**  -- Logging verbosity: 0=silent, 1=error, 2=warn, 3=info, 4=debug, 5=detail

**`--mine`**  -- Enable mining

**`--minerthreads 1`**   -- Number of CPU threads to use for mining

**`--syncmode full`**  -- Blockchain sync mode ("fast", "full", or "light")

**`--rpcvhosts=localhost`** -- Comma separated list of virtual hostnames from which to accept requests (server enforced)

**`--identity "validator-0"`**  -- Custom node name

**`--nodekeyhex "83a5803e698a3642d5309f119643f6a729c7c51fac00fdffac31983cb5275bb5"`**  -- P2P node key as hex (for testing)

**`--etherbase "f232a4bf183cf17d09bea23e19ceff58ad9dbfed"`**  -- Public address for block mining rewards

**`--port "30303"`**  -- Network listening port 

**`--ethstats "validator-0:bb98a0b6442334d0cdf8a31b267892c1@172.19.240.9:3000"`**  -- Reporting URL of a ethstats service

**`--rpcport 8545`**  -- HTTP-RPC server listening port

**`--wsport 9000`** -- WS-RPC server listening port
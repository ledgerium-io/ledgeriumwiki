# Blockchain Parameters

Ledgerium Blockchain is using **geth** as core blockchain client and configured the **geth** as per its whitepaper requirements. However, core parameters of **geth** are applicable as is for Ledgerium Blockchain as well as described below.

**$ geth help**

**NAME:**  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**geth** - the go-ethereum command line interface  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Copyright 2018-2019 The Block Ledger Authors

**USAGE:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*geth [options] command [command options] [arguments...]*
   
**VERSION:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.8.12-stable

**COMMANDS:**  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**account**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Manage accounts  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**attach**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Start an interactive JavaScript environment (connect to node)  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**bug**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Opens a window to report a bug on the geth repo  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**console**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Start an interactive JavaScript environment  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**copydb**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Create a local chain from a target chaindata folder  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**dump**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dump a specific block from storage  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**dumpconfig**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Show configuration values  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**export**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Export blockchain into file  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**export-preimages**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Export the preimage database into an RLP stream  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**import**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Import a blockchain file  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**import-preimages**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Import the preimage database from an RLP stream  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**init**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bootstrap and initialize a new genesis block  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**js**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Execute the specified JavaScript files  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**license**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Display license information  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**makecache**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Generate ethash verification cache (for testing)  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**makedag**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Generate ethash mining DAG (for testing)  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**monitor**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Monitor and visualize node metrics  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**removedb**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remove blockchain and state databases  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**version**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Print version numbers  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**wallet**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Manage Ethereum presale wallets  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**help, h**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Shows a list of commands or help for one command  

**ETHEREUM OPTIONS:**  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--config value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TOML configuration file  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--datadir "/home/.ledgerium"**  &nbsp;Data directory for the databases and keystore  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--keystore**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Directory for the keystore (default = inside the datadir)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nousb**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disables monitoring for and managing USB hardware wallets  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--networkid value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Network identifier (integer, 2018=Toorak, 2019=Flinders, 2020=Southbank, 2021=Richmond) (default: 2019)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--testnet**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Toorak network: The original test network  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--flinders**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Flinders network: the first test network with block rewards  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--syncmode "fast"**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Blockchain sync mode ("fast", "full", or "light")  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--gcmode value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Blockchain garbage collection mode ("full", "archive") (default: "full")  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--ethstats value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reporting URL of a ethstats service (nodename:secret@host:port)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--identity value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Custom node name  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--lightserv value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum percentage of time allowed for serving LES requests (0-90) (default: 0)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--lightpeers value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum number of LES client peers (default: 100)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--lightkdf**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reduce key-derivation RAM & CPU usage at some expense of KDF strength

**API AND CONSOLE OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpc**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable the HTTP-RPC server  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpcaddr value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;HTTP-RPC server listening interface (default: "localhost")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpcport value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;HTTP-RPC server listening port (default: 8545)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpcapi value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;API's offered over the HTTP-RPC interface  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--ws**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable the WS-RPC server  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--wsaddr value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WS-RPC server listening interface (default: "localhost")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--wsport value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WS-RPC server listening port (default: 8546)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--wsapi value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;API's offered over the WS-RPC interface  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--wsorigins value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Origins from which to accept websockets requests  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--ipcdisable**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disable the IPC-RPC server  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--ipcpath**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Filename for IPC socket/pipe within the datadir (explicit paths escape it)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpccorsdomain value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated list of domains from which to accept cross origin requests (browser enforced)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--rpcvhosts value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated list of virtual hostnames from which to accept requests (server enforced). Accepts '*' wildcard. (default: "localhost")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--jspath**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;LoadScriptJavaScript root path for loadScript (default: ".")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--exec value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Execute JavaScript statement  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--preload value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated list of JavaScript files to preload into the console

**ACCOUNT OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--unlock value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated list of accounts to unlock  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--password value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Password file to use for non-interactive password input

**MINER OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--mine**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable mining  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--minerthreads value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of CPU threads to use for mining (default: 8)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--etherbase value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Public address for block mining rewards (default = first account created) (default: "0")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--targetgaslimit value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Target gas limit sets the artificial target gas floor for the blocks to mine (default: 4712388)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--gasprice "18000000000"**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Minimal gas price to accept for mining a transactions  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--extradata value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Block extra data set by the miner (default = client version)

**NETWORKING OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--bootnodes value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated enode URLs for P2P discovery bootstrap (set v4+v5 instead for light servers)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--bootnodesv4 value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated enode URLs for P2P v4 discovery bootstrap (light server, full nodes)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--bootnodesv5 value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comma separated enode URLs for P2P v5 discovery bootstrap (light server, light nodes)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--port value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Network listening port (default: 30303)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--maxpeers value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum number of network peers (network disabled if set to 0) (default: 25)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--maxpendpeers value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum number of pending connection attempts (defaults used if set to 0) (default: 0)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nat value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;NAT port mapping mechanism (any|none|upnp|pmp|extip:<IP>) (default: "any")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nodiscover**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disables the peer discovery mechanism (manual peer addition)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--v5disc**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enables the experimental RLPx V5 (Topic Discovery) mechanism  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--netrestrict value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Restricts network communication to the given IP networks (CIDR masks)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nodekey value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;P2P node key file  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nodekeyhex value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;P2P node key as hex (for testing)

**TRANSACTION POOL OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.nolocals**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disables price exemptions for locally submitted transactions  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.journal value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disk journal for local transaction to survive node restarts (default: "transactions.rlp")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.rejournal value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Time interval to regenerate the local transaction journal (default: 1h0m0s)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.pricelimit value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Minimum gas price limit to enforce for acceptance into the pool (default: 1)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.pricebump value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Price bump percentage to replace an already existing transaction (default: 10)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.accountslots value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Minimum number of executable transaction slots guaranteed per account (default: 16)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.globalslots value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum number of executable transaction slots for all accounts (default: 4096)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.accountqueue value**&nbsp;&nbsp;&nbsp;Maximum number of non-executable transaction slots permitted per account (default: 64)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.globalqueue value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum number of non-executable transaction slots for all accounts (default: 1024)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--txpool.lifetime value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Maximum amount of time non-executable transaction are queued (default: 3h0m0s)

**LOGGING AND DEBUGGING OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--metrics** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable metrics collection and reporting  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--fakepow** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disables proof-of-work verification  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--nocompaction**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Disables db compaction after import  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--verbosity value** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Logging verbosity: 0=silent, 1=error, 2=warn, 3=info, 4=debug, 5=detail (default: 3)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--vmodule value** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Per-module verbosity: comma-separated list of <pattern>=<level> (e.g. eth/*=5,p2p=4)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--backtrace value** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Request a stack trace at a specific logging statement (e.g. "block.go:271")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--pprofaddr value** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;pprof HTTP server listening interface (default: "127.0.0.1")  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--debug** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Prepends log messages with call-site location (file and line number)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--pprof** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable the pprof HTTP server  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--pprofport value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The pprof HTTP server listening port (default: 6060)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--memprofilerate value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Turn on memory profiling with the given rate (default: 524288)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--blockprofilerate value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Turn on block profiling with the given rate (default: 0)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--cpuprofile value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Write CPU profile to the given file  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--trace value** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Write execution trace to the given file

**QUORUM OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--permissioned**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If enabled, the node will allow only a defined list of nodes to connect    

**IBFT OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--istanbul.requesttimeout**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Timeout for each Istanbul round in milliseconds  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--istanbul.blockperiod**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  Default minimum difference between two consecutive block's timestamps in seconds

**PERFORMANCE TUNING OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--cache value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Megabytes of memory allocated to internal caching (default: 1024)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--cache.database value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Percentage of cache memory allowance to use for database io (default: 75)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--cache.gc value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Percentage of cache memory allowance to use for trie pruning (default: 25)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--trie-cache-gens value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of trie node generations to keep in memory (default: 120)
  
**VIRTUAL MACHINE OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--vmdebug**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Record information useful for VM and contract debugging
    
**GAS PRICE ORACLE OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--gpoblocks value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of recent blocks to check for gas prices (default: 20)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--gpopercentile value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Suggested gas price is the given percentile of a set of recent transaction gas prices (default: 60)

**WHISPER (EXPERIMENTAL) OPTIONS:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--shh**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enable Whisper  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--shh.maxmessagesize value**&nbsp;&nbsp;&nbsp;Max message size accepted (default: 1048576)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--shh.pow value**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Minimum POW accepted (default: 0.2)

**MISC OPTIONS:**    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**--help, -h**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Show help
  
**COPYRIGHT:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Copyright 2018-2019 The Block Ledger Authors**

# Geth Commands used for Ledgerium Blockchain Masternode

For each validator node in `docker-compose.yml`, you will see this geth command getting executed

**Geth Commands**  
geth  
 --datadir '/eth'  
 --networkid 2019  
 --rpc  
 --rpcaddr '0.0.0.0'  
 --rpcport 8545  
 --rpccorsdomain '\*'  
 --rpcapi 'db,eth,net,web3,istanbul,personal,admin,debug,txpool'  
 --rpcvhosts=localhost  
 --ws  
 --wsorigins '*'  
 --wsapi 'db,eth,net,web3,personal,admin,debug,txpool'  
 --wsaddr '0.0.0.0'  
 --wsport 9000  
 --mine  
 --minerthreads 1  
 --syncmode 'full'  
 --targetgaslimit 9007199254740000  
 --port "30303"  
 --debug  
 --metrics  
 --txpool.nolocals  
 --txpool.accountslots 128  
 --txpool.globalslots 32768  
 --txpool.accountqueue 512  
 --txpool.globalqueue 8192  
 --identity "validator-0"  
 --nodekeyhex "83a5803e698a3642d5309f119643f6a729c7c51fac00fdffac31983cb5275bb5"  
 --etherbase "f232a4bf183cf17d09bea23e19ceff58ad9dbfed" 
 --ethstats "validator-0:bb98a0b6442334d0cdf8a31b267892c1@testnet.ledgerium.net:3000"  
 --verbosity 6  
 --emitcheckpoints
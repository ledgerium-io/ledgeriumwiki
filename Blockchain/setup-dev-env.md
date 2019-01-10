# Setting up a development environment for running Ledgerium dapps and the blockchain core

The blockchain ecosystem is a combination of multiple technologies that come together. It is overwhelming to know that so much has been achieved in a short span. The tech stacks range from  (not limited to this list) GoLang, NodeJs, Haskell, Metamask, Solidity and supporting Web3 technologies. Hence this will always remain as a living document for the team.

### Basics
GoLang - There are multiple versions of golang used in different parts of the go-ethereum/Quorum ecosystem. It is recommended to use a `gvm` go version manager to switch under a development environment.

NodeJS - Multiple applications and scripts have been written in NodeJS due to the popularity of Web3 library and its support for browser and Nodejs. Fortunately (as of today) any latest version of NodeJS will be good to start. NPM is the package manager for NodeJS. 
To begin with, 
```
Install NodeJS

Do, npm install in the repository (should have the package.json file)

Run the application Eg: node index.js
```

### Ethereum/geth

Geth is the command line interface for running a full Ethereum node implemented in Go programming language. Using Geth, you can
* take part in the Ethereum frontier live network and
* mine real ether
* transfer funds between addresses
* create contracts and send transactions
* explore block history
* and much much more

Installation:
```
https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum
```
Version : 1.7.2-stable

### Metamask
From their website *MetaMask is a bridge that allows you to visit the distributed web of tomorrow in your browser today. It allows you to run Ethereum dApps right in your browser without running a full Ethereum node. MetaMask includes a secure identity vault, providing a user interface to manage your identities on different sites and sign blockchain transactions.*

It is understood that all Ledgerium Dapps will be authorized to perform actions on the blockchain using the metamask plugin.

### Web3 JS

This is the Ethereum compatible [JavaScript API](https://github.com/ethereum/wiki/wiki/JavaScript-API) which implements the [Generic JSON RPC](https://github.com/ethereum/wiki/wiki/JSON-RPC) spec. It's available on npm as a node module, for Bower and component as embeddable scripts, and as a meteor.js package.

Installation: https://github.com/ethereum/web3.js/
```
npm install -g web3
```
Version: 1.0.0 

### Solc

Solidity compiler
Installation: https://solidity.readthedocs.io/en/latest/installing-solidity.html
```
npm install -g solc
```
Version: 0.5.2 (Ubuntu) and 0.5.1 (Mac) 

### Truffle

Truffle is a world class development environment, testing framework and asset pipeline for Ethereum, aiming to make life as an Ethereum developer easier. With Truffle, you get:
* Built-in smart contract compilation, linking, deployment and binary management.
* Automated contract testing for rapid development.
* Scriptable, extensible deployment & migrations framework.
* Network management for deploying to any number of public & private networks.
* Package management with EthPM & NPM, using the ERC190 standard.
* Interactive console for direct contract communication.
* Configurable build pipeline with support for tight integration.
* External script runner that executes scripts within a Truffle environment.

Installation: https://truffleframework.com/truffle
```
npm install -g truffle
```
Requirements:
* NodeJS v8.9.4 or later 
* Windows, Linux or Mac OS X 

### Ganache 
* A personal blockchain for Ethereum development you can use to deploy contracts, develop your applications, and run tests. It is available as both a desktop application as well as a command-line tool (formerly known as the TestRPC). Ganache is available for Windows, Mac, and Linux.
* Comes with a full fledged GUI.

Installation: https://truffleframework.com/ganache
```
npm install -g ganache-cli
```

# Tools
### Github

GitHub Inc. is a web-based hosting service for version control using Git.

Available for Windows and Mac only

Installation: 
```
https://desktop.github.com/
```

### Docker hub

Docker Hub is the world's largest library and community for container images

Download: 
```
https://www.docker.com/products/docker-desktop
```

### Remix:

Web IDE with built in static analysis, test blockchain VM.
Reference:
```
https://remix.ethereum.org/
```

## IDE

### Visual Studio Code

The Visual studio code along with the solidity plugin gives developer the IDE they need for faster development and testing.

Download:  
```
https://code.visualstudio.com/Download
```

## OS

Windows, Linux or Mac OS X 



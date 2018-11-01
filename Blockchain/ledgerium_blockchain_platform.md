# Ledgerium Blockchain Core

## Proof of Stake - PoS
## Quorum - private/public hybrid blockchain 
- Privacy & Transparency
- Performance & throughput
- Permissioned & Governance
Quorum supports both transaction-level privacy and network-wide transparency, customizable to business requirements.

## Why Quorum
- Digital trust
- Signature validation in a permissioned network 
- Ethereum like community and license model
- Quorum is designed to develop and evolve alongside Ethereum

## ZKP
A zero-knowledge proof or protocol allows a “prover” to assure a “verifier” that they have knowledge of a secret or statement without revealing the secret itself. Quorum & Ethereum

## IBFT
IBFT is plug-in and play consensus mechanism on Quorum as Byzantine Fault Tolerance BFT. BFT conceptually means, it can tolerate F fault nodes in the total no of N nodes = 3F+1. AMIs guys!!!

## Why IBFT 
IBFT provides immediate finality to the blocks. It has its internal proposal and voting mechanism before any blocks get written on the blockchain! 

## Scalability 
Originally it is 15 transactions per second in PoW. However, with the given consensus mechanism of IBFT, with 1 block per second, higher blockagas limit, we can achieve 200 transactions per second. Anything beyond, we will wait for Ethereum core platform. In mid-2019, they are going to release Beacon Chain which has sharding feature implemented for scalability

## How to become a validator on Ledgerium network

**Rewards for being validator**
Total Reward Structure for Validator

- The amount of XLGs you are staking
- The effective inflation rate in the network (see graph below), which is derived from:
    The global inflation rate, which gradually decreases to 7% when more than 2/3 of the total XLG supply is bonded. If less than 2/3 is bonded, the global inflation rate will gradually adjusts up to a maximum of 20%.
- The staked XLG supply. Rewards get calculated based on the total supply, but distributed only to those who are staking. So the fewer people stake, the higher the effective rate of rewards for those staking.
- Fee revenues, which depend on the gas price and gas used in the network.
- The commission rate of your validator(s). This is the cut of rewards that your chosen validator(s) charge for running the consensus infrastructure.
- Validator uptime (see below for details).
- Your re-staking behavior (compounding interest).
- And finally, if you are thinking about rewards in fiat terms, the XLG token price.

**Purchasing physical equipment**

You will need a server that runs the Ledgerium Blockchain software. Ledgerium Blockchain is currently recommending medium grade equipment. Expect equipment upgrades as the network gets busier.
It is highly recommended that you have a fully functional, equally powerful backup server. Having no backup server would be a red flag to Delegators considering staking their XLG to your node (explained more below).
Firewalls installed for both servers.
Hardware Security Module (HSM) — An example of an HSM is the Ledger Nano S. It is a separate piece of hardware that allows for the signing of each block. This is absolutely required, as there is a huge risk to having the private key located on the server.

**Operating Costs**

You will need to co-locate at a Data Center. It is Highly recommended to do it at one of the top Data Centers in your city, as the high security is needed, along with 100% uptime. Keep in mind most co-location agreements are a minimum of 1 year. Cheaper co-lo’s will offer month to month, but be sure to vet them extensively for their services. They might be cheap because they have power outages, which means you’ll get slashed!
You will need to set up multiple sentry nodes to connect to your validator node. This is to prevent DDOS attacks on your main node. This involves spinning up multiple full nodes on AWS or a similar service, and allowing your validator node to only connect to these nodes.
Unfortunately, there is no option to do cloud validator nodes. Ledgerium mentions that cloud SGX could become available, but right now this is not possible.

**XLG for Staking**

Your balance of XLG is what allow you to get in the top rewards node. Since Ledgerium Blockchain is PoS Blockchain. You can imagine that the XLG have a similar role to a miner node in PoW model e.g. Bitcoin. The larger your stake of XLG, the larger you get rewarded. Similar to how the more powerful your miner is, the more bitcoin you get rewarded.


**Technical Knowledge**

You will need to know how to run the Ledgerium Blockchain software. Working on the DApp, and participating in Ledgerium Blockchain testnets can prepare you for this. You’ll also need to know how to vote on all governance issues.
You need to know how to set up your server and firewall at the co-location centers. You could hire a consultant to do this, but take extreme precautions to ensure the consultant has no idea that you are staking cryptocurrency. They could maliciously try to infiltrate the node.
You need to know how to set up sentry nodes on AWS.

**Open Delegation Model - Obtaining a network of Delegators to delegate stake to your node**

A key feature of the Ledgerium Blockchain Network is the fact that other XLG owners can delegate their XLG to you. This increases your nodes overall stake.
Serious contenders for validating create websites, post blogs, and make themselves available to the community to promote their node. This helps convince more users to delegate their XLG.
You can be public or private when asking people to delegate to you. Publicly showing your identify is more trust worthy, but also puts a target on your back to be hacked.

**What it will cost**

This is a simple estimation of equipment, and should be considered a ball park price. The XLG price is based on the XLG exchange rate on March 27th, 2019. All values are in USD, and North America equipment and rental prices.

**Hardware**
```
Server with firewall= $ 10,000
HSM = $150
Backup Server with firewall= $10,000
Backup HSM=$150
Operating costs
Monthly cost for firewall and server operation = $900/month
Backup location operation = $900/month
5 Sentry nodes on AWS = $300/month
```
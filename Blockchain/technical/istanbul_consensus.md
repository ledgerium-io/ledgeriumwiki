## Istanbul Consensus

1. istanbul package provides ways of interacting with the consensus mechanism, it allows new validators to be added and existing validators to be removed
2. it allows managing the number of validatos by a voting mechanism which involves at least 2F+1 nodes
3. The details of active nodes can be found in the extra data of each block that has been committed
		using the istanbul-tools one can decode the data in the following way
		istanbul extra decode --extradata "<extradata>"
4. This extra data contains one seal and 2F+1 committed seals, these committed seals aren't included when the block hash is calculated
5. the committed seals maybe different in different blocks, but as this is not included in the blockhash, the hash can be used to verify across other nodes

## istanbul.getSnapshot()

This call shows the current state of the blockchain and gives the below structure as output
```
{
	epoch: <num>,
	hash: "",
	number: ,
	policy: 0,
	tally: {
		<addr>: {
			authorize: bool,
			votes: num
		}
	},
	validators: [addr1,addr2..],
	votes: [{
			address: addr,
			authorize: bool,
			block: num,
			validator: addr
	}]
}
```
* epoch : indicates the number of blocks after which the proposal which hasn't been resolved is cleared
* hash  : the current block hash at the given block number
* tally : the object maintaining the current state of votes of all the validators
* validators : the list of all the addresses which can act as validators
* votes : the individual votes casted by validators as an array
* authorize : true - proposal to add as a validator, false - rproposal to remove as a validator

## istanbul.propose()

	This method is used to start voting/vote for an existing proposal to add or remove a validator
	takes as argument the coinbase of the node and a bool value indicating if the validator is to be added or removed

## istanbul.getSnapshotAtHash()
	
	Used to get the current state of the voting and active validators as of a particular block hash, takes as argument a block hash

## istanbul.getCandidates(callback)
	
	Gives all the addresses with the respective votes casted by that particular node as a error first callback

## istanbul.getValidators()

	Returns the list of active validators who can commit a block

Every block header contains the following fields

```
block = 
{
	difficulty: 1,
	extraData: "",
	gasLimit: ,
	gasUsed: 0,
	logsBloom: ,
	mixHash: ,
	nonce: "0x0000000000000000",
	number: 12220,
	parentHash: "",
	receiptsRoot: "",
	sha3Uncles: "",
	stateRoot: "",
	timestamp: ,
	transactionsRoot: ""
}
```

The extra data doesn’t include the committed seals as these can vary from block to block, so the only extra data is the rlpHash of the validators and seal.
When a block is sealed the block seal is computed as ECDSA(rlpHash(Block_Header), private_key)

## Istanbul Working

1. For a new block to be committed the validators pick a new node as proposer which will be responsible to create a new block.
2. This is broadcasted to all the validaotrs along with the pre-prepare message, making all the node's change their state to pre-prepared
3. These validators now publish a prepare message
4. Upon receiving 2F+1 pre-prepare messages from the validaotrs the proposer nodes prepares for the commit of the block 
5. The new block will comprise of all the transactions submitted to that particular node, from all the transactions the block headers will be calculated 
6. **The RLP hash of all the block header will give the resultant block hash, when published this block hash will be signed using the node's private key**
7. **This signature signifies the seal of the block, which signifies that the block hash been sealed into the blockchain by a particular proposer.**
8. And once this block has been pushed a commit message is sent along with the block details
9. Each validator along with the proposer waits for 2F+1 commit messages from other blocks
10. **Each node appends it's own signautre to the extra data of this block, this is the committed seal field in the extra data**
11. Once each block has 2F+1 committed seals all the validators publish a new-round message
12. The same process repeats once a new validator is chosen as a new block proposer 
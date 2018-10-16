# Adding a peer node to an existing quorum network

* TLS is default 'strict' in constellation, need to turn it off `--tls="off"` while running constellation.

* Docker compose file for the new node must use the original genesis.json from the parent network.

* Start from `istanbul setup --num 1 --docker-compose --save`

* Constellation `--othernodes` must be the list from parent network

* `istanbul.propose` the new node from each node (n/2 + 1)

* Once the node is up, ethstats must show the new validator

* [docker-compose.yml]()


### TODO
- [ ] Turn back on the default tls settings
- [ ] Check if there is a certificate error when coming from a non-https
- [ ] Can the constellation node `--url=` be a https URL?
- [ ] Build a tool that will generate the docker-compose on the fly
    - [x] For local docker (parent and new node)
    - [ ] For an external network with public IP Addresses (parent and new node on public addresses)
- [ ] Can we leverage/modify istanbul-tools here?
- [ ] Need to generate the extradata

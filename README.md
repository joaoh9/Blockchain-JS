# Blockchain with Javascript

### Libraries used in this application

- Node.js for running JavaScript code
- Express for API setup
- Sha256 for hash calculation

### Usage

- clone repository
- npm install
- run:

```console
nodemon --watch dev -e js src/networkNode.js 3001 http://localhost:3001"
console
nodemon --watch dev -e js src/networkNode.js 3002 http://localhost:3002"
console
nodemon --watch dev -e js src/networkNode.js 3003 http://localhost:3003"
```

for each node of the Blockchain, for as many nodes as you want, just keep increasing the 3003 port number.
Each of the nodes is now a port and it supports the following API operations:

## Get Routes

- /blockchain - get the intire Blockchain
- /mine - mine a block
- /consensus - update the blockchain with the new longest chain having mined the last block
- /block/:blockHash - get a block by blockHash
- /transaction/:transactionId - get a transaction by transactionId
- /address/:address - get address by address
- /block-explorer - renders html file `index.html` for block exploring

## Post Routes

- /transaction - create a new transaction. body: new Transaction object
- /transaction/broadcast - create and broadcast transaction
- /receive-new-block - receive new block and check its hash
- /register-and-broadcast-node - register a node and broadcast it the network
- /register-nodes-buld - register multiple nodes at once

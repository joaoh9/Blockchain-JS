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
nodemon --watch dev -e js src/networkNode.js 300X http://localhost:300X"
```

for each node of the Blockchain, where X is a number from 0 to 9

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

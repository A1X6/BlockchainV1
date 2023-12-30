
# Blockchain Implementation with Flask
#### Video Demo: https://youtu.be/bMg11ldqRvA
#### Description:

# Blockchain Implementation with Flask

## Overview

This project demonstrates a basic implementation of a blockchain using Python and Flask, a web framework. The blockchain, a decentralized and distributed ledger, records transactions across a network of computers. This implementation includes functionalities for mining new blocks, adding transactions, and synchronizing the blockchain across a network of nodes.

## Table of Contents

1. [Blockchain Overview](#blockchain-overview)
2. [Mining the Blockchain](#mining-the-blockchain)
3. [Decentralizing the Blockchain](#decentralizing-the-blockchain)
4. [Endpoints](#endpoints)
5. [Running the Application](#running-the-application)
6. [Dependencies](#dependencies)
7. [Usage Examples](#usage-examples)
8. [Conclusion](#conclusion)

## Blockchain Overview

The blockchain begins with a genesis block and expands as new blocks are mined. Each block comprises a list of transactions, a proof of work, a timestamp, and the hash of the previous block. Proof of work is employed to secure the blockchain by requiring computational effort to add a new block, thus preventing tampering.

## Mining the Blockchain

### 1. Mine Block
- **Endpoint:** `GET /mine_block`
- **Description:** Mines a new block, adds a sample transaction, and returns the details of the mined block.
- **Implementation:** Retrieves the previous block, calculates the proof of work, adds a sample transaction, and creates a new block.

### 2. Get Chain
- **Endpoint:** `GET /get_chain`
- **Description:** Retrieves the full blockchain.
- **Implementation:** Returns the current state of the blockchain, including all mined blocks.

### 3. Is Valid
- **Endpoint:** `GET /is_valid`
- **Description:** Checks if the blockchain is valid.
- **Implementation:** Iterates through the blockchain to validate the integrity of each block.

### 4. Add Transaction
- **Endpoint:** `POST /add_transaction`
- **Description:** Adds a new transaction to the blockchain.
- **Implementation:** Parses incoming JSON for sender, receiver, and amount, adds the transaction to the transaction pool.

## Decentralizing the Blockchain

### 1. Connect Node
- **Endpoint:** `POST /connect_node`
- **Description:** Allows nodes to connect to the network.
- **Implementation:** Accepts a list of nodes in JSON format and adds them to the set of nodes.

### 2. Replace Chain
- **Endpoint:** `GET /replace_chain`
- **Description:** Replaces the local chain with the longest valid chain in the network.
- **Implementation:** Compares the length and validity of the local chain with those of the neighboring nodes, replacing it if a longer valid chain is found.

## Endpoints

- **/mine_block:** Mine a new block and add it to the blockchain.
- **/get_chain:** Get the full blockchain.
- **/is_valid:** Check if the blockchain is valid.
- **/add_transaction:** Add a new transaction to the blockchain.
- **/connect_node:** Connect nodes to the network.
- **/replace_chain:** Replace the local chain with the longest valid chain in the network.

## Usage Examples

### Mining a Block:

Visit [http://0.0.0.0:5001/mine_block](http://0.0.0.0:5001/mine_block) to mine a new block.

### Get the Blockchain:

Visit [http://0.0.0.0:5001/get_chain](http://0.0.0.0:5001/get_chain) to retrieve the full blockchain.

### Check Blockchain Validity:

Visit [http://0.0.0.0:5001/is_valid](http://0.0.0.0:5001/is_valid) to check if the blockchain is valid.

### Add a Transaction:

Use POST request to [http://0.0.0.0:5001/add_transaction](http://0.0.0.0:5001/add_transaction) with JSON data for sender, receiver, and amount.

### Connect Nodes:

Use POST request to [http://0.0.0.0:5001/connect_node](http://0.0.0.0:5001/connect_node) with a list of nodes to connect to the network.

### Replace Chain:

Visit [http://0.0.0.0:5001/replace_chain](http://0.0.0.0:5001/replace_chain) to replace the local chain with the longest valid chain in the network.

## Conclusion

This simple blockchain implementation with Flask provides a foundation for understanding the fundamentals of blockchain technology. It includes features for mining blocks, adding transactions, and decentralizing the network. Feel free to explore the code, interact with the endpoints, and gain insights into how a basic blockchain system operates.


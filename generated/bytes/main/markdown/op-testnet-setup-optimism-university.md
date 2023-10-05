## OP Testnet Setup


## Introduction

Running OP Testnet from source allows users to set up and initialize their own test network for Optimism's Ethereum Layer 2 solution. Since OP Sepolia is a non-migrated network, it requires initialization via a genesis file.

    


---
## Initialization

To initialize the data directory, you'll need to download the genesis JSON and run the following command: `curl -o <path to genesis JSON> -sL <URL to genesis JSON>`.

    


---
## Shared Secret Creation

To create a shared secret between `op-geth` and `op-node`, navigate to your `op-geth` directory and run the command `openssl rand -hex 32 > jwt.txt`. This shared secret will ensure secure communication between the different components of the OP Testnet.

    


---
## Script Setup

In the root of your working directory, create a new directory called `scripts`. Inside this directory, insert a snippet of code into the run-`op-geth.sh` file and modify the path to the `op-geth` directory.

    


---
## Synchronization

Before you can use the OP Testnet, you need to synchronize the data directory. The datadir provided by Optimism is not updated continuously, so synchronization is necessary. While the synchronization process is ongoing, you will receive log messages from `op-node`.

    


---
## Synchronization Estimation

To estimate how long the synchronization will take, you can use the Foundry script provided. Simply navigate to your scripts directory, create a new file called `run-estimate.sh`, and run the command `./run-estimate.sh` to get an estimate of the synchronization time.

    


---
## Evaluation





##### What is the purpose of initializing the data directory in OP Testnet setup?  
     
- [x]  To set up and initialize the test network for Optimism's Ethereum Layer 2 solution
- [ ]  To synchronize the data directory with the Optimism network
- [ ]  To estimate the synchronization time for the OP Testnet
- [ ]  To create a shared secret between `op-geth` and `op-node`

    


---
## Evaluation





##### What is the purpose of creating a shared secret in OP Testnet setup?  
     
- [ ]  To set up and initialize the test network for Optimism's Ethereum Layer 2 solution
- [ ]  To synchronize the data directory with the Optimism network
- [ ]  To estimate the synchronization time for the OP Testnet
- [x]  To ensure secure communication between the different components of the OP Testnet

    
   
## Science of Optimism:How It Works


## Introduction

Optimism functions by utilizing the security of another blockchain, referred to as the parent chain. Instead of having its own consensus mechanism, Optimistic Rollups depend on the consensus mechanism of the parent chain, such as Proof of Work (PoW) or Proof of Stake (PoS).

    


---
## Block Storage

In the case of Optimism, L2 blocks are stored on the Ethereum blockchain using a non-contract address. Once these blocks are submitted as transaction calldata on Ethereum, they cannot be altered or censored. This ensures the availability and integrity guarantees of Ethereum are inherited by the Optimism network.

    


---
## Block Production

Optimism block production is primarily managed by a single party called the 'sequencer.' In Bedrock, the sequencer has a private mempool, similar to Ethereum's L1, to prevent opportunities for MEV (Miner Extractable Value). Blocks are produced every two seconds on OP Mainnet, regardless of whether they are empty or filled with transactions.

    


---
## Transaction Inclusion

Transactions submitted on the Ethereum L1, known as deposits, are included in the appropriate L2 block. Each L2 block is identified by its epoch (the corresponding L1 block) and a serial number within that epoch. The first block of the epoch includes all the deposits that occurred in the corresponding L1 block.

    


---
## Execution Engine

The execution engine, implemented as the op-geth component, receives blocks using two mechanisms. It can update itself using a peer-to-peer network with other execution engines, similar to how L1 execution clients synchronize the state across the network or the rollup node, implemented as the op-node component, derives the L2 blocks from the L1 blockchain. 

    


---
## Evaluation





##### How does Optimism utilize the security of another blockchain?  
     
- [x]  By utilizing the security of another blockchain, referred to as the parent chain
- [ ]  By having its own consensus mechanism
- [ ]  By depending on the consensus mechanism of the child chain
- [ ]  By using a private mempool for block production

    


---
## Evaluation





##### How are L2 blocks stored on the Ethereum blockchain in Optimism?  
     
- [ ]  By submitting them as transaction calldata on Ethereum
- [ ]  By storing them in a contract address on Ethereum
- [x]  By storing them on the Ethereum blockchain using a non-contract address
- [ ]  By storing them on a separate blockchain

    
   
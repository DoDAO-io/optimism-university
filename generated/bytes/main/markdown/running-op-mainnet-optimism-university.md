## Running OP Mainnet


## Getting the Data Directory

To run OP Mainnet from source, start by downloading the data directory for `op-geth`. The Bedrock version is recommended, which is 303 GB in size. Use a tool like aria2 to reduce the chance of data corruption.

    


---
## Setting up `l2geth`

After downloading, navigate to your op-geth directory and create a new directory called 'datadir'. If you're using the optional `l2geth` archive node, download the data directory snapshot using aria2. Navigate to your `l2geth` directory and create a new directory called 'datadir'.

    


---
## Creating a Shared Secret

To establish a connection between `op-geth` and `op-node`, create a shared secret. Navigate to your `op-geth` directory and run the command 'openssl rand -hex 32 > jwt.txt' to generate the shared secret.

    


---
## Starting the Components

In the root of your working directory, create a new directory called `scripts`. Inside this directory, create two new files: 'run-l2geth.sh' and 'run-op-geth.sh'. Insert the necessary code into these files, modifying the paths to the `l2geth` and `op-geth` directories. These scripts will be used to start the `l2geth` and `op-geth` components.

    


---
## Configuring Archive Nodes

If you're using archive nodes, point `op-geth` at `l2geth` using the `--rollup.historicalrpc` flag. This enables the historical RPC endpoint, which fetches historical execution data from Legacy Geth. Modify the code snippet in the `run-op-geth.sh` file to include the L1 RPC URL and set the L1KIND to the network provider you're using.

    


---
## Synchronizing the Data Directory

Before using the node, synchronize the data directory. The datadir provided by Optimism isn't updated continuously, so synchronization is necessary. During the synchronization process, `op-node` will display log messages indicating its progress. This is normal and means that `op-node` is looking for a location in the batch queue.

    


---
## Estimating Sync Time

To estimate the synchronization time, use the Foundry script. Navigate to your `scripts` directory and create a new file called `run-estimate.sh`. Run the script to get an estimated sync time based on the number of blocks synchronized in a minute.

    


---
## Evaluation





##### What is the recommended size of the data directory for running OP Mainnet from source?  
     
- [x]  303 GB
- [ ]  256 GB
- [ ]  512 GB
- [ ]  128 GB

    


---
## Evaluation





##### What command should be run to generate the shared secret for establishing a connection between `op-geth` and `op-node`?  
     
- [ ]  openssl rand -hex 16 > jwt.txt
- [ ]  openssl rand -hex 64 > jwt.txt
- [x]  openssl rand -hex 32 > jwt.txt
- [ ]  openssl rand -hex 8 > jwt.txt

    
   
## OP Node Deployment


## Preparation

Deploying an OP node involves setting up and configuring different components, including the Rollup Node, Execution Engine, and Legacy Geth. Before deploying an `op-node`, ensure that your system meets the minimum requirements. These requirements may vary depending on the network you are participating in. Make sure you have sufficient disk space available to store the network's data.

    


---
## Execution Engine Initialization

The Execution Engine, also known as `op-geth`, requires initialization. For networks like OP Sepolia, you'll need to download the genesis file and initialize the data directory via geth init. For networks migrated from a legacy network, you'll download a preconfigured data directory and extract it. `op-geth` accepts standard go-ethereum flags and additional flags specific to Optimism.

    


---
## Configuration

You'll need to configure the authenticated RPC endpoint, JWT secret file, and other parameters based on your requirements. Consult the documentation for the network you are participating in to get the correct configuration details. The Rollup Node requires a configuration file called `rollup.json` or 'rollup config' to specify network-specific genesis parameters.

    


---
## Network Setup

For official networks like OP Goerli, OP Sepolia, and OP Mainnet, the genesis config is hardcoded in the `op-node` software and can be specified via a `--network flag`. You can also manually specify a path to a rollup config using the `--rollup.config flag`. The `op-node` participates in a peer-to-peer network to distribute blocks that have not been submitted to L1 yet.

    


---
## Peer Connection

It automatically discovers and connects to peers using a set of bootnodes. You can also manually specify peers to connect to via the `--p2p.static` flag. Make sure to run the node with a static IP address accessible from the public Internet and open the required port on your firewall.

    


---
## Legacy Geth

For upgraded networks like OP Mainnet or OP Goerli, you'll need to run Legacy Geth to serve historical execution traces. Legacy Geth is our old `l2geth` binary running against a preconfigured data directory. Configure Legacy Geth by following the instructions for using a preconfigured data directory and specify the `USING_OVM=true` environment variable.

    


---
## Troubleshooting

If you encounter any issues during the deployment process, here are some common problems and their solutions:. Make sure `op-geth` authenticated RPC is enabled and the URL is correct. Ensure that the `op-node` has write access to the P2P discovery and peerstore directories. Verify that the `op-node` 's L1 URL, rollup config/ `--network` parameter, and L2 URL are correct for the given network.

    


---
## Evaluation





##### What is the purpose of deploying an OP node?  
     
- [ ]  To buy assets for fun
- [x]  To participate in a peer-to-peer network and distribute blocks
- [ ]  To increase the value of owned assets over time
- [ ]  To decrease the value of owned assets over time

    


---
## Evaluation





##### What is the purpose of Legacy Geth in OP node deployment?  
     
- [ ]  To configure the authenticated RPC endpoint
- [ ]  To manually specify peers to connect to
- [x]  To serve historical execution traces in upgraded networks
- [ ]  To troubleshoot any issues during the deployment process

    
   
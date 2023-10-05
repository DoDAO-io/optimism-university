## Oracles


## Oracles in Blockchain

Oracles are important tools in blockchain technology. They allow code running on a blockchain to access a wide range of information, bringing offchain data onchain. Oracles are crucial in stablecoins using ETH as collateral, as they determine how many stablecoins are given for a given amount of ETH by providing the ETH/USD exchange rate.

    


---
## Types of Oracles

There are two types of oracles: push and pull. Push oracles continuously update and provide up-to-date information onchain. Pull oracles, on the other hand, are only updated when a contract requests information. This requires two transactions, with the first transaction requesting information and the second providing the answer.

    


---
## Gas and Chainlink Oracles

Gas Oracle is a push oracle that provides information about gas prices and related parameters. The L1 gas price is updated onchain every 5 minutes and can change by up to 20% each time. Chainlink, another popular oracle provider, offers a variety of price feeds that provide up-to-date information accessible onchain.

    


---
## Tellor Oracle

Tellor is a customizable oracle that allows users to put any verifiable data onchain. It rewards entities providing accurate information and penalizes those providing incorrect information. It usually operates as a pull oracle but can act as a push oracle under certain circumstances.

    


---
## UMA Oracle

UMA is a generic oracle that allows any contract to request information. Staked entities provide answers, and external entities can dispute the proposed answer by providing their own answer and staking their tokens. UMA operates as a pull oracle, meaning information is not obtained until it is requested by a contract.

    


---
## Uniswap Pools

Uniswap pools, although not technically oracles, provide quotes that give the relative costs of assets. These quotes can be used to determine asset prices. However, relying solely on onchain asset prices, especially in low liquidity pools, can lead to price manipulation.

    


---
## Evaluation





##### What is the role of oracles in the blockchain ecosystem?  
     
- [x]  Providing offchain data onchain
- [ ]  Updating gas prices and related parameters
- [ ]  Determining asset prices in Uniswap pools
- [ ]  Rewarding entities providing accurate information

    


---
## Evaluation





##### What are the two types of oracles?  
     
- [ ]  Gas and Chainlink oracles
- [x]  Push and pull oracles
- [ ]  Tellor and UMA oracles
- [ ]  Stablecoins and Uniswap oracles

    
   
## **Major Blockchain Networks and Their Consensus Algorithms (2025)**

Below is a table of the **major blockchain networks** (public, private, and consortium) available as of today, indicating the **current consensus algorithm** each uses. In cases where a network has switched algorithms, the current one is shown.

| **Blockchain**                   | **Type**                      | **Current Consensus Algorithm**                                                                                                                                                                                                                                                                                           |
|----------------------------------|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bitcoin**                      | Public (Permissionless)       | **Proof of Work (PoW)** – A decentralized consensus mechanism where miners compete to solve cryptographic puzzles and validate blocks. (It has not changed since its inception.)                                                                                                                                        |
| **Ethereum**                     | Public (Permissionless)       | **Proof of Stake (PoS)** – Since *The Merge* in September 2022, Ethereum has used PoS (previously, it used PoW). Validators lock up ETH (staking) instead of mining to confirm blocks.                                                                                                                             |
| **Solana**                       | Public                        | **Delegated Proof of Stake + Proof of History (DPoS + PoH)** – Combines PoS with delegated validators and a unique cryptographic clock (Proof of History) to order events, achieving high performance at ~65k TPS.                                                                                                      |
| **Ripple (XRP Ledger)**          | Public (Permissioned)         | **XRP Ledger Consensus Protocol** – A federated Byzantine agreement (FBA) algorithm where a network of trusted validators reaches consensus via an 80% supermajority vote, without mining. (It does not use PoW/PoS, but its own protocol.)                                                                |
| **Cardano**                      | Public                        | **Proof of Stake (PoS) – Ouroboros** – A PoS algorithm developed by Cardano (since 2017) called Ouroboros. Validators (stake pools) produce blocks based on the amount of ADA delegated by users. *(It has never used PoW.)*                                                                         |
| **Polkadot**                     | Public                        | **Nominated Proof of Stake (NPoS)** – A PoS variant where nominators support validators with DOT. It uses a hybrid consensus: block production via BABE and a finality gadget, GRANDPA (BFT), for speed and security.                                                                                             |
| **Avalanche**                    | Public                        | **Proof of Stake (PoS)** – Uses the Avalanche consensus, a family of probabilistic algorithms (Snowball, Avalanche) based on repeated random sampling (aBFT). Its contract chain uses the Snowman protocol (a linear version of Avalanche).                                                                   |
| **Algorand**                     | Public                        | **Pure Proof of Stake (PPoS)** – A unique PoS algorithm in which validators are randomly selected via VRF functions to propose and vote on blocks. It is highly efficient and avoids forks (providing instant finality).                                                                                              |
| **Stellar**                      | Public                        | **Stellar Consensus Protocol (SCP)** – An algorithm based on a Federated Byzantine Agreement. Each node trusts a set of other nodes (quorum slice), and through federated voting, the network reaches consensus when a supermajority quorum is formed.                                                             |
| **Cosmos (Cosmos Hub)**          | Public                        | **Tendermint BFT (PoS)** – Cosmos Hub uses Tendermint Core, a classic BFT algorithm adapted to PoS. Validators stake ATOM and take turns proposing blocks, which are validated using Byzantine Fault Tolerant consensus (immediate finality with 2/3+ votes).                                                    |
| **Tezos**                        | Public                        | **Liquid Proof of Stake (LPoS)** – A delegated PoS variant used by Tezos. Validators (“bakers”) are elected proportionally to their stake (self + delegated) to create blocks, and users can freely delegate XTZ (“liquid”) without relinquishing custody.                                                   |
| **Fantom**                       | Public                        | **Lachesis (aBFT PoS)** – An asynchronous BFT algorithm without a leader. Lachesis uses a Directed Acyclic Graph (DAG) to record events and reach consensus independently on each node, achieving high speed and near-instant finality. It is a customized PoS variant for validating transactions.             |
| **NEAR Protocol**                | Public                        | **Proof of Stake (PoS) with Sharding** – NEAR employs PoS (with validators staking NEAR) alongside a sharded architecture called Nightshade. It uses a block production algorithm known as Doomslug to achieve rapid finality in each round. (Each shard is validated in parallel and combined into one chain.) |
| **Binance Smart Chain (BNB)**    | Public                        | **Staked Authority (PoSA)** – A hybrid mechanism combining PoA and DPoS used by BSC. Only **21 validators** (elected based on BNB stake) take turns producing blocks every 3 seconds, allowing high TPS and low fees. *(Also referred to as “Proof of Staked Authority” by Binance.)*                    |
| **Hedera Hashgraph**             | Public (Council-Governed)     | **Hashgraph (aBFT)** – An algorithm based on gossip-about-gossip and virtual voting. Nodes randomly propagate events and use the gossip history to virtually compute the majority vote, achieving very fast asynchronous Byzantine consensus without the need for mining.                                        |
| **TRON**                         | Public                        | **Delegated Proof of Stake (DPoS)** – 27 Super Representatives (validators chosen by the community) produce blocks in 3-second turns and rotate every 6 hours. TRX holders vote to elect these representatives, maintaining network security.                                                               |
| **EOS**                          | Public                        | **Delegated Proof of Stake (DPoS)** – Uses DPoS with **21 active Block Producers**. EOS holders vote to elect these producers, who take turns adding blocks in fixed rounds, offering quick finality and high capacity (albeit with some centralization).                                                   |
| **Hyperledger Fabric**           | Private / Consortium          | **Ordering Service Consensus (Raft/CFT)** – A permissioned platform without mining. Transactions are ordered by orderer nodes. By default, it uses Raft (a Crash Fault Tolerant consensus) to order blocks in a distributed manner. *(Fabric also supports BFT algorithms in recent versions, such as BFT-SMaRt.)* |

*Note:* *"Permissioned" indicates that validator nodes must be authorized (typical in private or consortium networks), unlike public permissionless networks where anyone can participate as a validator or miner.*

---

## **Other Types of Consensus Algorithms in Blockchain**

## Proof of Authority (PoA)
It is a consensus algorithm based on the reputation of authorized validators, who must reveal their identity and assume responsibilities, ensuring transparency and security.  
- **Advantages:** High efficiency, low operational costs, eco-friendly.  
- **Disadvantages:** Privacy risks, centralization, susceptibility to censorship.  
- **Ideal for:** Private networks that require control and scalability.

## Proof of History (PoH)
Designed by Solana, it uses a reliable timestamp record that allows rapid transaction validation through a looping hash function.  
- **Advantages:** Speed (50,000+ transactions per second), scalability, decentralization, and efficiency.  
- **Disadvantages:** Technical complexity and limited adoption outside Solana.  
- **Ideal for:** Networks seeking massive scalability and instant confirmation.

## Hybrid PoW/PoS
Combines Proof of Work (PoW) and Proof of Stake (PoS) to enhance security, sustainability, and flexibility.  
- **Advantages:** Resistant to attacks (such as the 51% attack), lower energy consumption, and adaptable.  
- **Disadvantages:** Complex implementation.  
- **Examples:** Decred and Hcash.

## Delayed Proof of Work (dPoW)
Allows a smaller blockchain to leverage the security of a larger one (like Bitcoin). It combines PoW and PoS to create a backup layer on the main blockchain.  
- **Advantages:** Enhanced security by backing transactions on two networks.  
- **Disadvantages:** Dependency on the main blockchain.

## Other Algorithms
- **XRP Ledger Consensus Protocol:** Developed by Ripple, focused on efficiency and speed for payments.  
- **Proof of Burn (PoB):** Uses the “burning” of coins as a mechanism to validate transactions.

## **Consensus Algorithms in Blockchain: Proof of Stake (PoS)**

Another popular consensus algorithm in the blockchain ecosystem is **Proof of Stake** (PoS). It is an alternative to **Proof of Work** (PoW) that, instead of requiring mining nodes, uses **validators** to verify transactions and validate new blocks.

In this mechanism, nodes are required to hold a certain amount of cryptocurrency and **lock it up in the network** as a form of collateral. This process is known as **staking**. Nodes that meet these conditions can become **validators** of the blockchain and, based on the **amount of cryptocurrency** they own and have staked, may be **randomly selected** to participate in the consensus process, validate transactions, and create new blocks.

For their participation, validators also receive **rewards in the form of cryptocurrency**, in addition to **transaction fees**. However, if they act dishonestly, they may also be **penalized** through a mechanism called **slashing**, which is designed to discourage harmful behavior on the network.

---

## **Main Advantages of PoS:**

- Compared to PoW, **Proof of Stake is more energy-efficient**, as it doesn't require massive processing power.
- **It ensures network security and stability** by incentivizing honest behavior, since validators risk losing their staked funds.
- **It is more scalable than PoW**, since it doesn't require solving complex mathematical problems.

---

However, this consensus algorithm is **more prone to centralization**, as entities with a larger amount of staked cryptocurrency are more likely to be selected as validators.

**Ethereum**, which initially used the **Proof of Work** consensus algorithm, transitioned to **Proof of Stake** on **September 15, 2022**.

Other blockchain networks that implement PoS include **Cardano** and **The Open Network (TON)**.

---

## **The Ethereum Merge**

The term **Merge** refers to the process that allowed the Ethereum network to transition from a **Proof-of-Work** system (using miners and the ETHHash algorithm) to a **Proof-of-Stake** system. This was achieved by merging the **mainnet** with the **Beacon Chain**, completing Ethereum's transformation into a **PoS** chain.

As a result, the Ethereum development team made the blockchain significantly **more energy-efficient**. The shift to PoS, based on validator nodes that stake ETH, reduced Ethereum's **energy consumption by 99.95%**, as the network no longer relies on mining equipment to operate.

Moreover, the Merge laid the foundation for **scalability** through **sharding**, a blockchain fragmentation technology that could allow Ethereum to reach more than **1,000 transactions per second (TPS)** in its initial stages.

> **Sharding** is a process of horizontally splitting a database into smaller parts or shards. This aims to improve the management and performance of the network by making it lighter and easier to operate.

All of this occurred **without affecting the Ethereum Virtual Machine (EVM)**, with **no interference to existing protocols or deployed smart contracts**, and **without losing any tokens or balances** in the process.  
In fact, all historical data from the current Ethereum (**ETH1**) is fully integrated into **ETH2**, and the transition is **seamless** for users.

---

## **New Terms Introduced with the Ethereum Merge:**

- **Attestation:** A validator’s vote to approve or disapprove the validity of a block.
- **Checkpoint:** A pair of blocks at the head of an epoch used to determine finality.
- **Epoch:** A group of 32 slots, roughly 6.4 minutes. If “justified,” it has been voted valid and can initiate the next checkpoint. If “finalized,” it can no longer be changed.
- **Slashing:** A penalty mechanism for malicious validators. A significant portion of their staked ETH is forfeited as punishment.
- **Slot:** A 12-second period during which a randomly chosen validator can propose a block. Some slots may be empty if the validator is inactive.
- **Validators:** Entities that validate and propose new blocks in the PoS consensus model. They are rewarded in ETH, as miners were in PoW.

---

## **Curiosities After Ethereum Merge and ETH2**

- **Gas costs and transaction fees** on the network **have not changed** with the Merge. ETH2 **does not reduce transaction costs**.
- **Scalability of Ethereum** with ETH2 **has not improved yet**, as block size and block production remain the same. Scalability will depend on **shard chains**, expected in **2024**.
- Current ETH2 stakers must wait for the **Shanghai upgrade** to **withdraw rewards** accumulated during the Beacon Chain phase. Those staking after the Merge will receive rewards immediately.
- The **EVM update** and the rollout of **Swarm** are still under development. There is no official roadmap with fixed dates. It's recommended to follow Ethereum’s official website for updates.

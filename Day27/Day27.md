## **How Does Consensus Work in a Blockchain?**

After understanding the basic concepts, it's important to grasp how the **consensus process** works in a blockchain. Below are the key steps that illustrate how consensus is achieved in this decentralized environment.

---

## **Steps of the Consensus Process**

### 1. Transaction Creation

When a user wants to make a transaction, it is **created and sent** to the network of nodes.

### 2. Transaction Propagation

The created transaction is **broadcasted** to all nodes in the network. Each node receives it and adds it to its list of pending transactions, known as the **mempool**.

### 3. Transaction Verification

Nodes begin to **verify** the transaction by checking:

- The sender has sufficient funds.
- The transaction hasn’t already been sent (prevention of **double spending**).

### 4. Block Creation

Once verified, the transaction is **grouped** with others into a new **block**, which is then broadcast to the network for validation.

### 5. Consensus

Nodes must reach a **general agreement** on the validity of the new block. This may involve:

- Solving **mathematical problems** (as in Bitcoin, using proof of work).
- **Randomly selecting validators** (as in Ethereum, using proof of stake).

Depending on the consensus algorithm used, a node may:

- **“Mine”** the block (as in Bitcoin).
- **“Validate”** the block (as in Ethereum).

### 6. Addition and Linking to the Chain

Once consensus is reached:

- The block is **added** to the existing blockchain.
- All nodes update their **copy of the ledger** to reflect the new state of the network.

---

This consensus mechanism allows the blockchain to operate in a **secure and efficient** way, ensuring that all participants have a **consistent and trustworthy** view of transactions.

> **Consensus not only enables decentralized block validation, but it is also the heart of the system that maintains trust and integrity across the entire blockchain network.**

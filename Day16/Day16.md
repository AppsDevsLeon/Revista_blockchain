## **Peer-to-Peer (P2P) Distributed Networks**

A peer-to-peer distributed network consists of multiple interconnected computers, each maintaining an exact copy of the ledger (a record of all transactions).

Information is automatically replicated across all nodes, enabling any malicious or accidental modification to be quickly detected and corrected by the majority of nodes.

![network](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day16/Images/2022-09-30_16-44-49-2f01f6aa2670c613df15c0aadae24c44.webp)

## **What is a Node?**

A node in a blockchain network is an individual computer actively participating in the network. Each node has a complete copy of the ledger, allowing it to independently verify and audit all transactions and detect any irregularities.

![node](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day16/Images/r2.png)

# Blockchain Nodes

A blockchain network maintains security, integrity, and performance through various node types, each performing distinct roles. This document details node types and includes a comparison of blockchain networks based on their node usage.

## **Types of Nodes**

### **Full Nodes**
Full nodes store the complete blockchain ledger. They independently validate all blocks and transactions, enforcing network rules strictly, which enhances decentralization and security.

### **Mining Nodes**
Mining nodes are responsible for:
- Grouping new transactions into blocks.
- Verifying and validating these transactions.
- Proposing new blocks to the network.

### **Regular Nodes**
Regular nodes store a complete or partial copy of the ledger and perform transaction validations. They contribute to the overall network health.

### **Light Nodes**
Light nodes store only essential blockchain data to verify transactions rapidly. They rely on full nodes for complete blockchain information.

### **Archival Nodes**
Archival nodes store the entire blockchain history, facilitating detailed analysis and audits.

## **Node Comparison Table**

| Node Type       | Ledger Copy         | Validation Role           | Mining Capability | Storage Requirements |
|-----------------|---------------------|---------------------------|-------------------|----------------------|
| Full Node       | Complete            | Complete Validation       | No                | High                 |
| Mining Node     | Complete            | Validation & Creation     | Yes               | High                 |
| Regular Node    | Partial/Full        | Basic Validation          | No                | Moderate             |
| Light Node      | Partial             | Limited Validation        | No                | Low                  |
| Archival Node   | Complete History    | Complete Validation       | No                | Very High            |

## **Blockchain Networks and Node Types Used**

| Blockchain Network | Full Nodes | Mining Nodes | Light Nodes | Archival Nodes |
|--------------------|------------|--------------|-------------|----------------|
| Bitcoin            | ✔️          | ✔️            | ✔️               | ✔️               |
| Ethereum           | ✔️          | ✔️                     | ✔️                | ✔️              |
| Litecoin          | ✔️          | ✔️           | ✔️         | ❌              |
| Solana             | ✔️                | ❌ (validators instead)   | ✔️(validators)    | ❌              |
| Cardano           | ✔️           | ❌ (validators instead) | ✔️(validators)    | ✔️              |
| Polkadot           | ✔️           | ❌ (validators instead) | ✔️(validators)    | ✔️              |

---

## **Benefits of Node Diversity**

- **Security and Resilience:** Diversity in node types enhances overall network robustness.
- **Transparency:** Multiple nodes ensure the accuracy and integrity of blockchain data.
- **Decentralization:** Prevents a single entity from controlling the blockchain network.

## **Benefits of Distributed Networks**

- **Resilience:** By maintaining identical copies across multiple computers, any corrupt data can be easily detected and restored.
- **Transparency:** Every transaction is verifiable and auditable by any node.
- **Security:** Malicious modification requires simultaneous control of the majority of nodes, which is extremely difficult.

---

## **Decentralization**

A blockchain network uses a decentralized model, storing data on multiple distributed nodes. This significantly differs from traditional centralized storage, where all information resides at a single point of control.

---

## **Problems with Centralization**

Significant issues with centralized systems include:

- **Security breaches:** Exposing large amounts of data in case of attacks.
- **Censorship:** A centralized authority can censor and shut down content or services.
- **Dependency:** Technical problems at a central authority impact all users (e.g., AWS downtime).

---

## **Benefits of Decentralization**

Conversely, decentralization offers:

- **Censorship resistance:** No single authority can restrict information.
- **High availability:** Without central points of failure, the network remains operational even if some nodes fail.
- **Enhanced security:** Difficult to manipulate as it would require simultaneous control over the majority of nodes.

---

## **Security in P2P Networks**

Security in peer-to-peer blockchain networks is achieved through:

- **Cryptographic Links:** Each block is cryptographically connected to the previous one, making modifications difficult.
- **Distributed Consensus:** Modifying the network would require simultaneously altering more than half of the nodes, a nearly impossible task.


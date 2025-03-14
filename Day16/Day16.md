## **Peer-to-Peer (P2P) Distributed Networks**

A peer-to-peer distributed network consists of multiple interconnected computers, each maintaining an exact copy of the ledger (a record of all transactions).

Information is automatically replicated across all nodes, enabling any malicious or accidental modification to be quickly detected and corrected by the majority of nodes.

![network](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day16/Images/2022-09-30_16-44-49-2f01f6aa2670c613df15c0aadae24c44.webp)

## **What is a Node?**

A node in a blockchain network is an individual computer actively participating in the network. Each node has a complete copy of the ledger, allowing it to independently verify and audit all transactions and detect any irregularities.

![node](https://github.com/AppsDevsLeon/Revista_blockchain/blob/main/Day16/Images/r2.png)

## **Types of Nodes**

### Regular Nodes
These nodes store a complete copy of the ledger, validate transactions, and ensure overall network integrity.

### Mining Nodes
Mining nodes are responsible for:
- Grouping new transactions into blocks.
- Verifying and validating those transactions.
- Proposing the new blocks to the rest of the network for inclusion in the global ledger.

Miners receive cryptocurrency rewards for their validation work.

---

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


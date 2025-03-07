## **Fundamentals of Blockchain and the Pillars of the Technology**

Blockchain is a revolutionary technology that has transformed the way we manage trust in digital information. To understand how it works, it is essential to know its fundamental principles and how each of its elements ensures the security, transparency, and reliability of the system.

## **What is the problem with traditional systems?**

In traditional systems, the authenticity of documents like academic certificates, contracts, and financial records depends on centralized entities, which create vulnerabilities:

- **Risk of forgery**: Documents or transactions can be altered.
- **Dependency on third parties**: Governments, banks, and companies verify the information.
- **Data manipulation**: If a central entity suffers a breach, the information could be compromised.

Blockchain offers a solution by eliminating intermediaries and ensuring data integrity through advanced cryptography and decentralization.

## **The Fundamental Pillars of Blockchain**

### **1. Security: The Foundation of Trust**

#### What risks exist in traditional systems?
- **Risk of fraud or manipulation**: In traditional systems, data can be altered or deleted undetected, as they rely on a central entity to maintain information integrity.
- **Dependence on a single control source**: Data is usually stored in a centralized database, creating single points of failure.

#### How does Blockchain resolve it?
- **Advanced Cryptography (SHA256)**: Each block contains a unique hash code that acts as a digital seal, ensuring the information hasn't been altered. This guarantees that any attempt to modify a block would alter the entire chain, making it evident to all participants.
- **Immutability**: Once a block is recorded, it cannot be modified without invalidating the entire chain. This ensures that data cannot be manipulated.
- **Distribution**: Information is not stored in one place. Instead of relying on a central entity, the blockchain network distributes data across thousands of nodes (computers), avoiding a single point of failure.

### **2. Transparency: Everything in Sight, No Tricks**

#### What risks exist in traditional systems?
- **Opacity**: In traditional systems, processes can be hidden, preventing stakeholders from verifying the truthfulness of transactions or records.
- **Lack of traceability**: It is difficult to verify the history of transactions without access to the complete database, which could allow for manipulation.

#### How does Blockchain resolve it?
- **Public digital ledger**: Blockchain records all transactions in a ledger accessible to all network users. Anyone can verify transactions at any time, increasing trust in the system.
- **Accessibility and data protection**: Although transactions are public, they are secured by cryptography, ensuring that only authorized parties can make changes.

### **3. Decentralization: No Single Owner**

#### What risks exist in traditional systems?
- **Dependence on a central authority**: In traditional systems, one entity controls the information and the validation process. If this entity is corrupt or has issues, the entire system is affected.
- **Risk of censorship or blocking of information**: The central authority can manipulate or block access to information.

#### How does Blockchain resolve it?
- **Distributed network**: Instead of relying on a central authority, blockchain distributes information across thousands of nodes (computers) in the network, each of which validates transactions. This eliminates the risk of manipulation by a single entity.
- **No points of failure**: If a node is compromised, the network continues to operate correctly thanks to the data distribution. Additionally, the network validates transactions collectively, ensuring the information’s accuracy without a single control point.

### **4. Anonymity: Privacy with Traceability**

#### What risks exist in traditional systems?
- **Exposure of personal identity**: Traditional systems often require users to provide sensitive personal information (such as names and addresses), which can be vulnerable to identity theft or leaks.
- **Risk of surveillance**: Transactions can be easily traced, exposing users' personal details.

#### How does Blockchain resolve it?
- **Alphanumeric addresses instead of real names**: Instead of exposing user identities, blockchain uses alphanumeric addresses that allow traceability without compromising privacy.
- **Traceability without identity disclosure**: Although transactions are publicly verifiable, users’ identities are protected through cryptography. This allows transactions to be traced without exposing user privacy.

### **5. Immutability: The Impossibility of Altering Records**

#### What risks exist in traditional systems?
- **Record manipulation**: Traditional systems may allow records to be altered by individuals with access to central databases, which creates insecurity in data integrity.
- **Retroactive changes without control**: Once data is modified, it can be difficult to verify or detect these alterations.

#### How does Blockchain resolve it?
- **Interconnected chain of blocks**: Blockchain ensures that once a block is recorded, its information cannot be altered without changing the entire chain. This is achieved through the use of hashes that link blocks together.
- **Immediate detectability**: If someone tries to alter a block, its hash would change, invalidating not only that block but all subsequent blocks, immediately alerting the network.

### **6. Consensus: Ensuring Transaction Validation**

#### What risks exist in traditional systems?
- **Unitary validation**: In traditional systems, transactions and records can be validated by a single entity, which introduces risks of fraud and errors.
- **Lack of trust**: Relying on a single authority to validate transactions can generate mistrust among the parties involved.

#### How does Blockchain resolve it?
- **Consensus mechanisms**: Blockchain uses algorithms like Proof of Work (PoW) or Proof of Stake (PoS) to ensure that all transactions are validated in a decentralized manner by the network, removing the need to trust a single entity.
- **Trust without intermediaries**: Thanks to consensus mechanisms, all participants in the network validate transactions and ensure their correctness, eliminating the need to trust a single party.

## **Key Components of Blockchain**

In addition to the fundamental pillars of security, transparency, decentralization, and anonymity, blockchain is composed of several elements that allow it to function properly. Below are some of these key components:

### **1. SHA256 (Secure Hash Algorithm 256-bit)**

**SHA256** is a cryptographic hash function that converts any set of data into a unique 256-bit sequence. This function is crucial in blockchain for several reasons:

- **Security**: SHA256 is collision-resistant, meaning it’s impossible to generate two different inputs that produce the same hash. This ensures each block is unique.
- **Immutability**: If a block is altered, its hash changes, invalidating the block and all subsequent blocks. This mechanism ensures no data manipulation.
- **Quick verification**: SHA256 allows for quick verification if a block has been altered, making blockchain an extremely secure and efficient system.

**Example**: If a $100 transaction is recorded, the hash of that transaction will be unique. If someone tries to change the amount or recipient, the hash will change, and the alteration will be easily detected.

### **2. Timestamping**

**Timestamping** is the process of recording the exact time and date when a block is created. This element is essential for ensuring that data is accurate and verified.

- **Purpose**: The timestamp ensures that the block is valid at a specific moment, helping to organize transactions chronologically.
- **Importance**: Without proper timestamping, it would be difficult to determine whether one transaction occurred before or after another, potentially leading to disputes.

**Example**: In a smart contract, timestamping ensures that the contract’s execution occurs at the right time and that the date and time of the transaction cannot be altered.

### **3. Transactions in Blockchain**

**Transactions** are the core of blockchain. They are the operations recorded and verified across the network of blocks. Each transaction is securely, immutably, and transparently recorded.

- **Purpose**: Transactions enable users to exchange value securely. Blockchain verifies and records each one to ensure its validity.
- **Process**: Transactions are grouped into blocks and distributed across the network, where nodes validate their authenticity.

**Example**: In the case of Bitcoin, when a user sends money, the transaction is verified by the network and recorded in a blockchain block.

### **4. Nonce (Number Used Once)**

The **nonce** is a random number used during the **mining** process of blockchain. Miners must find a nonce that, when combined with the block data, produces a hash that meets a specific difficulty criterion.

- **Purpose**: The nonce ensures that the block is unique and prevents miners from manipulating the validation process.
- **Proof of Work**: The use of nonce is part of the **proof-of-work** mechanism, which ensures that significant computational work is done to validate the block.

**Example**: Bitcoin miners must find a nonce that makes the block’s hash meet a certain number of leading zeros. This process requires computational power and guarantees that only miners with sufficient resources can add blocks to the chain.

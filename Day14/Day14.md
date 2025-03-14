## **Blockchain Blocks**

Let's expand the concept of a hash into something we call a block in blockchain technology.

## **What is a Block?**

A blockchain block organizes information into three clearly defined main parts:

- **Block Number:** A unique identifier indicating the block's position in the chain.
- **Nonce:** An arbitrary number used to adjust the block's hash to meet specific requirements.
- **Data:** Specific information stored within the block (e.g., transactions).

The following image illustrates the typical structure of a blockchain block:

![Blockchain Block](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a20.png)

The block's hash includes all the above information. For example, the hash shown above starts with four zeros (`0000`). This type of hash is relatively rare and signifies a valid or "signed" block.

## **What Happens if Block Data is Modified?**

If any data within the block is modified, the resulting hash will change completely and likely will no longer meet the original requirement (starting with four zeros). For example:

![Modified Block](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a21.png)

Here, the hash no longer starts with four zeros, indicating the block is invalid. The red background visually indicates that the block is invalid or unsigned.

To solve this issue, the Nonce value is adjusted until a hash is found again meeting the initial requirement (starting with four zeros). For example:

![Valid Block after adjusting Nonce](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a22.png)

In this case, a Nonce was found that generates a valid hash, making the block valid and signed again.

## **Information Stored in Blocks According to Blockchain Networks**

Each blockchain network may store slightly different information in its blocks, but generally includes similar key elements. Here is a comparative table:

| Blockchain Network | Block Contents                                                                                   |
|--------------------|--------------------------------------------------------------------------------------------------|
| **Bitcoin**        | Previous Hash, Timestamp, Nonce, Transactions, Merkle Root                                       |
| **Ethereum**       | Previous Hash, Timestamp, Nonce, Transactions, Merkle Root, Gas Used, Block Number                |
| **Litecoin**       | Previous Hash, Timestamp, Nonce, Transactions, Merkle Root                                       |
| **Solana**         | Previous Hash, Timestamp (Proof of History), Transactions, Signatures, Validators                 |
| **Cardano**        | Previous Hash, Timestamp, Nonce, Transactions, Cryptographic Proofs, Merkle Root                  |
| **Polkadot**       | Previous Hash, Timestamp, Transactions, Parachain Validations, Validity Proofs                   |

## **Key Components of a Block**

- **Previous Hash:** Cryptographic link to the previous block.
- **Timestamp:** Indicates the exact time when the block was created.
- **Nonce:** Arbitrary number used to adjust the block's hash to meet specific criteria.
- **Transactions:** Records of transactions stored within the block.
- **Merkle Root:** Enables fast validation and verification of transaction integrity.


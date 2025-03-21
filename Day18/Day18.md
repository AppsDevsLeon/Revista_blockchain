
## **Nonce Concept**

The term **nonce** (from English *number used once*) is an arbitrary number that miners can freely modify to find a **valid hash** for a block. This number has no function other than altering the result of the hash algorithm until it meets a predefined difficulty condition (e.g., the hash starts with a certain number of zeros).

---

## **Structure of a Block and the Role of the Nonce**

A typical block contains:

- Block number.
- List of transactions.
- Previous block hash.
- **Nonce** ← *value modified during the mining process.*
- Current block hash.

The formula to calculate the block hash would be:

```text
Hash = SHA256(block_number + transactions + previous_hash + nonce)
```

 **Important**: The only field that miners can modify without violating the integrity of the data is the nonce. Everything else must remain intact.

---

## **Visual Example of a Block**

This image represents:

- The block number.
- The included transactions.
- The Previous Hash.
- The Nonce field.
- The Current Hash.

---

The image shows the structure of a block in a blockchain, specifically block #3, which contains key information such as:

Block number: Indicates its position in the chain.
Nonce: A field that is empty in this case, but used in mining to find a valid hash.
Transaction data: Records the transactions in this block, including "jbcoins" transfers between users.
Prev. Hash: The hash of the previous block, ensuring the continuity and integrity of the chain.
Hash: The unique fingerprint of the block, generated from all the information in the block.

![nonce](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day18/Images/Nonce1.png)

## **How the Nonce Works in Practice**

Suppose we have a block with the following data:

- Block number: 42
- Data: "Alice sends 5 BTC to Bob"
- Previous hash: a7f4...d1e2
- Initial nonce: 0

With this data, a hash is calculated. If the hash does not start with the required zeros (e.g., 0000...), the miner increments the nonce: 1, 2, 3, ..., and recalculates the hash until a value that meets the difficulty criterion is found.

---

## **Illustration of the Hash Change with Different Nonces**

```text
Fixed data:
- Block number: 42
- Transaction: Alice sends 5 BTC to Bob
- Previous hash: a7f4...d1e2

Iterations:

Nonce = 0      → Hash = 1f7c3a5e9b...
Nonce = 1      → Hash = 83adf26711...
Nonce = 2      → Hash = 00a9c8de42... ✅ (valid)
Nonce = 3      → Hash = c7e4b8d231...
```

Each small change in the nonce produces a completely different hash. This behavior is known as the **avalanche effect**.

---

## **Image: Avalanche Effect When Modifying the Nonce**

Each minimal change in the nonce generates a radically different hash.

---

## **Search Space and Energy Consumption**

- The nonce in Bitcoin is a 32-bit integer, allowing for up to `2³² = 4,294,967,296` possible attempts per block.
- If a valid hash is not found within that range, the *timestamp* or other complementary values (*extra nonce*) are modified.
- Due to the number of possible attempts, a large computational capacity is required to find the correct hash. This is why mining consumes enormous amounts of energy.

---

## **Illustrated Mining Process**

```text
[Block Data] + [Previous Hash] + [Nonce]
        ↓
      SHA-256
        ↓
Does it meet the difficulty criterion (e.g., starts with 0000...)?
    ↓                         ↓
 [Yes]                      [No]
Save block              Increment nonce
to the chain               and repeat
```

---

## **Image: Miners Testing Different Nonces**

---

The **nonce** field is at the core of the **Proof of Work (PoW)** mechanism. Its existence allows miners to "play" with the block's content without altering the data or breaking the integrity of the chain.

- It allows variability without modifying the data.
- It is the only freely modifiable field to generate different hashes.
- It is responsible for the enormous energy cost of PoW.

In the next section, we will explain how the mining difficulty adjusts automatically and how it affects the time to create new blocks.

## **References**

- Nakamoto, S. (2008). *Bitcoin: A Peer-to-Peer Electronic Cash System*.
- Mastering Bitcoin (Andreas M. Antonopoulos).
- Blockchain Course – Mining and Proof of Work Module.


## **Increase in Mining Difficulty in Blockchain**

Now that we understand the cryptographic puzzle of mining, it's time to move forward and look at how the difficulty of this process increases and why it is necessary. As we have seen, mining focuses primarily on the nonce field, which is controlled by the miners and changes in order to generate different hashes until a valid one is found.

The probability of finding a valid hash is very small, which results in constant competition among miners.

## **The Range of Nonces and the Difficulty of Finding a Valid Hash**

A block contains a field that holds a value of 32 bits of allocated memory. This means there is a limited range of around 4 billion possible values for the nonce.

### **How Do We Know the Number of Values?**

A 32-bit value can be either a 1 or 0 bit, meaning it has two possible values. This gives us a total of:

```text
2^32 = 4,294,967,296 possible values
```

This gives us a range of approximately 4 billion possible values for the nonce.

### **Example: Calculations of an Average Miner**

An average miner can calculate up to 100 million hashes per second. This means they can calculate the entire range of 4 billion possible values in just 40 seconds.

```text
4,294,967,296 values / 100,000,000 calculations per second = 40,000 seconds
```

**Mining pools** and **industrial miners** can traverse this entire range of values in fractions of a second.

### **The Problem: Low Probability of Finding a Valid Hash**

Although the calculation is fast, the probability of finding a valid hash is extremely low, even after traversing the 4 billion possible attempts. The probability of finding a valid hash is:

```text
P(valid hash) = 16^(-18) (an extremely low probability)
```

## **How to Increase the Difficulty of Mining?**

To prevent blocks from being created in seconds or fractions of seconds, it is necessary to increase the difficulty of the cryptographic puzzle. This is done by adding a new field in the block: the **timestamp**.

### **What is the Timestamp?**

The timestamp is a field that represents the number of seconds elapsed since January 1, 1970 (Unix time). This timestamp changes every second and is included as part of the hash calculation of the block.

The formula for the block hash now depends on the block identifier (block number), the timestamp, the nonce, the data, and the previous hash.

### **Example of Calculation with Timestamp**

```text
Hash = SHA256(block_number + timestamp + nonce + data + previous_hash)
```

### **The Problem with Industrial Miners**

While average miners may take up to 40 seconds to calculate the entire nonce range, industrial miners or mining pools can do this in fractions of a second. However, the timestamp, which changes every second, allows average miners to restart their calculations, as the change in the timestamp makes the hash calculation different every second.

### **How Difficulty is Increased for Industrial Miners**

To further complicate the process for industrial miners, large mining pools, with their enormous computational power, can perform calculations in fractions of a second. To counteract this, the difficulty is adjusted to ensure that a new block is created approximately every **10 minutes**, not in fractions of a second.

### **Solution: Use of MemPool and Difficulty Adjustments**

An effective solution to the increased computational power of industrial miners is the use of **MemPool** and automatic difficulty adjustments. This ensures that mining remains an efficient and fair process for all participants, regardless of their computational power.

## **Conclusion: Difficulty and Block Creation in Blockchain**

Mining in blockchain is a highly competitive process where miners must calculate valid hashes while facing an extremely low probability of success. To ensure that block creation is efficient and not completed in seconds or fractions of seconds, the difficulty is increased by adjusting the timestamp and using mechanisms like MemPool. This keeps the process under control and ensures that the goal of generating a block every 10 minutes is met.


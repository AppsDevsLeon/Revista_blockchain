## **Hash, Hashing, and SHA-256**

Before we start, we need to understand exactly what a hash is, and more specifically, the SHA-256 hash. A hash appears as a seemingly random sequence of numbers and letters, acting as a unique digital fingerprint of specific digital data.

## What is SHA-256?

SHA-256 (Secure Hash Algorithm 256-bit) is a cryptographic function that generates a unique, fixed-length 256-bit (32 bytes) string, typically represented in hexadecimal with 64 characters. This algorithm exclusively generates hexadecimal values, meaning numbers from 0-9 and letters from A to F.

Before we proceed, let's take a closer look at SHA-256 hashes. A hash looks like a bunch of random numbers and serves as a digital fingerprint of specific digital information.

For example, the following hash begins with `e3b0`, representing the SHA-256 hash when there's no data (an empty value):

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a18.png)

If we type any text into a box, such as the word `blockchain`, the generated hash changes completely:

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a19.png)

The specific hash for the word "blockchain" is:

```
ef7797e13d3a75526946a3bcf00daec9fc9c9c4d51ddc7cc5df888f74dd434d1
```

If we slightly modify the original text, for example changing the last letter to uppercase (`blockchaiN`), the resulting hash is entirely different:

```
6cfa1dbb6eb068b5050efee9f90a954fb0896e5c97e84713bfe023b9408c2cef
```

You could write tons of text and always get a hash of the same length. Whether it is a tiny amount of information, no information, or the entire digital contents of the Library of Congress, the hash length will always remain the same as shown above. You will never guess what the hash will be, but it will always be the same hash whenever you enter the exact same data.

## Mathematical Properties of SHA-256

SHA-256 employs rigorous mathematical procedures involving logical and arithmetic operations, such as:

- **Bitwise operations**: AND, OR, XOR, NOT
- **Bit shifts**: rotations and right shifts
- **Modulo 2³² additions**: binary addition with controlled overflow (mod 2³²)

The algorithm processes data in 512-bit blocks (64 bytes). Each block is divided into 16 words of 32 bits, which are then expanded into 64 words through a mathematical expansion and mixing process, enhancing security and apparent randomness.

These operations ensure SHA-256’s high security, making it resistant to known cryptographic attacks.

## Important Properties of SHA-256

- **Fixed length**: Always 256 bits, represented as 64 hexadecimal characters (0-9 and A-F).
- **Deterministic**: The same input always produces the same hash.
- **One-way**: It is impossible to reverse a hash to recover original data.
- **Collision-resistant**: Virtually impossible to find two different inputs generating the same hash.

## Avalanche Effect

SHA-256 exhibits the **avalanche effect**, meaning even a small change in the original data will result in a completely different and unpredictable hash. This is crucial for ensuring data integrity and security.

For example:
- Original text: `blockchain`
  - Hash: `ef7797e13d3a75526946a3bcf00daec9fc9c9c4d51ddc7cc5df888f74dd434d1`
- Modified text: `blockchaiN`
  - Hash: `6cfa1dbb6eb068b5050efee9f90a954fb0896e5c97e84713bfe023b9408c2cef`

This property makes it impossible to alter data without significantly changing the resulting hash, ensuring integrity across multiple technological applications.

## Applications of SHA-256

SHA-256 is widely used in:

- Blockchain (Bitcoin, Ethereum, etc.)
- File integrity verification
- Secure password storage
- Digital signatures

The significance of SHA-256 lies in its combination of speed and security, making it indispensable in numerous modern technological applications.


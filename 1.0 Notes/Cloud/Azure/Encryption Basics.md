Encryption

Encryption - commonly used to protect the confidentiality of data in transit and rest,. 

![[encryptpic.png]]

### Symmetric encryption

Symmetric encryption - uses the same key to encrypt and decrypt (Single Key, shares key, secret key, session key)

- Symmetric Algorithms
    - DES
        - 64 bit key size 16 rounds of substitution and transposition
        - broken in 56 hours in 1998
    - 3DES
        - 64 bit key/48 rounds of substitution and transposition using either 2/3 keys
        - Replaced DES as US Gov standard in 1999
        - Considered deprecated
    - AES | Rijndael
        - 128/192/256 bits: 10/12/14 rounds of substitution and transposition
        - replaced 3DES in 2002 as US Gov Standard
    - RC4
        - Stream Cipher
        - Key Sizes 40-2048 bits
        - 4 Variants
            - Spritz
            - RC4A
            - VMPC
            - RC4a+
    - Symmetric Characteristics
        - Processing
            - Computationally efficient
        - Key Size
            - generally, 128/192/256 bit
        - Scalability
            - Not Scalable
        - Key Exchange
            - inherently insecure

### Asymmetric encryption

asymmetric encryption - uses two mathematically related keys to encrypt and decrypt. usually, referred to public and private key. Public key is freely distributed. Private key must be secured

![[asym.png]]

- Asymmetric Algorithms
    - RSA
        - Widely implemented de facto commercial standard
        - Works with both encryption and digital signitures
    - Elliptic Curve Cryptosystem (ECC)
        - similar function to RSA but with smaller key sizes (required less computing power)
        - Current us government standard
    - Diffie-Hellman
        - Primarily used for key agreement/exchange
        - Allows 2 parties in same DH group to jointly establish a shared secret key
    - EL Gamal
        - used for transmitting digital signatured and key exchange
- Asymmetric Characteristics
    - Processing
        - computaitionally intensive
    - Key Size
        - Generally 2048 or greater
    - Scalability
        - Scalable
    - Key Exchange
        - designed for key exchange

**Message Flow - Hybrid**

![[symm.png]]

Symmetric vs. Asymmetric

| Feature | Symmetric | Asymmetric |
| --- | --- | --- |
| # of Keys | Single Shared Key | Key Pair |
| Block Sizes | Large | Small |
| Processing | computationally Efficient | Computationally intensive |
| scalability  | no scalable  | Scalable  |
| Key Exchange | Key Exhange is inherently insecure | Key exchange Distributuion system |

**Key management** 

Key Management - describes he activity involving the handeling of cryptographic keys during entire life cylcle 

- Usage
    - Key Should only be used for one purpose
- Strength
    - Strength should be commensurate with data/ process protection requirements
- Storage
    - keys must be securely stored
- KPMS
    - Key management practice statement - document that outlines in detail the org structure, responsible roles and rules for key management


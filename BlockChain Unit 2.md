## **Cryptography**

### Definition
- It is the **study and practice** of keeping secret information away from adversary
- **BitCoin** was intially proposed as a cryptograpy based currency that would avoid the downsides of a centralised institution
- The idea of transferring value through a **chain of digital signatures** 
-  The idea rose from **Juilius Caesar** who did not trust his messengers and developed a system in which each alphabet was replaced by a character **three positions** ahead of it in the roman alpahabet

## Objectives of **Cryptography**

1. Confidentiality 
	- Only Target will recieve the information 
	- Cannot be understood by anyone else
2. Integritiy 
	- Data cannot be modified
	- No tampering of data without being noticed by others 
3. Non-Repudiation
	- It is the assurance that someone cannot deny the validity of something
	- Sender cannot deny that he did not perform the transaction
4. Authentication
	- Identification of sender and reciever verified before transactions

# **Cryptographic Ciphers**



## **Symmetric Ciphers** (K1=K2=K)

## How it works?

- Very basic and old method 
- It uses **Single-Key Encryption**
- The **encrypting** key and **decrypting** key is the same


![[Symmetric Ciphers.png]]

### Examples
1. AES
2. DES

## Types of **Symmetric Cipher**

- [[#Transposition Cipher]]
- [[#Substitution Cipher]]
- [[#Stream Cipher]]
- [[#Block Cipher]]

### Transposition Cipher 

1. Change the position of the characters in a text by referring to a **key**
2. The **Order of numbers** in that key is how the columns are arranged
![[Trans_Cipher.png]]

3. For Decryption ,just sort the column headers by numbers and rearrange

### Substitution Cipher

1. Somewhat similar to Caesar Cipher
2. A keyword n is given, we just pick the letter in the nth position after that letter
3. While Decrypting we just go backwards

#### Example
Plain Text : Data Encryption
Keyword : 4
Cipher Text: Hexe Irgvctxmsr

### Stream Cipher
	OTP/RC4

Bit by Bit Conversion

**One byte** is encrypted at a time while in ***block cipher*** **128 bits** are encrypted at a time

## DES - Data Encryption Standard

1. Symmetric Key **Block Cipher** by NIST
2. Proposed by IBM
3. It uses **16 round Feistel Structure**
4. The block size is **64** bit
5. The effective key length is **56** bits, since **8** bits of the key are not used by the encryption algorithm
6. DES is weak against **brute force attacks**

## Disadvantages of Symmetric Key Cryptography

1. The number of keys between parties increases somewhat at quadratic speed
2. No validity for the origin of keys
3. Both sides use the same key,not that secure

## Assymetric Key Cryptography

-  Uses **private key** and **public key** mechanism.
![[AsyKey.png]]
- The **private key** is only known to the user/owner and needs to be kept **private**.**Public key** may be given to anyone.
- Senders can combine a message with their private key to create a **digital signature** on the message.
- Anyone with the corresponding **public key** can now verify whether the signature is **valid**

### RSA - **Rivest–Shamir–Adleman**

	TBD 

## Digital Signatures
- Electronic Fingerprints 
- Digital signatures use a standard, accepted format, called **Public Key Infrastructure (PKI)**

### But why? 

1. Provide **Authenticity , Integrity , Non-repudiation** 

> [!NOTE]
> Non Repudiation here means neither the user nor the sender can deny of having processed the information

2. To use the Internet as the safe and secure medium for Banking, e-Commerce and e-Governance with Security of Servers

## Digital Signatures in BlockChain

![[Sign_BlockChain.png]]

- Bitcoin uses **Elliptic Curve Digital Signature Algorithm (ECDSA)**,Based on **elliptic curve** cryptography Supports good randomness in key generation

## **Hash** Functions 

1. A c**ryptographic hash function** takes data and essentially  translates it into a **string of letters and numbers**.
2. Data goes into a **hash function**, the function runs, and a string of letters and numbers is produced, that string is called a **hash**.
3. In the BitCoin Blockchain hashes are **256 bits or 64 characters** .

### Features 
1. Takes any input length string 
2. Produces fixed size output 
3. Easy to compute 
4. Almost impossible to reverse 
5. Collision resistant 
6. Hides original string 
7. Almost impossible to get original string from hash value 
8. Puzzle friendly

### Popular Hash Functions

1. Message Direct
2. Secure Hash Algorithm


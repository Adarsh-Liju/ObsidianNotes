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

1. **One byte** is encrypted at a time while in ***block cipher*** **128 bits** are encrypted at a time
2. 




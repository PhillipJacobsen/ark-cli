# Example CLI using ARK Blockchain SDK

This project is intended to provide an example of how to integrate the [ARK.io Blockchain](https://ark.io/) SDK into a node.js application. It implements a command line interface to perform tasks such as check wallet balance, sign / verify messages, and send transactions.

## Installation

`npm install`

In package.json file configure the ip address of your ARK relay node via **nodeIP** parameter.

In package.json file configure the network(devnet or mainnet) via **network** parameter.

## Using the CLI

To get list of commands: `ark-cli --help`

To get help on each command: `ark-cli <command> --help`

### Commands

- **ark-cli relay** Get status of relay node used for accessing blockchain
- **ark-cli validate** Validate a wallet address
- **ark-cli peers** Get list of peers
- **ark-cli nonce** Get nonce of wallet
- **ark-cli balance** Get balance of wallet
- **ark-cli sign** Sign message using Schnorr algorithm
- **ark-cli verify** Verify Signature using Schnorr algorithm
- **ark-cli tx** Send transaction with optional smartbridge message
- **ark-cli tx-ipfs** Send IPFS transaction

### **ark-cli relay**

**Description:** Get status of relay node used for accessing blockchain  
**Options:** none

### **ark-cli validate**

**Description:** Validate a wallet address  
**Options:**  
 --adr wallet address

### **ark-cli peers**

**Description:** Get list of peers  
**Options:** none

### **ark-cli nonce**

**Description:** Get nonce of a wallet  
**Options:**  
 --adr wallet address

### **ark-cli balance**

**Description:** Get balance of a wallet  
**Options:**  
 --adr wallet address

### **ark-cli sign**

**Description**: Sign message using Schnorr algorithm  
**Options:**  
 --msg Message to be signed  
 --passphrase Your Private Passphrase(12 words)

### **ark-cli verify**

**Description:** Verify Signature using Schnorr algorithm  
**Options:**  
 --msg Message to be signed  
 --publicKey Public key of sender  
 --signature Message signature

### **ark-cli tx**

**Description:** Send transaction with optional smartbridge message  
**Options:**  
 --adr Recipient's Address  
 --amt Amount of coins to send  
 --fee Transaction fee amount  
 --passphrase Your Private Passphrase(12 words)  
 --smartbridge Message to include with transaction(optional)

### **ark-cli tx-ipfs**

**Description:** Send IFPS transaction
**Options:**  
 --hash IPFS Hash  
 --fee Transaction fee amount  
 --passphrase Your Private Passphrase(12 words)  

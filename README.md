# Example CLI using ARK.io Blockchain SDK

This project is intended to provide an example of how to integrate the [ARK.io Blockchain SDK](https://ark.dev/docs/sdk/) into a node.js application. It implements a command line interface to perform tasks such as check wallet balance, sign / verify messages, and send transactions.

## Installation on Ubuntu
1. Install build essential tools  
`sudo apt install build-essential`

2. Install Node Using the Node Version Manager(NVM)  
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash`  
`source ~/.bashrc`  
`nvm install v16.15.1`  

3. Download ark-cli program  
`git clone https://github.com/PhillipJacobsen/ark-cli.git`

4. install program  
`cd ark-cli`  
`npm install`  
`npm link`  

5. In package.json file configure the ip address of your ARK relay node via **nodeIP** parameter.

6. In package.json file configure the network(devnet or mainnet) via **network** parameter.

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

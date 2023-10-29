

<!-- TOC -->

- [00:00 Introduction](#0000-introduction)
	- [Workshop Introduction](#workshop-introduction)
- [00:26 Overview of Solana Network](#0026-overview-of-solana-network)
	- [Technical Advantages of Solana](#technical-advantages-of-solana)
	- [How Solana Network Works](#how-solana-network-works)
- [03:14 General Programming Model on Solana Blockchain](#0314-general-programming-model-on-solana-blockchain)
	- [Accounts on Solana Blockchain](#accounts-on-solana-blockchain)
- [04:29 Conclusion](#0429-conclusion)
	- [Key Takeaways](#key-takeaways)
- [05:02 Understanding Solana Accounts](#0502-understanding-solana-accounts)
	- [Solana Account Structure](#solana-account-structure)
	- [Programs on Solana](#programs-on-solana)
	- [Key Points about Programs](#key-points-about-programs)
- [08:44 Solana Program Instructions and Transactions](#0844-solana-program-instructions-and-transactions)
	- [Structure of Instructions](#structure-of-instructions)
	- [Parallel Execution and Transactions](#parallel-execution-and-transactions)
	- [Key Points about Instructions and Transactions](#key-points-about-instructions-and-transactions)
- [10:35 Understanding Transactions and Signatures](#1035-understanding-transactions-and-signatures)
	- [The Role of Public Keys in Transactions](#the-role-of-public-keys-in-transactions)
	- [Key Takeaways on Transactions and Instructions](#key-takeaways-on-transactions-and-instructions)
- [11:13 Life Cycle of a Transaction](#1113-life-cycle-of-a-transaction)
	- [Client Perspective](#client-perspective)
	- [Transaction Flow](#transaction-flow)
- [12:12 Using and Building Solana Transactions](#1212-using-and-building-solana-transactions)
	- [Example Code Repository Setup](#example-code-repository-setup)
	- [Paying for Transaction Fees](#paying-for-transaction-fees)
	- [Script 1: Simple Transaction](#script-1-simple-transaction)
- [13:46 Understanding Rent in Transactions](#1346-understanding-rent-in-transactions)
- [16:06 Paying for Space on the Blockchain](#1606-paying-for-space-on-the-blockchain)
	- [Allocating Space on the Blockchain](#allocating-space-on-the-blockchain)
- [16:25 Creating an Account](#1625-creating-an-account)
	- [Building Instructions for Account Creation](#building-instructions-for-account-creation)
- [17:13 Constructing a Transaction](#1713-constructing-a-transaction)
	- [Obtaining Block Hash and Building Transaction](#obtaining-block-hash-and-building-transaction)
- [19:13 Signing and Sending the Transaction](#1913-signing-and-sending-the-transaction)
	- [Signing and Sending Transaction](#signing-and-sending-transaction)
- [20:05 Summary of Script Execution](#2005-summary-of-script-execution)
	- [Script Execution Summary](#script-execution-summary)
- [21:20 Understanding the Solana Explorer](#2120-understanding-the-solana-explorer)
	- [Opening Solana Explorer and Basic Information](#opening-solana-explorer-and-basic-information)
	- [Transaction Details](#transaction-details)
- [22:36 Building Complex Transactions](#2236-building-complex-transactions)
	- [Setting Up for Complex Transaction](#setting-up-for-complex-transaction)
	- [Allocating Space on Chain](#allocating-space-on-chain)
	- [Executing Transfer Instructions](#executing-transfer-instructions)
	- [Building Multiple Instructions in a Transaction](#building-multiple-instructions-in-a-transaction)
	- [Atomic Execution of Instructions](#atomic-execution-of-instructions)
	- [Building and Sending the Transaction](#building-and-sending-the-transaction)
- [26:03 Summary of Complex Transaction](#2603-summary-of-complex-transaction)
	- [Summary of Steps](#summary-of-steps)
- [26:45 Building Transactions for the Solana Blockchain](#2645-building-transactions-for-the-solana-blockchain)
	- [Overview of Building Transactions](#overview-of-building-transactions)
- [27:02 Tokens on the Solana Blockchain](#2702-tokens-on-the-solana-blockchain)
	- [Three Programs for Tokens](#three-programs-for-tokens)
- [27:39 Creating a Token on Solana](#2739-creating-a-token-on-solana)
	- [Minting Tokens with Token Program](#minting-tokens-with-token-program)
	- [Ownership via Associated Token Accounts ATA](#ownership-via-associated-token-accounts-ata)
	- [Metadata for Tokens](#metadata-for-tokens)
- [29:14 Creating an SPL Token](#2914-creating-an-spl-token)
	- [Steps to Create an SPL Token](#steps-to-create-an-spl-token)
- [30:27 Demonstration: Creating an SPL Token with Metadata](#3027-demonstration-creating-an-spl-token-with-metadata)
	- [Code Setup and Imports](#code-setup-and-imports)
	- [Configuring Token Metadata](#configuring-token-metadata)
- [32:12 Building Instructions for Creating an Account](#3212-building-instructions-for-creating-an-account)
	- [Creating an Account](#creating-an-account)
- [34:50 Creating Metadata Account](#3450-creating-metadata-account)
	- [Program Derived Address PDA](#program-derived-address-pda)
- [36:54 Bundling Instructions into Transaction](#3654-bundling-instructions-into-transaction)
	- [Bundling Instructions](#bundling-instructions)
- [37:46 Overview of Completed Script and Logged Addresses](#3746-overview-of-completed-script-and-logged-addresses)
	- [Completed Script and Logged Addresses](#completed-script-and-logged-addresses)
- [38:03 Viewing Transaction on Solana Explorer](#3803-viewing-transaction-on-solana-explorer)
	- [Viewing Transaction on Solana Explorer](#viewing-transaction-on-solana-explorer)
- [38:23 Examining Instruction Data and Logs](#3823-examining-instruction-data-and-logs)
	- [Examining Instruction Data and Logs](#examining-instruction-data-and-logs)
- [39:17 Minting Tokens to Associated Token Account](#3917-minting-tokens-to-associated-token-account)
	- [Minting Tokens to Associated Token Account](#minting-tokens-to-associated-token-account)
- [40:27 Understanding Associated Token Account Ownership](#4027-understanding-associated-token-account-ownership)
	- [Understanding Associated Token Account Ownership](#understanding-associated-token-account-ownership)
- [42:18 Minting Tokens with Decimals](#4218-minting-tokens-with-decimals)
	- [Minting Tokens with Decimals](#minting-tokens-with-decimals)
- [43:14 Minting Tokens to Associated Token Account](#4314-minting-tokens-to-associated-token-account)
	- [Minting Tokens](#minting-tokens)
- [43:32 Minting Tokens and Checking Balances](#4332-minting-tokens-and-checking-balances)
	- [Minting Tokens and Checking Balances](#minting-tokens-and-checking-balances)
- [44:10 Minting Additional Tokens](#4410-minting-additional-tokens)
	- [Minting Additional Tokens](#minting-additional-tokens)
- [44:51 Updating Token Metadata](#4451-updating-token-metadata)
	- [Updating Token Metadata](#updating-token-metadata)
- [45:43 Conclusion](#4543-conclusion)
	- [Summary](#summary)
- [49:03 Overview of SPL Tokens on Solana](#4903-overview-of-spl-tokens-on-solana)
	- [Creating New SPL Tokens](#creating-new-spl-tokens)
- [50:20 NFTs as SPL Tokens](#5020-nfts-as-spl-tokens)
	- [Properties of NFTs](#properties-of-nfts)
	- [Master Edition and Collection](#master-edition-and-collection)
- [52:03 Minting NFTs on Solana](#5203-minting-nfts-on-solana)
	- [Minting NFTs](#minting-nfts)
- [53:22 Using Metaplex SDK for NFTs](#5322-using-metaplex-sdk-for-nfts)
	- [Setting Up Metaplex Instance](#setting-up-metaplex-instance)
- [54:20 Uploading Metadata with Metaplex SDK](#5420-uploading-metadata-with-metaplex-sdk)
	- [Uploading Metadata](#uploading-metadata)
- [54:56 Creating NFTs on the Solana Blockchain](#5456-creating-nfts-on-the-solana-blockchain)
	- [Setting Up NFT Metadata](#setting-up-nft-metadata)
	- [Viewing Uploaded Object on RWeave](#viewing-uploaded-object-on-rweave)
	- [Transaction Details on Blockchain Explorer](#transaction-details-on-blockchain-explorer)
- [59:35 Key Takeaways and Account Structure](#5935-key-takeaways-and-account-structure)
	- [Key Takeaways](#key-takeaways)
	- [Account Structure and Data Structures](#account-structure-and-data-structures)
- [01:00:30 Associating Tokens and Metadata](#010030-associating-tokens-and-metadata)
	- [Associating Token Accounts](#associating-token-accounts)
	- [Metadata Accounts](#metadata-accounts)
- [01:01:58 Challenge and Conclusion](#010158-challenge-and-conclusion)
	- [Challenge - Create an NFT Collection](#challenge---create-an-nft-collection)
	- [Conclusion](#conclusion)

<!-- /TOC -->


# [00:00](https://youtu.be/0P8JeL3TURU?t=0) Introduction

Section Overview: In this section, Nick from the Solana Foundation devrel team introduces the Solana Workshop and provides an overview of what will be covered.

## Workshop Introduction

- Nick from the Solana Foundation devrel team welcomes viewers to the Solana Workshop.
- The workshop will cover the basics of the Solana blockchain, including how it works and how to develop on Solana.
- Topics include the Solana programming model, interacting with the blockchain using JavaScript and TypeScript, and common actions in Solana development.

# [00:26](https://youtu.be/0P8JeL3TURU?t=26) Overview of Solana Network

Section Overview: This section provides a high-level overview of the Solana Network, including its technical advantages and how it works.

## Technical Advantages of Solana

- Fast confirmation times compared to other blockchains (around 400 milliseconds).
- Low transaction fees (about 5,000 Lamports per transaction signature).
- Valid consensus maintained by over 25,000 voting validators globally distributed.

## How Solana Network Works

- Validator leader receives transactions throughout the entire blockchain.
- Leader packs these transactions into blocks that are propagated through the network using a code called "turbine."
- Transactions can be executed in parallel due to stateless nature of transactions on Solana.
- Proof of History is a key innovation that enables fast execution on Solana.

# [03:14](https://youtu.be/0P8JeL3TURU?t=194) General Programming Model on Solana Blockchain

Section Overview: This section explains the general programming model on the Solana blockchain, focusing on accounts.

## Accounts on Solana Blockchain

- Everything in Solana is an account.
- Accounts are unique 256-bit addresses that hold balances of SOL (native token) and can store arbitrary data.
- Data storage is paid for through rent.
- Anyone can credit SOL to an account and read data from it, but only owners can debit SOL or modify the underlying data.

# [04:29](https://youtu.be/0P8JeL3TURU?t=269) Conclusion

Section Overview: This section concludes the workshop introduction and provides a summary of key takeaways.

## Key Takeaways

- Solana offers fast confirmation times, low transaction fees, parallel execution of transactions, and is ideal for high-performance applications.
- The Solana programming model revolves around accounts, which are unique addresses that hold balances and store data.
- Ownership verification ensures security over data on Solana.
# [05:02](https://youtu.be/0P8JeL3TURU?t=302) Understanding Solana Accounts

Section Overview: This section provides an overview of Solana accounts and their structure.

## Solana Account Structure

- A Solana account consists of:
  - A value for the native Soul token, where one Soul is equivalent to about a billion Lamports.
  - The number of Lamports that the account has ownership over.
  - The actual data stored within the account as raw bytes.
  - An executable Boolean flag that indicates if the account is a program or not.
  - An owner value, which determines who can update the data in the account.

## Programs on Solana

- Programs on Solana are similar to smart contracts on other blockchains.
- They are pieces of code deployed to the blockchain and execute instructions.
- Programs have an executable flag set to true and store eBPF bytecode as their data.
- Programs are typically written in Rust, but can also be written in C, C++, Python, or JavaScript (transpiled into Rust).

## Key Points about Programs

- Every program on Solana is stateless and can only read/write data to other accounts.
- Programs cannot write data to their own accounts, enabling parallel execution for speed improvements.
- Only the owner of an account can update it, so a program can be made the owner of any other account it has permission for.
- Instructions are used by programs to interact with each other through cross-program invocation (CPI).
- Instructions can be built using front-end languages like JavaScript or TypeScript and sent for execution.

# [08:44](https://youtu.be/0P8JeL3TURU?t=524) Solana Program Instructions and Transactions

Section Overview: This section explains how instructions and transactions work in Solana.

## Structure of Instructions

- An instruction consists of:
  - The program ID executing the instruction
  - An array of keys representing the accounts involved in the instruction
  - Data in the form of raw bytes sent to the program

## Parallel Execution and Transactions

- Solana's performant runtime requires all addresses/accounts touched within an instruction to be provided.
- Instructions can be bundled together into a transaction, which is sent to validators for processing.
- A transaction includes instructions, a recent block hash for deduplication, and the fee payer address.

## Key Points about Instructions and Transactions

- Instructions specify the program ID, accounts involved, and data for execution.
- Transactions bundle multiple instructions together for processing on the Solana network.
- Recent block hash ensures transaction uniqueness and provides security features.
- Fee payer address determines who pays for the transaction.

Note: The transcript was already in English.
# [10:35](https://youtu.be/0P8JeL3TURU?t=635) Understanding Transactions and Signatures

Section Overview: In this section, the speaker explains the role of transactions and signatures in the Solana blockchain.

## The Role of Public Keys in Transactions

- Transactions require a public key to sign and verify them.
- Public keys are used for cryptographic verification and signature verification on the blockchain.
- All signatures are included in transactions as raw bytes.

## Key Takeaways on Transactions and Instructions

- Programs invoke instructions in transactions.
- Instructions are sent via transactions.
- Transactions must be atomic, meaning they either succeed or fail entirely.
- All transactions must be signed.

# [11:13](https://youtu.be/0P8JeL3TURU?t=673) Life Cycle of a Transaction

Section Overview: This section describes the life cycle of a transaction on the Solana blockchain.

## Client Perspective

- A decentralized application (DApp) client builds instructions for users' transactions.
- The client constructs instructions that are included in a transaction.

## Transaction Flow

1. The transaction is sent to RPC clients.
2. RPC clients forward the transaction to voting validators.
3. Voting validators use the Solana runtime to execute each instruction within the transaction.
4. Each instruction calls a specific program to execute its code (e.g., incrementing a counter).

# [12:12](https://youtu.be/0P8JeL3TURU?t=732) Using and Building Solana Transactions

Section Overview: This section introduces how to use and build Solana transactions through example code.

## Example Code Repository Setup

- Connect to the Solana devnet using the Solana CLI.
- Have a local key pair file with an associated address for executing transactions on devnet.

## Paying for Transaction Fees

- To execute transactions on devnet, ensure there is enough balance to pay for fees.
- Request an airdrop if the balance is low (< 1 SOL).

## Script 1: Simple Transaction

- The script demonstrates creating a simple transaction using TypeScript or JavaScript.
- Import necessary functions and values from Solana web3.js and local helper functions.
- Log the payer address key pair to the console.
- Get the balance of the payer address.
- If the balance is low, request an airdrop.
- Generate a new random key pair for demonstration purposes.
- Build the first instruction for creating an account on-chain using the payer address and new key pair.

# [13:46](https://youtu.be/0P8JeL3TURU?t=826) Understanding Rent in Transactions

Section Overview: This section explains rent in transactions and its role in allocating space on-chain.

- Rent is paid to allocate space on-chain for an address to exist.
- The Solana devnet blockchain requires paying rent when creating accounts on-chain.
# [16:06](https://youtu.be/0P8JeL3TURU?t=966) Paying for Space on the Blockchain

Section Overview: In this section, the concept of paying for space on the blockchain is discussed. The Solana web3js library's helper function called "get minimum balance for rent exemptions" is introduced.

## Allocating Space on the Blockchain

- When allocating space on the blockchain, a fee needs to be paid upfront.
- This fee encourages validators to maintain the allocated space and data on the blockchain.
- The Solana web3js library provides a helper function called "get minimum balance for rent exemptions" to determine the minimum amount of rent that can be paid for an account.
- For a simple account that only stores token balances, no additional space allocation is needed.

# [16:25](https://youtu.be/0P8JeL3TURU?t=985) Creating an Account

Section Overview: This section covers creating an account using the system program in Solana. The required data for creating an account is explained.

## Building Instructions for Account Creation

- The system program in Solana is responsible for owning generic normal accounts that hold balances.
- To create an account, necessary data such as payer address, new address to allocate on-chain (using a randomly generated key pair), number of Lan ports to store (ensuring it meets the minimum balance requirement), and owner program (system program) are provided.
- All these details are combined into a variable called "create account instruction IX."

# [17:13](https://youtu.be/0P8JeL3TURU?t=1033) Constructing a Transaction

Section Overview: This section focuses on constructing a transaction in Solana. The process involves obtaining a recent block hash and building a version transaction with instructions.

## Obtaining Block Hash and Building Transaction

- Every transaction in Solana requires a recent block hash.
- The connection with the blockchain is used to retrieve this block hash.
- Destructuring is used to extract the block hash value.
- A version transaction, a newer standard in Solana, is built with the instructions provided.
- The transaction includes the recent block hash, payer information, and signatures.

# [19:13](https://youtu.be/0P8JeL3TURU?t=1153) Signing and Sending the Transaction

Section Overview: This section covers signing and sending the constructed transaction in Solana. The importance of signatures and required signers are explained.

## Signing and Sending Transaction

- Every transaction in Solana requires at least one signature.
- If an account is being created on-chain, the key pair associated with that address must also sign the transaction.
- In this case, the payer's key pair is used for signing.
- The signed transaction is then sent to the blockchain using the connection.
- Logging is done for simplicity and demonstration purposes.

# [20:05](https://youtu.be/0P8JeL3TURU?t=1205) Summary of Script Execution

Section Overview: This section provides a summary of the executed script in Solana. It includes details such as payer address, Lan Port balance, total balance in Soul tokens, generated random address, and lanport cost for space allocation.

## Script Execution Summary

- Payer address: Nic b1d...
- Lan Port balance: 240+
- Total balance in Soul tokens: 240+
- Generated random address using web3js
- Lanport cost for space allocation (minimum of zero bytes)
- Logging of transactions structure including signatures, account keys involved, payer address, allocated address (system program), and recent block hash value.
# [21:20](https://youtu.be/0P8JeL3TURU?t=1280) Understanding the Solana Explorer

Section Overview: In this section, the speaker discusses how to use the Solana Explorer and understand the information displayed on it.

## Opening Solana Explorer and Basic Information
- The speaker opens the Solana Explorer and explains that they are on cluster devnet.
- Common information displayed on a blockchain explorer includes timestamp, signature value, recent block hash, total transaction fee, and accounts involved in the transaction.

## Transaction Details
- The speaker points out the accounts included in the transaction (Nick value, AT3, system program).
- Post balances of accounts are shown.
- Two signatures were required for this transaction.
- The instruction executed was "create account" from the system program.

# [22:36](https://youtu.be/0P8JeL3TURU?t=1356) Building Complex Transactions

Section Overview: This section focuses on building more complex transactions using Solana.

## Setting Up for Complex Transaction
- Importing necessary modules and defining variables for payer address and test wallet address.
- Helper functions are used to generate key pairs for demonstration purposes.

## Allocating Space on Chain
- Allocating space on chain for a new random address generated.
- Setting space to zero (minimum balance for rent exemption).
- Test wallet address is set as the address to allocate on chain with an additional 2 million lamports stored inside.

## Executing Transfer Instructions
- Transferring funds from payer account to test wallet account.
- Another transfer instruction is executed to send funds to another random address (demonstration purposes).

## Building Multiple Instructions in a Transaction
- Loading a static public key value (Nic address) for demonstration purposes.
- Building transfer instructions using different addresses.
  
## Atomic Execution of Instructions
- All instructions within a transaction are executed atomically (in order).
- If any instruction fails, the entire transaction fails.
  
## Building and Sending the Transaction
- Building the transaction by signing it with payer and test wallet addresses.
- Sending the transaction to the blockchain.
- Logging out the Explorer URL for demonstration purposes.

# [26:03](https://youtu.be/0P8JeL3TURU?t=1563) Summary of Complex Transaction

Section Overview: The speaker summarizes the complex transaction that was built and executed successfully.

## Summary of Steps
- The same payer address is used.
- A new random test wallet address is generated and allocated on chain with additional funds.
- Funds are transferred from payer account to test wallet account.
- Another transfer is made to a static wallet address (Nic address) for demonstration purposes.

Note: The transcript provided does not include any further sections or timestamps.
# [26:45](https://youtu.be/0P8JeL3TURU?t=1605) Building Transactions for the Solana Blockchain

Section Overview: This section provides an overview of building transactions for the Solana blockchain.

## Overview of Building Transactions

- Applications build and send transactions to an RPC (Remote Procedure Call).
- The RPC forwards the transactions to the network's voting validators.
- Validators execute the transactions, which invoke programs.
- Programs can update accounts they have authority or ownership over.

# [27:02](https://youtu.be/0P8JeL3TURU?t=1622) Tokens on the Solana Blockchain

Section Overview: This section discusses tokens on the Solana blockchain and their associated programs.

## Three Programs for Tokens

- Tokens on Solana consist of three programs: token program, associated token program (ATA), and metadata program.
- Token program and ATA are deployed by Solana Labs, while metadata program is commonly deployed by Metaplex Foundation.
- These programs are used by most users on the Solana blockchain.

# [27:39](https://youtu.be/0P8JeL3TURU?t=1659) Creating a Token on Solana

Section Overview: This section explains how to create a token on the Solana blockchain using transactions.

## Minting Tokens with Token Program

- To create a token, use the token program to create a mint. A mint is an account that controls a certain amount of token balance.
- Similar to a government's treasury department creating national currency, the token program controls a mint that can mint new tokens.

## Ownership via Associated Token Accounts (ATA)

- After minting tokens, they need to be owned by a user's wallet in order to interact with the blockchain.
- Ownership is established through associated token accounts (ATA), where wallets own and have authority over ATAs storing SPL tokens.

## Metadata for Tokens

- Tokens can have metadata associated with them using programs like Metaplex's metadata program.
- Metadata includes information like token name, image, symbol, etc., stored in a metadata account owned by the metadata program.

# [29:14](https://youtu.be/0P8JeL3TURU?t=1754) Creating an SPL Token

Section Overview: This section demonstrates the process of creating an SPL (Solana Program Library) token using a Solana transaction.

## Steps to Create an SPL Token

- Use a Solana transaction to create instructions for various actions on-chain.
- Instructions include creating a new account, initializing it as a mint, creating an associated token account, and minting tokens into the associated token account.
- All these actions can be done with a single transaction on the Solana blockchain, showcasing its composability.

# [30:27](https://youtu.be/0P8JeL3TURU?t=1827) Demonstration: Creating an SPL Token with Metadata

Section Overview: This section provides a demonstration of creating an SPL token with metadata on the Solana blockchain using TypeScript code.

## Code Setup and Imports

- Import necessary variables, values, functions from local repository and external libraries like web3js and Solana SPL token library.
- Log payer address and test wallet for reference.
- Generate a new key pair for use with the SPL token.

## Configuring Token Metadata

- Define configuration information for the desired metadata of the token.
- Information includes name, symbol (e.g., "gold"), URI (address pointing to additional metadata), and decimals value.

Note: The remaining part of the transcript is not included in this summary.
# [32:12](https://youtu.be/0P8JeL3TURU?t=1932) Building Instructions for Creating an Account

Section Overview: In this section, we will discuss how to build instructions for creating an account on the Solana blockchain.

## Creating an Account

- We use the `system program.createAccount` instruction to create an account.
- The size of the account is determined by a constant variable called `mintSize`, which is obtained from the Solana SPL token package.
- The minimum balance required for rent exemption is calculated based on the size of the account.
- The mint account is owned by the token program, indicated by the authority provided.
- We initialize the mint account as a mint and provide necessary values such as address, decimals, payer, mint authority, and freeze authority.
- The mint authority has permission to mint additional tokens, while freeze authority can prevent additional minting or disable it entirely.

# [34:50](https://youtu.be/0P8JeL3TURU?t=2090) Creating Metadata Account

Section Overview: This section explains how to create a metadata account using a program derived address (PDA).

## Program Derived Address (PDA)

- A PDA is a special type of address that allows a program to sign transactions for specific use cases.
- We derive a metadata account using a PDA owned by the token metadata program (`metaqbxx`).
- The PDA value is computed using a combination of metadata values and the mint key pair generated earlier.
- The derived address is logged to the console for demonstration purposes.
- We create a metadata V3 instruction with all required values and addresses including metadata account, mint, payer, update authority, and data fields such as name, symbol, and seller fee basis points.

# [36:54](https://youtu.be/0P8JeL3TURU?t=2214) Bundling Instructions into Transaction

Section Overview: This section covers bundling multiple instructions into a single transaction.

## Bundling Instructions

- We use a helper function called `build` to bundle the previously created instructions into a single transaction.
- The function includes the recent block hash and allows signing with applicable addresses such as payer and mint key pair.
- This ensures that the fees are paid by the payer and the allocated account is properly initialized on-chain.

Note: The transcript provided does not contain any timestamps beyond 0:37:13, so this is where the summary ends.
# [37:46](https://youtu.be/0P8JeL3TURU?t=2266) Overview of Completed Script and Logged Addresses

Section Overview: In this section, the speaker discusses the completion of a script and the logged addresses associated with it.

## Completed Script and Logged Addresses

- The script has successfully completed.
- Various addresses have been logged, including:
  - Nic address of the payer
  - Test wallet address (same as before)
  - Randomly generated mint address
  - Derived metadata PDA

# [38:03](https://youtu.be/0P8JeL3TURU?t=2283) Viewing Transaction on Solana Explorer

Section Overview: This section focuses on viewing a transaction on the Solana Explorer and exploring additional accounts included in the transaction.

## Viewing Transaction on Solana Explorer

- Open the transaction on the Solana Explorer.
- Standard information about the transaction is displayed.
- Additional accounts included in this transaction are:
  - Payer account
  - Additional signer (in this case, mint account)
  - System Program token program account
  - Token metadata account
- Instructions and data passed along in the transaction can be examined.

# [38:23](https://youtu.be/0P8JeL3TURU?t=2303) Examining Instruction Data and Logs

Section Overview: Here, we explore instruction data and logs associated with the executed program instructions.

## Examining Instruction Data and Logs

- Token metadata instruction includes accounts passed in and raw hexadecimal encoded bytes of instruction data.
- All data is logged into the console or explorer since it is stored on-chain.
- Program instruction logs can be viewed to see their execution.

# [39:17](https://youtu.be/0P8JeL3TURU?t=2357) Minting Tokens to Associated Token Account

Section Overview: This section covers minting tokens to an associated token account.

## Minting Tokens to Associated Token Account

- The first three steps of instructions have been completed, but tokens have not been minted to the associated token account yet.
- Minting tokens can be done in a single transaction or multiple transactions.
- In this demonstration, it is set up as two different transactions to allow for multiple minting.
- Open script number four, "mint tokens."
- Load necessary imports and define payer address.
- Get the token mint address (loaded from a local JSON file).
- Create or get the associated token account (ATA) owned by the payer and linked to the mint.
- Log the public key value of the token account.

# [40:27](https://youtu.be/0P8JeL3TURU?t=2427) Understanding Associated Token Account Ownership

Section Overview: This section explains the concept of ownership of associated token accounts.

## Understanding Associated Token Account Ownership

- The associated token account (ATA) has ownership over the tokens that are minted.
- The ATA is owned by the user, while it references back to the tokens.
- The payer is set as both owner and payer in this case, but they can be different values depending on use case.
- Developers can choose to pay for allocating space on-chain or have users pay for it.

# [42:18](https://youtu.be/0P8JeL3TURU?t=2538) Minting Tokens with Decimals

Section Overview: Here, we explore how decimals play a role in minting tokens under SPL token program.

## Minting Tokens with Decimals

- Decimals are important when minting tokens under SPL token program.
- If a token mint has two decimal places, requesting to mint 1,000 tokens should consider including enough tokens with two decimal places.
# [43:14](https://youtu.be/0P8JeL3TURU?t=2594) Minting Tokens to Associated Token Account

Section Overview: In this section, the speaker discusses using a helper function provided by the SPL Token Program SDK to mint tokens to an associated token account. The necessary variables for the transaction are passed in, including the payer, mint of the tokens, ATA (Associated Token Account), and the number of tokens to be minted.

## Minting Tokens
- A helper function from the SPL Token Program SDK is used to mint tokens to an associated token account.
- The necessary variables for the transaction are passed in: payer, mint of the tokens, ATA (Associated Token Account), and number of tokens to be minted.
- The signature is logged out to an Explorer URL on the console.

# [43:32](https://youtu.be/0P8JeL3TURU?t=2612) Minting Tokens and Checking Balances

Section Overview: This section demonstrates minting tokens to an associated token account and checking balances using an Explorer URL. It also mentions that creating a new associated token account takes longer than deriving it.

## Minting Tokens and Checking Balances
- Tokens are minted to an associated token account.
- Creating a new associated token account takes some time as it needs to be created on-chain.
- Subsequent runs of the script will be faster as only derivation is required.
- An Explorer URL is opened where token balances can be seen.
- 10 tokens have been successfully minted to the specified token address.

# [44:10](https://youtu.be/0P8JeL3TURU?t=2650) Minting Additional Tokens

Section Overview: This section explains how additional tokens can be minted by running the script again without changing any values. It also shows that obtaining the PDA address is faster when there's no need for creation.

## Minting Additional Tokens
- Running the script again without changing any values allows for minting additional tokens.
- Obtaining the PDA (Program Derived Address) address is faster as it doesn't need to be created again.
- An Explorer URL is opened where the updated token balances can be seen.
- The current supply of tokens is now 20.

# [44:51](https://youtu.be/0P8JeL3TURU?t=2691) Updating Token Metadata

Section Overview: This section discusses the ability to update token metadata as long as the token and its metadata are not frozen. It demonstrates updating the metadata by changing the name, symbol, and URI of a token.

## Updating Token Metadata
- Token metadata can be updated if the token and its metadata are not frozen.
- A script is provided to demonstrate updating token metadata.
- The script loads the token mint and payer address, then creates new token metadata information.
- The name, symbol, and URI values are changed in this example.
- The PDA for the metadata account is derived, and its address is logged out.
- An update instruction for metadata V2 is created with all necessary information using an instruction builder helper function.
- A transaction is built with the payer signing it since they are also the authority for this demonstration.
- After running the script successfully, a transaction Explorer URL is provided to view details of the executed instructions.
- Opening the updated token mint on an Explorer shows that the metadata has been successfully updated.

# [45:43](https://youtu.be/0P8JeL3TURU?t=2743) Conclusion

Section Overview: This section concludes that all four topics discussed in previous sections have been successfully completed.

## Summary
- All four topics covered in previous sections have been successfully completed.
# [49:03](https://youtu.be/0P8JeL3TURU?t=2943) Overview of SPL Tokens on Solana

Section Overview: In this section, the speaker discusses the key takeaways about SPL tokens on the Solana blockchain. They highlight that there is no need to deploy a new program to create new tokens on Solana. New tokens can be created using a single transaction and RPC call.

## Creating New SPL Tokens

- No need to deploy a new program to create new tokens on Solana.
- New tokens can be created using only one single transaction and RPC call.
- Various accounts are used to describe the tokens, such as mint, associate token account, and metadata account.
- These accounts interact in a composable manner, which is one of the strong points of Solana.

# [50:20](https://youtu.be/0P8JeL3TURU?t=3020) NFTs as SPL Tokens

Section Overview: This section explains that NFTs (Non-Fungible Tokens) are actually SPL tokens on the Solana blockchain. The speaker describes some unique properties of NFTs and introduces the concepts of master edition and collection.

## Properties of NFTs

- Every NFT on Solana is an SPL token with specific properties.
- NFTs have zero decimal places for each mint, indicating non-fungibility.
- Each NFT has a supply of exactly one.
- NFTs can have highly customizable metadata, including multiple images and attributes.
- Master edition and collection are additional pieces of information associated with NFTs.

## Master Edition and Collection

- Master Edition is an account used to store specific metadata information related to an NFT.
- Collection is an NFT grouping that has a relationship with all the individual NFTs within it.

# [52:03](https://youtu.be/0P8JeL3TURU?t=3123) Minting NFTs on Solana

Section Overview: In this section, the speaker demonstrates the process of minting NFTs on the Solana blockchain using the Metaplex SDK. They explain how to create a new Metaplex instance and upload metadata to IPFS.

## Minting NFTs

- Open script number six, "create nfts," which uses the Metaplex SDK.
- Obtain necessary keys and import dependencies.
- Create metadata for the NFT, including name, symbol, description, and an image stored on IPFS.
- Use the Metaplex SDK to upload the metadata as JSON to IPFS.
- Retrieve and log the URI of the uploaded metadata.

# [53:22](https://youtu.be/0P8JeL3TURU?t=3202) Using Metaplex SDK for NFTs

Section Overview: The speaker explains that they will use the Metaplex SDK to handle actions related to minting NFTs. They provide an overview of how to set up a new Metaplex instance with connection and key pair information.

## Setting Up Metaplex Instance

- Use the open-source Metaplex SDK provided by the Metaplex Foundation.
- Create a new instance of Metaplex with connection and key pair information.
- Additional configuration values may be required for specific networks (e.g., devnet).

# [54:20](https://youtu.be/0P8JeL3TURU?t=3260) Uploading Metadata with Metaplex SDK

Section Overview: The speaker demonstrates how to use the Metaplex SDK to upload metadata as a JavaScript object to IPFS. They also mention logging out the URI for verification purposes.

## Uploading Metadata

- Use the `upload` function from the Metaplex SDK to upload a JavaScript object as JSON metadata to IPFS.
- Log out the URI of the uploaded metadata for verification purposes.

Note: The summary has been created based on English language transcript.
# [54:56](https://youtu.be/0P8JeL3TURU?t=3296) Creating NFTs on the Solana Blockchain

Section Overview: In this section, the speaker discusses the process of creating NFTs (Non-Fungible Tokens) on the Solana blockchain using Metaplex SDK.

## Setting Up NFT Metadata

- The speaker explains that to create an NFT, they need to provide image, metadata URL, name, symbol, and seller fee basis points.
- Seller fee basis points represent the royalties requested by the creator. In this case, a 5% royalty is requested.
- The NFT is set as mutable to allow for future updates to its metadata.
- The script logs out the NFT object returned from Metaplex SDK and also logs out the signature for viewing the transaction on Explorer.

## Viewing Uploaded Object on RWeave

- The speaker mentions that they are using RWeave to upload and store data for their NFT.
- They open the RWeave address and show the uploaded object containing all the addresses and data set during NFT creation.

## Transaction Details on Blockchain Explorer

- The speaker opens the transaction on a blockchain explorer.
- They highlight that it is a complex transaction involving multiple accounts.
- The metadata associated with the created NFT is displayed, including name, symbol, image, creator address, etc.
- Interested individuals can explore further by examining instructions executed or referring to Metaplex documentation.

# [59:35](https://youtu.be/0P8JeL3TURU?t=3575) Key Takeaways and Account Structure

Section Overview: This section provides key takeaways from creating NFTs on Solana and discusses account structure in more detail.

## Key Takeaways

- SPL tokens underlie NFTs on Solana with unique properties such as zero decimal places and a supply of exactly one.
- Customizable metadata allows for extensive information inclusion within an NFT.
- Interested individuals can refer to Metaplex documentation for more information on NFT editions.

## Account Structure and Data Structures

- The speaker revisits the account structure used in SPL tokens, specifically the mint account.
- They highlight the decimals calculation and other relevant data structures.

Note: The transcript does not provide timestamps beyond 0:59:52.
# [01:00:30](https://youtu.be/0P8JeL3TURU?t=3630) Associating Tokens and Metadata

Section Overview: In this section, the speaker explains the process of associating tokens with token accounts and metadata accounts.

## Associating Token Accounts
- Associated token accounts are derived from a program-derived address (PDA).
- The PDA is created using the seeds of the user's wallet, the token program, and the mint.
- These associated token accounts store data related to a user's balance.

## Metadata Accounts
- Metadata accounts are used to store additional information about SPL tokens or NFTs.
- A PDA is derived using the static value of the metadata program and the mint address.
- The metadata account is owned by the metadata program.
- Within this account, specific data such as title, symbol, URI value (stored off-chain), and list of creators can be stored.

# [01:01:58](https://youtu.be/0P8JeL3TURU?t=3718) Challenge and Conclusion

Section Overview: The speaker concludes day one of the workshop by presenting a challenge to create an NFT collection and provides some closing remarks.

## Challenge - Create an NFT Collection
- Participants are challenged to create their own NFT collection for a game called "Seven Seas" with pirate ships.
- They should use different images for each ship and explore IPFS for storage.
- Additional three SPL tokens should be created for gold, rum, and cannons.

## Conclusion
- The speaker thanks viewers for watching and hopes they have learned from the workshop.

[Generated with Video Highlight](https://videohighlight.com/video/summary/0P8JeL3TURU)
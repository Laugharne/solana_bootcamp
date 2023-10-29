# [00:00](https://youtu.be/EKvJ4ShVzNA?t=0) Introduction

<!-- TOC -->

- [00:00 Introduction](#0000-introduction)
- [15:10 Leather Casters](#1510-leather-casters)
	- [Leather Casters Features](#leather-casters-features)
- [16:06 Dominari](#1606-dominari)
	- [Dominari Features](#dominari-features)
- [16:53 These Quest](#1653-these-quest)
	- [These Quest Features](#these-quest-features)
- [17:30 Conclusion](#1730-conclusion)
	- [Tiny Adventure](#tiny-adventure)
- [18:16 Solana Program Tutorial](#1816-solana-program-tutorial)
	- [Getting Started with the Tutorial](#getting-started-with-the-tutorial)
	- [Setting Up Development Environment](#setting-up-development-environment)
	- [Building and Deploying the Program](#building-and-deploying-the-program)
	- [Exploring Deployed Program Details](#exploring-deployed-program-details)
	- [Running and Interacting with Deployed Program](#running-and-interacting-with-deployed-program)
	- [JSON Representation of Program](#json-representation-of-program)
- [23:43 Exploring Program Interactions](#2343-exploring-program-interactions)
	- [Viewing Program Interactions on-chain](#viewing-program-interactions-on-chain)
- [24:45 Understanding the Program Structure](#2445-understanding-the-program-structure)
	- [Initializing the Account](#initializing-the-account)
	- [Context and Accounts](#context-and-accounts)
	- [Game Data Account](#game-data-account)
	- [Multiplayer Game Development](#multiplayer-game-development)
	- [Paying for Accounts and Space](#paying-for-accounts-and-space)
	- [Move Left and Move Right Functions](#move-left-and-move-right-functions)
- [29:33 Client-Side Implementation](#2933-client-side-implementation)
	- [Derivation of Program Derived Address PDA](#derivation-of-program-derived-address-pda)
	- [Fetching Game Data Account](#fetching-game-data-account)
- [[30:54](https://youtu.be/EKvJ4ShVzNA?t=1854) Creating a New Game Data Account and Signers](#t1854s-creating-a-new-game-data-account-and-signers)
- [[31:13](https://youtu.be/EKvJ4ShVzNA?t=1873) Transaction Stages and Confirmation](#t1873s-transaction-stages-and-confirmation)
- [[31:35](https://youtu.be/EKvJ4ShVzNA?t=1895) Creating Instructions and Fetching Game Data](#t1895s-creating-instructions-and-fetching-game-data)
- [[32:37](https://youtu.be/EKvJ4ShVzNA?t=1957) Changing Text and Building the Program](#t1957s-changing-text-and-building-the-program)
- [[33:28](https://youtu.be/EKvJ4ShVzNA?t=2008) Questions and Solana as a Database](#t2008s-questions-and-solana-as-a-database)
- [[33:52](https://youtu.be/EKvJ4ShVzNA?t=2032) Account Representation and Transaction Validity](#t2032s-account-representation-and-transaction-validity)
- [[34:35](https://youtu.be/EKvJ4ShVzNA?t=2075) Multiple Instructions and Transaction Validity](#t2075s-multiple-instructions-and-transaction-validity)
- [[35:17](https://youtu.be/EKvJ4ShVzNA?t=2117) Signers and Transaction Flow](#t2117s-signers-and-transaction-flow)
- [[36:07](https://youtu.be/EKvJ4ShVzNA?t=2167) Interacting with Programs in Unity Client](#t2167s-interacting-with-programs-in-unity-client)
- [37:01 Understanding the RPC Node and WebSocket Connection](#3701-understanding-the-rpc-node-and-websocket-connection)
	- [Moving to the Right and Account Updates](#moving-to-the-right-and-account-updates)
- [37:24 Reading and Writing Data with RPC Node](#3724-reading-and-writing-data-with-rpc-node)
	- [Reading Data](#reading-data)
	- [Writing Data](#writing-data)
- [38:03 State Changes and Real-Time Updates](#3803-state-changes-and-real-time-updates)
	- [Voting on State Changes](#voting-on-state-changes)
	- [Real-Time Updates in Multiplayer Games](#real-time-updates-in-multiplayer-games)
- [38:44 Implementing Position in a Multiplayer Game](#3844-implementing-position-in-a-multiplayer-game)
	- [Adding X and Y Position](#adding-x-and-y-position)
- [39:56 Introduction to Tiny Adventure 2](#3956-introduction-to-tiny-adventure-2)
	- [Game Overview](#game-overview)
- [40:27 Saving SOL in a PDA with Password Protection](#4027-saving-sol-in-a-pda-with-password-protection)
	- [Collecting Chests](#collecting-chests)
- [41:34 Opening Solana Playground for Tiny Adventure 2 Tutorial](#4134-opening-solana-playground-for-tiny-adventure-2-tutorial)
	- [Accessing Solana Playground](#accessing-solana-playground)
- [42:25 Deploying Tiny Adventure 2](#4225-deploying-tiny-adventure-2)
	- [Deploying the Game](#deploying-the-game)
- [43:14 Initializing and Transferring Soil](#4314-initializing-and-transferring-soil)
	- [Initializing Level One](#initializing-level-one)
	- [Transferring Soil into a PDA](#transferring-soil-into-a-pda)
	- [Example Run](#example-run)
	- [Transferring Soil Back](#transferring-soil-back)
	- [Account Details](#account-details)
- [48:48 Initializing Level One](#4848-initializing-level-one)
	- [Initialization Process](#initialization-process)
	- [Additional Features](#additional-features)
- [49:29 Adding a Password and Error Handling](#4929-adding-a-password-and-error-handling)
	- [Adding a Password](#adding-a-password)
	- [Error Handling](#error-handling)
- [50:32 Displaying Errors in the Client Application](#5032-displaying-errors-in-the-client-application)
	- [Checking for Custom Errors](#checking-for-custom-errors)
	- [Exporting IDL File](#exporting-idl-file)
- [53:26 Overview of Tiny Adventure 2 and Saving Soul](#5326-overview-of-tiny-adventure-2-and-saving-soul)
	- [Tiny Adventure 2 Flow](#tiny-adventure-2-flow)
	- [Saving Soul in a PDA](#saving-soul-in-a-pda)
- [54:04 Interacting with SPL Tokens](#5404-interacting-with-spl-tokens)
	- [Understanding SPL Tokens](#understanding-spl-tokens)
	- [Associated Token Accounts](#associated-token-accounts)
	- [Creating Token Accounts](#creating-token-accounts)
- [[56:26](https://youtu.be/EKvJ4ShVzNA?t=3386) Signing the PDA with the PDA for Transfer in the Program](#t3386s-signing-the-pda-with-the-pda-for-transfer-in-the-program)
- [[56:46](https://youtu.be/EKvJ4ShVzNA?t=3406) Setting Up Local Development Environment](#t3406s-setting-up-local-development-environment)
- [[57:09](https://youtu.be/EKvJ4ShVzNA?t=3429) Checking Out Repository and Building Anchor Program Locally](#t3429s-checking-out-repository-and-building-anchor-program-locally)
- [[59:09](https://youtu.be/EKvJ4ShVzNA?t=3549) Deploying the Anchor Program](#t3549s-deploying-the-anchor-program)
- [[01:01:09](https://youtu.be/EKvJ4ShVzNA?t=3669) Introduction to Client and Recommended Extensions](#t3669s-introduction-to-client-and-recommended-extensions)
- [01:03:19 Local Setup and Tools](#010319-local-setup-and-tools)
	- [Setting Up Tools](#setting-up-tools)
	- [Configuring Analyzer and Formatting](#configuring-analyzer-and-formatting)
	- [Running the Program Locally](#running-the-program-locally)
	- [Running the JavaScript Client](#running-the-javascript-client)
	- [Additional Resources](#additional-resources)
- [01:09:55 Next.js Apps and API Integration](#010955-nextjs-apps-and-api-integration)
	- [Integrating with APIs in Next.js](#integrating-with-apis-in-nextjs)
- [01:10:20 Burner Key Pair and Environment Setup](#011020-burner-key-pair-and-environment-setup)
	- [Burner Key Pair and Environment File](#burner-key-pair-and-environment-file)
- [01:10:39 Interacting with Games via APIs](#011039-interacting-with-games-via-apis)
	- [Interacting with Games without Login](#interacting-with-games-without-login)
- [01:10:58 Transaction Fees and API Functionality](#011058-transaction-fees-and-api-functionality)
	- [Transaction Fees and API Functionality](#transaction-fees-and-api-functionality)
- [01:11:24 Backend Key Pair for Signing Transactions](#011124-backend-key-pair-for-signing-transactions)
	- [Backend Key Pair for Signing Transactions](#backend-key-pair-for-signing-transactions)
- [01:11:57 Unity Game Engine Introduction](#011157-unity-game-engine-introduction)
	- [Introduction to Unity Game Engine](#introduction-to-unity-game-engine)
- [01:12:38 Using Unity with Solana Game Starter Kits](#011238-using-unity-with-solana-game-starter-kits)
	- [Using Unity with Solana Game Starter Kits](#using-unity-with-solana-game-starter-kits)
- [01:13:24 Blockchain Games and Wallet Support](#011324-blockchain-games-and-wallet-support)
	- [Blockchain Games and Wallet Support](#blockchain-games-and-wallet-support)
- [01:14:30 Solnet Implementation and Code Generation Tool](#011430-solnet-implementation-and-code-generation-tool)
	- [Solnet Implementation and Code Generation Tool](#solnet-implementation-and-code-generation-tool)
- [01:15:23 Using the Code Generation Tool](#011523-using-the-code-generation-tool)
	- [Using the Code Generation Tool](#using-the-code-generation-tool)
- [01:16:25 Unity Setup for Tiny Adventure Game](#011625-unity-setup-for-tiny-adventure-game)
	- [Unity Setup for Tiny Adventure Game](#unity-setup-for-tiny-adventure-game)
- [01:17:22 Understanding the Game Data Account](#011722-understanding-the-game-data-account)
	- [Game Data Account Details](#game-data-account-details)
- [01:17:49 Simplified Instruction Creation](#011749-simplified-instruction-creation)
	- [Creating Instructions](#creating-instructions)
- [01:18:12 Manual Transaction Creation](#011812-manual-transaction-creation)
	- [Manual Transaction Process](#manual-transaction-process)
- [01:18:30 Unity Implementation Example](#011830-unity-implementation-example)
	- [Unity Implementation Steps](#unity-implementation-steps)
- [01:18:48 Homework and Further Resources](#011848-homework-and-further-resources)
	- [Homework and Resources](#homework-and-resources)
- [01:19:10 Future Topics and Conclusion](#011910-future-topics-and-conclusion)
	- [Future Topics](#future-topics)
	- [Conclusion](#conclusion)

<!-- /TOC -->
- In Chrono Kingdom, players build cities, produce resources, create units, and engage in battles with other cities. [14:27](https://youtu.be/EKvJ4ShVzNA?t=867)
- The game follows a similar concept to Tribal Wars or old browser games. [14:51](https://youtu.be/EKvJ4ShVzNA?t=891)

# [15:10](https://youtu.be/EKvJ4ShVzNA?t=910) Leather Casters

Section Overview: The speaker discusses Leather Casters, the first Solana on-chain game. Players control a mage who can move around on a grid, collect tokens, and use them to perform spells.

## Leather Casters Features

- In Leather Casters, players control a mage who can move around on a grid and collect tokens (water, earth, fire) to perform spells. [15:10](https://youtu.be/EKvJ4ShVzNA?t=910)
- Currently, the focus is on their referral system called Buddy Link. [15:29](https://youtu.be/EKvJ4ShVzNA?t=929)

# [16:06](https://youtu.be/EKvJ4ShVzNA?t=966) Dominari

Section Overview: The speaker introduces Dominari, an on-chain grid strategy game where players build buildings, produce units, and engage in battles against other players.

## Dominari Features

- Dominari is an on-chain grid strategy game where players build buildings, produce units, and engage in battles against other players. [16:06](https://youtu.be/EKvJ4ShVzNA?t=966)
- A new round starts every five seconds for players to move their units and fight. [16:28](https://youtu.be/EKvJ4ShVzNA?t=988)

# [16:53](https://youtu.be/EKvJ4ShVzNA?t=1013) These Quest

Section Overview: The speaker introduces These Quest as an unchained match 3 game from the last hackathon. Players choose avatars with different stats and fight against each other using collected items.

## These Quest Features

- These Quest is an unchained match 3 game where players choose avatars with different stats and fight against each other using collected items. [16:53](https://youtu.be/EKvJ4ShVzNA?t=1013)
- The game features an interesting on-chain matchmaking system. [17:30](https://youtu.be/EKvJ4ShVzNA?t=1050)

# [17:30](https://youtu.be/EKvJ4ShVzNA?t=1050) Conclusion

Section Overview: The speaker concludes the discussion of games and transitions to coding a game called "Tiny Adventure."

## Tiny Adventure

- The speaker introduces "Tiny Adventure" as the game they will be coding. No further details are provided in this section. [17:30](https://youtu.be/EKvJ4ShVzNA?t=1050)
# [18:16](https://youtu.be/EKvJ4ShVzNA?t=1096) Solana Program Tutorial

Section Overview: In this section, the speaker invites viewers to open beta.solpg.io and start the Tiny Adventure tutorial. They explain how to create a new wallet and obtain Solana tokens for deploying a program.

## Getting Started with the Tutorial

- Open beta.solpg.io to access the tutorial.
- Start the Tiny Adventure tutorial.
- Create a new wallet by clicking on the red dot in the bottom left corner.
- Choose whether to save your key phrase or not.
- Perform Solana airdrop 2 times to obtain enough Solana tokens for program deployment.

## Setting Up Development Environment

- Switch the endpoint to devnet for development purposes.
- Use "Solana airdrop 2" command to obtain definite Solana tokens for testing (if needed).
- If unable to get tokens, visit saltfosset.com or use custom RPC from Helios, Triton, or other providers' faucets.

## Building and Deploying the Program

- Type "build" in the bottom console to build the program using Rust code.
- The program is compiled into an .so file that will be deployed.
- Type "deploy" in the console to deploy the program onto the blockchain.
- A unique program ID is generated as an address on the Solana blockchain.
    - This ID can be viewed on explorer.solana.com by switching to devnet.

## Exploring Deployed Program Details

- On explorer.solana.com, paste the program ID obtained earlier.
    - The deployed program details are displayed, including executable data size and deployment cost in Solana tokens.
    - Closing a deployed program returns its associated tokens but renders its address unusable.

## Running and Interacting with Deployed Program

- Run the deployed program using "run" command in console.
    - The game starts with a message and the character's initial position.
    - Each transaction updates the player's position.
- Copy the transaction hash and paste it into explorer.solana.com to view the corresponding transaction details.

## JSON Representation of Program

- Click on "IDL" and "Initialize" to deploy the program's JSON representation onto the blockchain.
- Refreshing the transaction shows real-time interactions with the program.

# [23:43](https://youtu.be/EKvJ4ShVzNA?t=1423) Exploring Program Interactions

Section Overview: The speaker demonstrates how program interactions are displayed on-chain using a JSON representation of the program.

## Viewing Program Interactions on-chain

- After deploying the JSON representation, refresh explorer.solana.com to see updated program interactions.
- The game data account and instructions are visible, showing how they interact with the deployed program.
# [24:45](https://youtu.be/EKvJ4ShVzNA?t=1485) Understanding the Program Structure

Section Overview: In this section, the speaker explains the structure of the Rust program used in the game development process.

## Initializing the Account

- The program starts by initializing the account with context, accounts, and new game data.
- The player's position is set to zero.
- The import for Anchor files is included at the top of the program.

## Context and Accounts

- The initialize function is called with a specific context that consists of various accounts.
- The game data account and signer are passed into the program.
- The system program is required to create a new game data account.

## Game Data Account

- The game data account contains only a single value, which represents the player's position (u8).
- It uses one byte of data and can range from 0 to 255.
- A Program Derived Address (PDA) is used to derive different entries in a table based on the program ID.

## Multiplayer Game Development

- By adding a signer as a reference, each player can have their own level within the game.
- This allows for multiplayer functionality where multiple players can interact with the same program simultaneously.

## Paying for Accounts and Space

- The payer needs to pay for certain accounts in Solana blockchain using rent exemption.
- An account discriminator (8 bytes) is added by Anchor as part of space allocation.

## Move Left and Move Right Functions

- Two functions are implemented: move left and move right.
- If player position reaches three, it means they have completed the game successfully.
- Player position is incremented or decremented accordingly, allowing movement within the game world.

# [29:33](https://youtu.be/EKvJ4ShVzNA?t=1773) Client-Side Implementation

Section Overview: This section focuses on client-side implementation using derived PDA addresses.

## Derivation of Program Derived Address (PDA)

- The client-side implementation follows a similar structure to the program.
- The web3 public key is used to derive the program address.
- In this case, only "level one" is used as a seed for the PDA.

## Fetching Game Data Account

- The game data account is fetched using the program account and game data.
- RPC node is called to retrieve the data of the specified account.

Note: The summary has been created based on the provided transcript.
# [30:54](https://youtu.be/EKvJ4ShVzNA?t=1854) Creating a New Game Data Account and Signers

Section Overview: In order to perform transactions on Solana, a new game data account needs to be created. Every transaction requires a signer, which consists of a private and public key. The private key is needed to sign for changing data. Transactions are sent to the RPC node for propagation through the network and changing the state.

- A new game data account needs to be created.
- Every transaction requires a signer.
- Signers consist of a private and public key.
- The private key is needed to sign for changing data.
- Transactions are sent to the RPC node for propagation through the network and changing the state.

# [31:13](https://youtu.be/EKvJ4ShVzNA?t=1873) Transaction Stages and Confirmation

Section Overview: Transactions go through multiple stages, starting with being processed as soon as data changes in one of the validators. Once confirmed, it becomes non-revertible. Finalized stage ensures complete finality after 31 confirmations.

- Transactions go through multiple stages: processed, confirmed, finalized.
- Processed stage occurs when data changes in one of the validators.
- Confirmed stage indicates that the transaction will make it into the state.
- Finalized stage provides complete finality after 31 confirmations.

# [31:35](https://youtu.be/EKvJ4ShVzNA?t=1895) Creating Instructions and Fetching Game Data

Section Overview: After confirming a transaction, instructions can be created and executed. In this case, the "move left" method is called with the game data account. The game data account is then fetched to retrieve updated information.

- Create instructions for next transactions (e.g., "move left").
- Execute instructions by calling methods with relevant parameters (e.g., game data account).
- Send instructions to RPC node for confirmation.
- Fetch game data account after executing instructions.

# [32:37](https://youtu.be/EKvJ4ShVzNA?t=1957) Changing Text and Building the Program

Section Overview: To interact with the program, text can be changed and a story can be written. After modifying the text, the program needs to be built and deployed. The data and program ID are then sent for interaction within the Unity client.

- Change text and write a story.
- Build and deploy the program.
- Send data and program ID for interaction in Unity client.

# [33:28](https://youtu.be/EKvJ4ShVzNA?t=2008) Questions and Solana as a Database

Section Overview: Questions from participants are addressed. Solana is described as a big database where everything is an account with a unique address. Accounts consist of private and public keys, allowing only owners or authorized signers to make changes. Transactions consist of instructions, recent blockage ensures transaction validity, and v-payer pays for transaction fees.

- Addressing participant questions.
- Solana is described as a big database.
- Everything in Solana is an account with a unique address.
- Accounts have private and public keys for ownership verification.
- Transactions consist of instructions.
- Recent blockage ensures transaction validity.
- V-payer pays for transaction fees.

# [33:52](https://youtu.be/EKvJ4ShVzNA?t=2032) Account Representation and Transaction Validity

Section Overview: Account addresses in Solana are represented by 32 kilobyte strings using Base 58 encoding. Each wallet has a private-public key pair, allowing only owners to make changes to their accounts. Executable accounts like deployed programs can also be changed by authorized signers. Transactions require recent blockage for validation within a certain time frame.

- Account addresses in Solana are represented by 32 kilobyte strings using Base 58 encoding.
- Wallets have private-public key pairs for ownership verification.
- Only owners or authorized signers can change accounts.
- Executable accounts can also be changed by authorized signers.
- Transactions require recent blockage for validation within a certain time frame.

# [34:35](https://youtu.be/EKvJ4ShVzNA?t=2075) Multiple Instructions and Transaction Validity

Section Overview: Transactions can consist of multiple instructions, allowing for multiple changes to be made simultaneously. Recent blockage is crucial for validators to determine transaction validity within a specific time frame.

- Transactions can consist of multiple instructions.
- Multiple changes can be made simultaneously.
- Recent blockage is crucial for transaction validity.

# [35:17](https://youtu.be/EKvJ4ShVzNA?t=2117) Signers and Transaction Flow

Section Overview: Signers play a role in transaction validation. Additional signers can be added for co-signing or multi-signature transactions. A graph example illustrates the relationship between game data accounts, instructions, and the resulting game state.

- Signers play a role in transaction validation.
- Additional signers can be added for co-signing or multi-signature transactions.
- A graph example illustrates the relationship between game data accounts, instructions, and the resulting game state.

# [36:07](https://youtu.be/EKvJ4ShVzNA?t=2167) Interacting with Programs in Unity Client

Section Overview: The Unity client allows interaction with programs deployed on Solana. Changes made through interactions in Playground are reflected directly in the Unity client.

- Interact with programs deployed on Solana using the Unity client.
- Changes made through interactions in Playground are reflected directly in the Unity client.
# [37:01](https://youtu.be/EKvJ4ShVzNA?t=2221) Understanding the RPC Node and WebSocket Connection

Section Overview: In this section, the speaker explains how the RPC node and WebSocket connection work in Unity with Solana blockchain.

## Moving to the Right and Account Updates

- The speaker moves to the right in Unity, and it reflects on the right side because there is a WebSocket connection between the account and game data.
- Whenever there is a state change in Unity, the RPC node informs the client through WebSocket.

# [37:24](https://youtu.be/EKvJ4ShVzNA?t=2244) Reading and Writing Data with RPC Node

Section Overview: This section focuses on reading and writing data using the RPC node.

## Reading Data

- When reading data, the RPC node looks into its state, retrieves the requested version of data with commitment, and sends it back to the client via WebSocket.

## Writing Data

- To write data, a signed transaction with fees needs to be sent. The RPC node propagates this transaction to the current leader of the network.
- The leader distributes this data through a stake-weighted tree to all other validators who vote on its state.

# [38:03](https://youtu.be/EKvJ4ShVzNA?t=2283) State Changes and Real-Time Updates

Section Overview: This section discusses how state changes occur and real-time updates are achieved in Solana multiplayer games.

## Voting on State Changes

- Transactions are distributed as small parts called threads across the network for voting.
- Validators vote on these threads until a consensus is reached for changing the state.

## Real-Time Updates in Multiplayer Games

- When there is a change in state, such as updating an account's position, it is immediately pushed by the RPC node to all clients connected via WebSocket.
- This enables real-time updates for multiplayer games built on Solana blockchain.

# [38:44](https://youtu.be/EKvJ4ShVzNA?t=2324) Implementing Position in a Multiplayer Game

Section Overview: The speaker introduces the concept of implementing position in a multiplayer game and provides different options for achieving this.

## Adding X and Y Position

- The speaker suggests adding an X and Y position to enable movement in multiple directions.
- Different implementation options include saving X and Y positions as separate PDAs per ship, having one player with movable position, or saving the position as a string.

# [39:56](https://youtu.be/EKvJ4ShVzNA?t=2396) Introduction to Tiny Adventure 2

Section Overview: In this section, the speaker introduces Tiny Adventure 2 and explains how to save SOL (Solana's native token) in a PDA (Program Derived Address).

## Game Overview

- Tiny Adventure 2 is a game where players can reset levels, spawn chests, collect them by moving right, and eventually encounter chests with passwords.
- The goal is to learn how to save SOL in a PDA and require passwords for chest collection.

# [40:27](https://youtu.be/EKvJ4ShVzNA?t=2427) Saving SOL in a PDA with Password Protection

Section Overview: This section focuses on saving SOL in a PDA with password protection.

## Collecting Chests

- Initially, the speaker demonstrates collecting chests without any password requirement.
- To add password protection, modifications need to be made to the program code before redeploying it.

# [41:34](https://youtu.be/EKvJ4ShVzNA?t=2494) Opening Solana Playground for Tiny Adventure 2 Tutorial

Section Overview: This section guides participants on opening Solana Playground for the Tiny Adventure 2 tutorial.

## Accessing Solana Playground

- Participants are instructed to open Solana Playground again.
- They should select the "Tiny Adventure 2" tutorial from the available options.

# [42:25](https://youtu.be/EKvJ4ShVzNA?t=2545) Deploying Tiny Adventure 2

Section Overview: This section explains the process of deploying Tiny Adventure 2 and provides a cautionary note about closing programs.

## Deploying the Game

- Participants are guided through deploying Tiny Adventure 2, following similar steps as in the previous tutorial.
- It is emphasized that closing a program permanently disables its ID, so caution should be exercised when closing mainnet programs with active users.
# [43:14](https://youtu.be/EKvJ4ShVzNA?t=2594) Initializing and Transferring Soil

Section Overview: In this section, the speaker explains the process of initializing and transferring soil (a cryptocurrency) in Solana.

## Initializing Level One
- The speaker mentions that they have multiple accounts and start by initializing level one.
- The chest reward is introduced as one billion lampers divided by 10, resulting in 0.1 soil.
- When the level is reset, a chest is spawned and the player's position is set to zero.
- A cross-program invocation (CPI) is used to transfer some soil from the payer's account to another program-derived address using the system program transfer function.

## Transferring Soil into a PDA
- The speaker explains that a CPI context with the desired program (in this case, the system program) is created for invoking another program.
- They mention that it would be possible to invoke other programs like "Tiny Adventure" from this point onward.
- A transfer instruction is used to transfer soil from the payer's account to the chest vault.
- System Program transfer function is called with the CPI context and amount, facilitating the transfer of soil from the account wallet to a PDA (Program Derived Address).

## Example Run
- The speaker demonstrates an example run where they show various steps and their impact on balances.
- They highlight how transferring 0.1 soil into the chest reduces their balance accordingly.
- Moving right increases their position, while collecting the chest restores their balance back to its original value.

## Transferring Soil Back
- When at position two in front of the chest, one unit is added to the player's position.
- As it's not possible to use System Program transfer for transferring back from PDA owned by our program, an alternative approach is taken.
- The chest vault account owned by our program subtracts the chest reward from its balance.
- The player account receives the chest reward, ensuring that soil can only be removed from accounts when signed.

## Account Details
- The game data account remains the same as before (level one sign up, nine bytes).
- A new account called "chest vault" is introduced with eight bytes, which is the minimum for an anchor account.
- The speaker explains how anchor derives these eight bytes using a specific process involving hashing.
- Other accounts mentioned include signers, system program, spawn chest account, and move right account.

# [48:48](https://youtu.be/EKvJ4ShVzNA?t=2928) Initializing Level One

Section Overview: In this section, the speaker continues explaining the initialization of level one and introduces additional features.

## Initialization Process
- The speaker mentions that the initialization process can be called multiple times due to the addition of an "init if needed" function.
- They highlight that this function initializes a new account only if necessary; otherwise, it proceeds without reinitializing existing accounts.
- A loop is used to iterate through a range of values.

## Additional Features
- The speaker briefly mentions other features added in this example but does not provide further details.

Note: This section does not have enough information to create meaningful bullet points.
# [49:29](https://youtu.be/EKvJ4ShVzNA?t=2969) Adding a Password and Error Handling

Section Overview: In this section, the speaker discusses adding a password to the program and implementing error handling for incorrect passwords.

## Adding a Password

- The speaker suggests adding a password string to the program.
- If the entered password is incorrect, an error message will be displayed.
- The code should be built and deployed after making these changes.

## Error Handling

- An error occurs during deployment due to an uppercase string issue.
- The password validation function should return an error code instead of panicking.
- By returning an error code, it becomes possible to handle errors more effectively in the client application.
- The Unity client can display custom error messages based on specific error codes.
- The IDL file contains information about different error codes that can be used in the client application.

# [50:32](https://youtu.be/EKvJ4ShVzNA?t=3032) Displaying Errors in the Client Application

Section Overview: This section focuses on displaying errors in the Unity client application when wrong passwords are entered.

## Checking for Custom Errors

- After deploying the updated code, an error is encountered during execution related to sending transactions.
- To make errors more user-friendly, custom error codes can be created.
- A specific error code is assigned for wrong passwords (e.g., 6000).
- In the Unity client, transaction info is checked for custom errors and compared with the wrong password error code.
- If a match is found, a corresponding string message (e.g., "Wrong Password") is displayed on-screen.

## Exporting IDL File

- The IDL file can be exported from Solana Studio by clicking on the gear icon and selecting "Export" under IDL.
- This exported file provides detailed information about different tokens and their associated error codes.

# [53:26](https://youtu.be/EKvJ4ShVzNA?t=3206) Overview of Tiny Adventure 2 and Saving Soul

Section Overview: The speaker provides an overview of the Tiny Adventure 2 program and explains how to save soul in a PDA.

## Tiny Adventure 2 Flow

- The flow of the Tiny Adventure 2 program involves various actions such as getting player position, resetting levels, spawning chests, moving right, and checking passwords.
- The game data account position is set to zero during level reset.
- A small amount of soul is added to the chest vault when spawning chests.
- Moving right progresses through the game until reaching the end.
- Passwords are checked, and players receive their earned soul.

## Saving Soul in a PDA

- The process of saving soul in a PDA was previously demonstrated in the program.
- To transfer soul out of a PDA, subtracting lamports is necessary.
- Interacting with SPL tokens (e.g., USDC, Pirate Gold) requires understanding token accounts and associated token accounts.
- Token accounts owned by wallets can be easily accessed using associated token accounts derived from token mint and program ID.
- Creating a token account owned by the program requires adding an authority (e.g., token account owner).
- Transferring tokens in and out of an account can be done using transfer instructions within an Anchor CPI context.

# [54:04](https://youtu.be/EKvJ4ShVzNA?t=3244) Interacting with SPL Tokens

Section Overview: This section briefly discusses interacting with SPL tokens within a program.

## Understanding SPL Tokens

- Most tokens on Solana, such as USDC or Pirate Gold, are considered SPL tokens.
- Interacting with these tokens involves owning token accounts that are associated with wallets or programs.

## Associated Token Accounts

- Associated token accounts are derived from the name of the token mint and associated token program ID.
- They allow wallets to easily find specific token accounts within their holdings.
- Each wallet can have only one associated token account per token.

## Creating Token Accounts

- To create a token account owned by the program, an authority (e.g., token account owner) needs to be added.
- The mint (e.g., Pirate Gold, USDC) is specified when creating the token account.
- Tokens can then be transferred in and out of this account using transfer instructions within an Anchor CPI context.

Note: The speaker mentions that more detailed information on interacting with SPL tokens will be covered in a future session with Jacob regarding staking tokens.
# [56:26](https://youtu.be/EKvJ4ShVzNA?t=3386) Signing the PDA with the PDA for Transfer in the Program

Section Overview: This section explains how to sign the PDA (Program Derived Address) with the PDA for transfer in the program.

- To sign the PDA, use `CPI.context.new_signer()`.
- In this case, the signup would be for these seats: token account owner, PDA, and bump.

# [56:46](https://youtu.be/EKvJ4ShVzNA?t=3406) Setting Up Local Development Environment

Section Overview: This section provides instructions on setting up a local development environment.

- Follow the instructions in the Ink! installation documentation to install Rust and Solana.
- Install Rust using `rustup` with the newest compatible version.
- Install Solana CLI by running a specific command in any terminal.
- Create a key pair using `solana-keygen` or `solana-keygen new`.
- Transfer some SOL into your key pair for testing purposes.
- Install Yarn or NPM as package managers. Yarn is recommended for its speed and parallel processing capabilities.
- Install Anchor Version Manager (AVM) by copying and running a specific command in your terminal.
- Verify installations by checking versions of Anchor (`anchor --version`), Solana (`solana --version`), and Rust (`rustc --version`).

# [57:09](https://youtu.be/EKvJ4ShVzNA?t=3429) Checking Out Repository and Building Anchor Program Locally

Section Overview: This section explains how to check out a repository and build an Anchor program locally.

- Check out the "game starter kits" repository using any Git client.
- Open Visual Studio Code and navigate to the "tiny Adventure" folder within the repository.
- Inside Visual Studio Code, go to "app" > "program" folders.
- Run `anc build` to build your Anchor program. Make sure you have set up your wallet beforehand.
  - Use `solana balance -u devnet` to check your wallet balance.
  - Use `solana address` to get your wallet address.
  - Transfer SOL into your wallet using `solana airdrop`.

# [59:09](https://youtu.be/EKvJ4ShVzNA?t=3549) Deploying the Anchor Program

Section Overview: This section explains how to deploy the Anchor program.

- Define your program ID in the code.
- Deploy the program using the defined program ID.
- This step is similar to what was done in the playground, but now we are deploying it locally.

# [01:01:09](https://youtu.be/EKvJ4ShVzNA?t=3669) Introduction to Client and Recommended Extensions

Section Overview: This section introduces the client for the Anchor program and recommends useful extensions.

- Rust Analyzer: A must-have extension for working with Rust in Visual Studio Code. Provides type information, auto-completion, and more.
- Beta Toml: Formats TOML files for better readability.
- Arrow Lens: Enhances error display for easier debugging.
- GitHub Copilot: AI-powered tool that assists with auto-completing sentences and common coding patterns. Useful but should not be solely relied upon.
- Crates: Shows information about crates used in a project.

Note: Timestamps are provided where available.
# [01:03:19](https://youtu.be/EKvJ4ShVzNA?t=3799) Local Setup and Tools

Section Overview: In this section, the speaker discusses the local setup and tools required for the project.

## Setting Up Tools

- Install LLDB, a Rust debugger.
- Use Prettier to format code correctly.
- Install Visual Studio Code with Rust Analyzer extension for better coding experience.

## Configuring Analyzer and Formatting

- Configure the analyzer and formatting in your settings.
- Set the default format to Rust Analyzer.
- Add Rust Analyzer to Clippy instead of using the default one.

## Running the Program Locally

- Go into the program directory.
- Install npm packages using `npm install` or yarn packages using `yarn install`.
- Run tests and deploy the program using `anchor test`.
- Run a local validator using `Solana test validator`.
- Deploy to localhost in Playground and receive free SOL tokens.

## Running the JavaScript Client

- Go into the app folder.
- Run `yarn Dev` to start the JavaScript client.
- The client uses Next.js framework for UI development.
- It includes features like moving characters, getting data, initializing, and wallet adapter for user convenience.

## Additional Resources

- Visit Solana Stack Exchange for asking questions related to Solana development.
- Watch tutorials on Rust programming language to learn about borrow checks, enums, option types, etc.
# [01:09:55](https://youtu.be/EKvJ4ShVzNA?t=4195) Next.js Apps and API Integration

Section Overview: In this section, the speaker discusses how Next.js apps can integrate with APIs to perform actions on the backend. They demonstrate an example of calling an API to interact with a game without being logged in.

## Integrating with APIs in Next.js

- Next.js apps can call APIs to perform actions on the backend.
- The speaker demonstrates an example where an API is called to interact with a game even when not logged in.
- The API used for this example is the "Valiant transaction API" which allows users to move within the game.
- Transaction fees for these interactions are paid using a burner key pair associated with the API.

# [01:10:20](https://youtu.be/EKvJ4ShVzNA?t=4220) Burner Key Pair and Environment Setup

Section Overview: This section focuses on the burner key pair used for interacting with the Valiant transaction API and provides insights into environment setup.

## Burner Key Pair and Environment File

- The burner key pair is used for signing transactions when interacting with the Valiant transaction API.
- It is important to keep private keys secure and never share them publicly.
- An environment file contains configuration details, including the burner key pair, required for setting up the environment.

# [01:10:39](https://youtu.be/EKvJ4ShVzNA?t=4239) Interacting with Games via APIs

Section Overview: This section explains how games can be interacted with through APIs, even without being logged in.

## Interacting with Games without Login

- Users can interact with games even if they are not logged in by making use of APIs.
- The speaker demonstrates how they can still move within a game without being logged in by calling an appropriate API endpoint.
- The Valiant transaction API is responsible for handling these interactions.

# [01:10:58](https://youtu.be/EKvJ4ShVzNA?t=4258) Transaction Fees and API Functionality

Section Overview: This section discusses the payment of transaction fees and the functionality of the Valiant transaction API.

## Transaction Fees and API Functionality

- The Valiant transaction API handles the payment of transaction fees using the burner key pair.
- The API receives instructions from either query parameters or request body.
- Depending on the instruction received, such as "move right" or "move left," appropriate actions are performed within the game.
- The recent blockage is obtained to ensure accurate execution of transactions.
- Transactions are sent with a signer, where the signer corresponds to the burner key pair.

# [01:11:24](https://youtu.be/EKvJ4ShVzNA?t=4284) Backend Key Pair for Signing Transactions

Section Overview: This section explains how a backend key pair can be used to sign transactions in order to ensure their authenticity before sending them to clients.

## Backend Key Pair for Signing Transactions

- A backend key pair is used for signing transactions in the backend.
- This allows for partial signing, ensuring that transactions are verified and authorized before being sent to clients.
- By signing transactions in the backend, it provides an additional layer of security and control over transaction execution.

# [01:11:57](https://youtu.be/EKvJ4ShVzNA?t=4317) Unity Game Engine Introduction

Section Overview: In this section, an introduction to Unity game engine is provided, including information on downloading and installing Unity Hub.

## Introduction to Unity Game Engine

- Unity game engine is introduced as a powerful tool for creating games.
- To get started with Unity, users need to download and install Unity Hub from unity.com.
- Once installed, users can access various examples and starter kits provided by Solana for game development.

# [01:12:38](https://youtu.be/EKvJ4ShVzNA?t=4358) Using Unity with Solana Game Starter Kits

Section Overview: This section explains how to use Unity with Solana game starter kits, specifically focusing on the Seven Seas example.

## Using Unity with Solana Game Starter Kits

- Users can access Solana game starter kits, including the Seven Seas example, within the Unity folder of the Solana game starter kits.
- Unity provides extensive capabilities for game development, similar to JavaScript and web3.js.
- Features such as RPC support, transaction creation, and exporting to various platforms (Android, iOS, Windows) are available in Unity.
- Supported wallets include wallet adapter for WebGL and all wallets for Android. Currently, only Phantom supports iOS using deep links.

# [01:13:24](https://youtu.be/EKvJ4ShVzNA?t=4404) Blockchain Games and Wallet Support

Section Overview: This section discusses blockchain games and wallet support in Unity, including potential opportunities for community contributions.

## Blockchain Games and Wallet Support

- Unity can be used to create blockchain games that interact with the Solana blockchain.
- Wallet support is available for WebGL (wallet adapter) and Android (all wallets). For iOS, currently only Phantom supports it using deep links.
- The speaker encourages community participation in adding support for Soleflare on iOS through a pull request.
- A comparison between C# and JavaScript implementation in Unity is provided.

# [01:14:30](https://youtu.be/EKvJ4ShVzNA?t=4470) Solnet Implementation and Code Generation Tool

Section Overview: This section explains the solnet implementation in Unity SDK and introduces a code generation tool for creating C# representations of games.

## Solnet Implementation and Code Generation Tool

- The unity SDK is based on solnet implementation.
- A code generation tool maintained by Magic Block allows users to generate C# representations of their games from IDL JSON files.
- The tool can be installed using `dot net tool install sodana Unity anchor tool`.
- By providing an IDL JSON file as input and specifying an output location, users can generate C# representation of their game.

# [01:15:23](https://youtu.be/EKvJ4ShVzNA?t=4523) Using the Code Generation Tool

Section Overview: This section demonstrates how to use the code generation tool in Unity to create C# representation of a game.

## Using the Code Generation Tool

- The speaker provides step-by-step instructions on using the code generation tool.
- Users need to navigate to the program folder and run the tool with appropriate input and output parameters.
- The IDL JSON file is used as input, and the generated C# representation is saved in the specified output location.

# [01:16:25](https://youtu.be/EKvJ4ShVzNA?t=4585) Unity Setup for Tiny Adventure Game

Section Overview: This section focuses on setting up Unity for the Tiny Adventure game example.

## Unity Setup for Tiny Adventure Game

- Users can find the Tiny Adventure game example within the Seven Seas example folder in Solana game starter kits.
- The speaker highlights important elements such as program ID, game data account, and level one program address within this setup.
# [01:17:22](https://youtu.be/EKvJ4ShVzNA?t=4642) Understanding the Game Data Account

Section Overview: In this section, the speaker explains the structure and purpose of the game data account in the Tiny Adventure game client.

## Game Data Account Details

- The game data account contains base64 decoded data.
- It is a part of the Tiny Adventure account client.
- The account includes necessary information such as discriminators, serialized data, and functions like move left and move right.

# [01:17:49](https://youtu.be/EKvJ4ShVzNA?t=4669) Simplified Instruction Creation

Section Overview: This section discusses how instructions are created for specific actions in the game.

## Creating Instructions

- The game provides pre-defined instructions for actions like moving right.
- Users don't need to worry about specific data or discriminators.
- To perform an action, users retrieve the corresponding instruction from the account and execute it using program ID and other required parameters.

# [01:18:12](https://youtu.be/EKvJ4ShVzNA?t=4692) Manual Transaction Creation

Section Overview: Here, manual transaction creation is explained as an alternative method to interact with the game.

## Manual Transaction Process

- Manually creating a transaction involves creating a new transaction object.
- The object includes recent blockage signature, empty signatures (to be filled by wallet adapter), instructions, and additional instructions if needed.
- Multiple instructions can be added to a single transaction for different actions like moving left or right.

# [01:18:30](https://youtu.be/EKvJ4ShVzNA?t=4710) Unity Implementation Example

Section Overview: This section demonstrates how transactions are implemented in Unity using code snippets.

## Unity Implementation Steps

- Transactions in Unity involve creating a new transaction object with necessary details.
- Instructions are added to the transaction object based on desired actions (e.g., move left or right).
- Additional features can be implemented by adding more instructions to a single transaction.

# [01:18:48](https://youtu.be/EKvJ4ShVzNA?t=4728) Homework and Further Resources

Section Overview: The speaker provides homework and additional resources for further learning.

## Homework and Resources

- Homework task: Modify the Tiny Adventure game to allow movement in all directions (up, down, left, right).
- Additional resources: Seven Seas example for further exploration.
- Questions can be asked in the comments section.

# [01:19:10](https://youtu.be/EKvJ4ShVzNA?t=4750) Future Topics and Conclusion

Section Overview: The speaker discusses future topics and concludes the session.

## Future Topics

- On the sixth day, implementation of the Seven Seas game will be covered in detail.
- All functions and features of the game will be explored.

## Conclusion

- A list of resources covered in the session is provided.
- Encouragement is given to build exciting projects in the coming days.
- Upcoming topics include staking gold, upgrading pirate ships, and participating in swap programs.

[Generated with Video Highlight](https://videohighlight.com/video/summary/EKvJ4ShVzNA)
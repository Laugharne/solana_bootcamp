# [](https://youtu.be/v88C0jL8pTQ?t=0) Introduction to Solana Pay and its Use Cases

Section Overview: In this section, we learn about Solana Pay and its various use cases beyond payments. We also explore how transaction requests can be used to interact with the Seven Seas game.

## Understanding Solana Pay

- Solana Pay is a payments protocol that goes beyond traditional payment use cases.
- It offers low transaction fees, fast settlement, and high throughput, making it suitable for building enterprise-grade payment infrastructure.
- The protocol solves the problem of connecting on-chain transactions to specific orders in e-commerce or point-of-sale terminals.
- Composability is a key feature of the Solana blockchain, allowing cross-promotions between different platforms and enabling dynamic checkout experiences based on user wallets.

## Use Cases of Solana Pay

- Solana Pay has been used for various purposes related to NFTs, such as minting, dynamic discounts, loyalty programs, and even photo booth experiences where users can mint NFTs directly to their wallets.
- In the demo of the Seven Seas game, we utilize Solana Pay for a pirate-themed use case.

# [01:05](https://youtu.be/v88C0jL8pTQ?t=65) Attributes of Solana Pay

Section Overview: This section highlights the key attributes of Solana Pay that make it an attractive option for merchants.

## Instant Settlement and Zero Fees

- With Solana Pay, settlements are instant. Merchants receive capital immediately after a customer makes a payment.
- Transaction fees are extremely low (e.g., 0.001 cent), almost negligible.
- Blockchain technology eliminates fraud possibilities like chargebacks or unauthorized credit card usage.

## Permissionless Innovation and Direct Communication

- By having access to users' wallet addresses through Solana Pay, merchants can offer dynamic checkout experiences without relying on third-party teams.
- Direct communication channels between merchants and customers enable personalized advertisements and immersive commerce engagements.

# [03:46](https://youtu.be/v88C0jL8pTQ?t=226) Solana Pay's Extensibility

Section Overview: This section emphasizes the extensibility of Solana Pay beyond payments.

## Use Cases Beyond Payments

- Despite its name, Solana Pay can be used for various purposes beyond payments.
- Transaction requests allow servers to access user wallet addresses, enabling interactions with NFTs, tokens, and specific protocols on-chain.
- The flexibility of Solana Pay makes it suitable for building custom checkout experiences and integrating with different platforms.

# [04:31](https://youtu.be/v88C0jL8pTQ?t=271) Benefits of Using Solana Pay

Section Overview: This section highlights the benefits that merchants gain from using Solana Pay.

## Instant Settlement and Capital Deployment

- Instant settlement allows merchants to have capital readily available for immediate deployment.
- Merchants can utilize received funds without delays or waiting periods.

## Zero Fees and Fraud Prevention

- The low transaction fees (almost zero) minimize costs for merchants.
- Blockchain technology eliminates fraud possibilities like chargebacks or unauthorized credit card usage.

## Permissionless Innovation and Direct Communication

- Merchants can offer dynamic checkout experiences based on users' assets without requiring approval from third-party teams.
- Direct communication channels between merchants and customers enable personalized advertisements and immersive commerce engagements.
# [06:19](https://youtu.be/v88C0jL8pTQ?t=379) Transfer Request for SBO Token

Section Overview: This section explains the transfer request process for an SBO token, including the optional fields and the importance of the reference or UUID.

## Transfer Request Process

- A transfer request can be made for an SBO token, which is optional as Native Soul can also be used.
- The transfer request includes the token mint, label, message, and an optional memo.
- The reference or UUID is crucial as it acts as a unique identifier to link the transaction happening on a store or point of sale system with the on-chain transaction.

# [06:36](https://youtu.be/v88C0jL8pTQ?t=396) Importance of Reference in Transfer Request

Section Overview: This section emphasizes the significance of the reference or UUID in connecting commerce transactions with on-chain transactions.

## Significance of Reference

- The reference or UUID connects commerce transactions with on-chain transactions.
- It serves as a randomly generated public key that should only be used once.
- The reference allows wallets supporting Solana Pay to decode QR codes and retrieve necessary parameters for the transfer request.

# [07:24](https://youtu.be/v88C0jL8pTQ?t=444) Wallet Support for Solana Pay

Section Overview: This section discusses wallets that currently support Solana Pay and their compatibility with scanning QR codes.

## Wallet Compatibility

- Wallets that support Solana Pay can decode QR codes encoded with transfer request URLs.
- Scanning such QR codes enables wallets to extract necessary parameters for processing transfers.
- Users need to ensure their chosen wallet supports Solana Pay before initiating transfers.

# [07:34](https://youtu.be/v88C0jL8pTQ?t=454) Transaction Requests in Solana Pay V2

Section Overview: This section introduces transaction requests in Solana Pay V2, which allow users to construct any valid Solana transaction.

## Transaction Requests

- In Solana Pay V2, users can construct any valid Solana transaction using transaction requests.
- Transaction requests are still URL-based but point to the user's server, which needs to respond to both GET and POST requests.
- Wallets make two requests (GET and POST) to the server upon scanning the QR code.
- The GET request expects a response with an icon and label for display purposes.
- The POST request includes the account address of the person who scanned the QR code.
- The server must respond with a valid transaction based on the received POST request.

# [09:06](https://youtu.be/v88C0jL8pTQ?t=546) Creating Valid Transactions in Solana Pay

Section Overview: This section explains how servers can create valid transactions upon receiving POST requests from wallets.

## Creating Valid Transactions

- Upon receiving a POST request, servers need to respond with a valid transaction.
- This process was demonstrated earlier in the workshop when scanning a QR code caused an interaction with the Seven Seas program.
- Servers have flexibility in creating various types of transactions beyond payments.

# [09:46](https://youtu.be/v88C0jL8pTQ?t=586) Setting Up Project Directories

Section Overview: This section covers setting up project directories for following along with the workshop.

## Project Directory Setup

- To follow along, create a project directory using VS Code or any preferred editor.
- Initialize a basic project within this directory using `npm init -y`.
- Create an "API" directory within the project directory and add an `index.js` file inside it.

# [10:26](https://youtu.be/v88C0jL8pTQ?t=626) Installing Dependencies

Section Overview: This section explains how to install necessary dependencies for working with Solana and Grok.

## Dependency Installation

- Install Solana and Grok dependencies locally using npm or yarn.
# [12:59](https://youtu.be/v88C0jL8pTQ?t=779) Setting up the Default Function

Section Overview: In this section, the focus is on exporting a default function titled "Handler" that takes a request and a response. The goal is to console.log that the function is handling a request and log out the request method.

## Exporting Default Function

- The convention is to export a default function named "Handler" that takes a request and a response.
- Console.log that the function is handling a request and log out the request method.
- Return a response for both GET and POST requests with status 200 in JSON format.

# [14:02](https://youtu.be/v88C0jL8pTQ?t=842) Running the Server Locally

Section Overview: This section covers running the server locally using `npx first-so-dev` command. It also verifies if the server is working by accessing `localhost/api` endpoint.

## Running Local Server

- Use `npx first-so-dev` command to run the server locally.
- Access `localhost/api` endpoint to verify if it returns an empty JSON response.
- Check console logs to confirm that requests are being handled correctly.

# [15:07](https://youtu.be/v88C0jL8pTQ?t=907) Exposing Local Server via External URL

Section Overview: Here, we use NGROK to expose our local port via an external URL. This step is necessary for testing our Solana pay endpoint, as it needs to hit our server when scanning QR codes from mobile wallets.

## Exposing Local Server

- Run NGROK in another terminal session to expose local port via an external URL.
- Obtain the external URL provided by NGROK for accessing our local server.
- Update code with this external URL in place of localhost/api endpoint.
- Verify that hitting this new URL still returns an empty JSON response and logs requests correctly.

# [16:06](https://youtu.be/v88C0jL8pTQ?t=966) Setting Up QR Code for Local Development Server

Section Overview: This section focuses on setting up a QR code that points to the local development server. The QR code is created using the "QR code styling" library and should conform to the Solana P spec.

## Creating QR Code

- Use the "QR code styling" library to create a QR code.
- Copy the URL obtained from NGROK, including the "/api" endpoint.
- Ensure that the URL used in the QR code is prefixed with "Solana:" as per Solana P spec.
- Test scanning the QR code with a mobile wallet to ensure it shows the correct information.

# [17:39](https://youtu.be/v88C0jL8pTQ?t=1059) Completing API Endpoint for Solana P Spec

Section Overview: In this section, we modify our API endpoint to conform to the Solana P spec. Currently, it only returns an empty JSON response, which is not useful. We add a GET handler and prepare for handling POST requests in future.

## Modifying API Endpoint

- Create a GET handler function that takes a response and returns a status 200 JSON response with label and icon.
- Update existing code to include console logs only for sanity check purposes.
- If request method is GET, return handle get function with response as parameter.
- For now, if request method is not GET (i.e., POST), return an error message.

Note: The transcript does not provide further details beyond this point.
# [20:19](https://youtu.be/v88C0jL8pTQ?t=1219) Testing the Endpoint

Section Overview: The speaker discusses different ways to test the endpoint, either by accessing it through a browser or scanning a QR code with a wallet like Phantom.

## Testing Options

- Access the endpoint in a browser by appending "/API" to the URL.
- Scan the QR code with a compatible wallet like Phantom.

# [20:44](https://youtu.be/v88C0jL8pTQ?t=1244) Handling GET Requests

Section Overview: The speaker explains that when scanning the QR code on a mobile device, both GET and POST requests are sent to the server. However, only software like Scan will display UI widgets with correct labels and icons.

## GET Request Handling

- When scanning the QR code, GET requests can be observed on the server.
- UI widgets may not appear on mobile wallets, but software like Scan should display them correctly.

# [21:32](https://youtu.be/v88C0jL8pTQ?t=1292) Creating POST Response

Section Overview: The speaker introduces handling POST requests and logging out account information from the request body. A response is scaffolded with status 200 and a placeholder transaction.

## Handling POST Requests

- Create a function called `handlePost` that takes both request and response as parameters.
- Log out account information from `request.body.account`.
- Scaffold response with status 200 and placeholder transaction.
- Add an `else if` condition for POST requests (in all caps).

# [23:14](https://youtu.be/v88C0jL8pTQ?t=1394) Validating POST Requests

Section Overview: The speaker mentions that proper validation checks should be implemented for account presence. A temporary trick using VS Code's `@tscheck` comment is used to type-check JavaScript code.

## Validating Account Presence

- Implement validation checks to ensure account presence (not shown in example).
- Use VS Code's `@tscheck` comment to perform type-checking.

# [24:01](https://youtu.be/v88C0jL8pTQ?t=1441) Routing Requests

Section Overview: The speaker explains that GET requests are routed to the `handleGet` function, POST requests are routed to the `handlePost` function, and other methods are currently not allowed.

## Request Routing

- GET requests are routed to the `handleGet` function.
- POST requests are routed to the `handlePost` function.
- Other methods are currently not allowed.

# [24:23](https://youtu.be/v88C0jL8pTQ?t=1463) Building Handle Post Function

Section Overview: The speaker starts building the `handlePost` function by creating a player object using the account from the request. A placeholder instruction and transaction are also scaffolded.

## Creating Handle Post Function

- Create a player object using `new PublicKey(request.body.account)`.
- Scaffold a placeholder instruction called `createCthuluInstruction`, which requires the player parameter.
- Scaffold a placeholder transaction preparation function called `prepareTransaction`, which requires the Cthulhu instruction parameter.

# [25:36](https://youtu.be/v88C0jL8pTQ?t=1536) Finalizing Handle Post Function

Section Overview: The speaker summarizes the steps required to get the correct transaction in the handle post function. The necessary components include obtaining the public key, creating a Cthulhu instruction, and preparing the transaction with base64 encoding.

## Finalizing Handle Post Function

- Obtain public key using `new PublicKey(request.body.account)`.
- Create Cthulhu instruction using player account.
- Prepare transaction by encoding it with base64.
- Use temporary trick with VS Code's `@tscheck` comment for type-checking JavaScript code.

# [26:27](https://youtu.be/v88C0jL8pTQ?t=1587) Installing Dependencies

Section Overview: The speaker sets up another terminal session to install required dependencies, specifically Solano web3.js, which provides the necessary functions for obtaining the public key.

## Installing Dependencies

- Install Solano web3.js using the terminal.
- Add missing import from web pages for the public key.

# [26:59](https://youtu.be/v88C0jL8pTQ?t=1619) Creating Instruction Function

Section Overview: The speaker starts creating the `createInstruction` function, which will involve getting the player's gold token account.

## Creating Instruction Function

- Create a function called `createInstruction` that takes in the player parameter.
- Get the player's gold token account (not explained further).

# [27:23](https://youtu.be/v88C0jL8pTQ?t=1643) Summary of Required Steps

Section Overview: The speaker summarizes the required steps for creating an instruction, including obtaining the player's gold token account.

## Summary of Required Steps

- Obtain the player's gold token account (not explained further).
# [27:48](https://youtu.be/v88C0jL8pTQ?t=1668) Getting the Token Account

Section Overview: In this section, the speaker explains how to retrieve the token account using a helper function from the Solana SPL token library.

## Retrieving the Token Account

- To get the PleasGo token account, a helper function from the Solana SPL token library is used.
- The function `getOrCreateAssociatedTokenAccount` is called with parameters such as connection, payer, gold token mint, and place account.

# [28:25](https://youtu.be/v88C0jL8pTQ?t=1705) Importing Libraries and Defining Variables

Section Overview: This section covers importing necessary libraries and defining variables required for further steps.

## Importing Libraries and Defining Variables

- Install the SPL token library, dot EnV, and base58 library.
- Add these dependencies to the project.
- Import `getOrCreateAssociatedTokenAccount` from `@solana/spl-token`.
- Define variables such as connection (from SP web3.js library), payer (to be defined later), and gold token mint.

# [29:34](https://youtu.be/v88C0jL8pTQ?t=1774) Missing Variables - Connection

Section Overview: Here, the missing variable "connection" is explained. It will be obtained from the SP web3.js library.

## Missing Variable - Connection

- The missing variable "connection" will come from the SP web3.js library.
- For this purpose, devnets will be used as it is where the 70s game is deployed.

# [30:07](https://youtu.be/v88C0jL8pTQ?t=1807) Missing Variables - Payer and Gold Token Mint

Section Overview: This section discusses two more missing variables - payer and gold token mint.

## Missing Variables - Payer and Gold Token Mint

- The payer variable will be left blank for now.
- The gold token mint will be a standardized one created in the deployed Seven Seas game.

# [31:09](https://youtu.be/v88C0jL8pTQ?t=1869) Fee Payer and Secret Key

Section Overview: Here, the concept of fee payer and secret key is explained. The speaker demonstrates how to set the fee payer using Solana's paid transaction request.

## Fee Payer and Secret Key

- The fee payer can choose to pay the fees for transactions.
- The secret key will be stored as an environment variable for security purposes.
- The speaker uses the base58 library to decode the environment variable containing the secret key.

# [34:24](https://youtu.be/v88C0jL8pTQ?t=2064) Creating Instruction Manually

Section Overview: In this section, the process of manually creating instructions is explained since Anchor is not used. The required accounts and ID for the Seven Seas program are also mentioned.

## Creating Instruction Manually

- Required accounts for the Cotulli instruction are obtained from either Anchor IDL or by examining the Seven Seas program.
- Instructions need to be constructed manually when not using Anchor.
- The ID for the Seven Seas program should not be forgotten while creating instructions.
- A new transaction instruction is returned.

Note: Timestamps have been associated with bullet points where available.
# [35:25](https://youtu.be/v88C0jL8pTQ?t=2125) Setting up Keys and Data Property

Section Overview: In this section, the speaker discusses the keys and data property required for the program.

## Keys
- The order of the keys is important as it follows the Katula instruction.
- The first key needed is the chest vault, with `isWritable` set to true and `isSigner` set to false.
- The second key is the level, with `isWritable` set to true and `isSigner` set to false.
- The third key is the game actions, with `isWritable` set to false and `isSigner` set to false.
- Next is the player, with `isWritable` set to true and it must be a signer.
- Then comes the player's token account, with `isWritable` set to true and `isSigner` set to false.
- After that is the system program ID, with `isWritable` and `isSigner` both set to false.
- Following that is another instance of the player, with `isWritable` set to false.
- Then we have the player's token account owner PDAID, with `isWritable` set to true and `isSigner` set to false.
- Next is the token vault, with `isWritable` set to true and `isSigner` set to false.
- Lastly, we have the token mint from SBO token library, with both `isWritable` and `isSigner` being false.

## Data Property
- The data property specifies which instruction in the program needs to be called along with any related data for that instruction. 
- A rudimentary approach has been used here by copying from a prepared buffer. Refactoring will be done later using Anchor.

# [41:13](https://youtu.be/v88C0jL8pTQ?t=2473) Anchor Discriminator and Instruction

Section Overview: The speaker discusses the anchor discriminator and passing data to the function.

- The anchor discriminator is used to determine which function in the program needs to be called.
- There are multiple ways to obtain the anchor discriminator, but a more rudimentary approach is used here.
- The actual buffer for the instruction is copied from a prepared earlier version.
- Refactoring will be done later to demonstrate a general approach using Anchor.

# [42:31](https://youtu.be/v88C0jL8pTQ?t=2551) Prepare Transaction Function

Section Overview: The speaker explains the prepare transaction function.

- The prepare transaction function takes an instruction and returns the desired transaction.
- To create a new transaction, `new Transaction` from web3.js is used.
- The instruction is added to the transaction using `transaction.add`.
- Properties are set on the transaction, starting with `recentBlockHash`, obtained using `connection.getLatestBlockHash`.

# [43:00](https://youtu.be/v88C0jL8pTQ?t=2580) Completing Prepare Transaction Function

Section Overview: The speaker continues explaining how to complete the prepare transaction function.

- An async function is required for this step as it involves awaiting `connection.getLatestBlockHash`.
- After obtaining the recent block hash, other properties of the transaction can be set.
# [44:12](https://youtu.be/v88C0jL8pTQ?t=2652) Setting up the Transaction

Section Overview: In this section, the speaker explains how to set up a transaction and handle the fee payer.

## Setting the Block Hash and Fee Payer
- The block hash property needs to be set for the transaction.
- The fee payer is set as the payer for the transaction.
- Partial signing of the transaction is required when setting ourselves as the fee payer.

## Serializing and Returning the Transaction
- Serialize the transaction and return it as a base64 string.
- Set verify signatures to false.
- Return serialized transaction as a base64 string.

# [45:59](https://youtu.be/v88C0jL8pTQ?t=2759) Finalizing the Transaction

Section Overview: This section covers finalizing the transaction by signing it and preparing it for execution.

## Steps to Finalize Transaction
- Create a new transaction with desired instructions.
- Set recent block hash and fee payer for the transaction.
- Partially sign the transaction since we are setting ourselves as fee payer.
- Serialize and return the finalized transaction as a base64 string.

# [46:27](https://youtu.be/v88C0jL8pTQ?t=2787) Preparing Environment Variables

Section Overview: Here, instructions are given on how to create an environment variable file with private key information.

## Creating Environment Variable File
- Create an environment variable file (`.env`).
- Set `payer` variable in `.env` file with your private key information.

# [46:53](https://youtu.be/v88C0jL8pTQ?t=2813) Testing QR Code Scanning

Section Overview: This section focuses on testing QR code scanning functionality.

## Scanning QR Code
- Open QR code scanner using Solana colon NG Rockin API URL.
- Scan QR code generated from previous steps.

# [47:26](https://youtu.be/v88C0jL8pTQ?t=2846) Troubleshooting Errors

Section Overview: The speaker encounters an error and troubleshoots the issue.

## Identifying the Error
- Observe the error message from the wallet.
- Check if server is responding with a GET and POST request.

# [47:40](https://youtu.be/v88C0jL8pTQ?t=2860) Handling Async Functions

Section Overview: This section addresses handling async functions to resolve errors.

## Making Functions Async
- Convert `handlePost` function to an async function.
- Await the `prepareTransaction` function within `handlePost`.

# [48:27](https://youtu.be/v88C0jL8pTQ?t=2907) Confirming Transaction

Section Overview: The speaker confirms the transaction and checks for successful execution.

## Confirming Transaction
- Allow confirmation of transaction on wallet UI.
- Verify that both GET and POST requests are successful.

# [49:16](https://youtu.be/v88C0jL8pTQ?t=2956) Recap and Conclusion

Section Overview: The speaker summarizes the process of setting up a Cotulla instruction and concludes the workshop.

## Recap of Workshop
- Cotulla instruction can be used for more than just payments.
- The final code and text-based walkthrough are available on GitHub.
- Thank viewers for joining.

[Generated with Video Highlight](https://videohighlight.com/video/summary/v88C0jL8pTQ)
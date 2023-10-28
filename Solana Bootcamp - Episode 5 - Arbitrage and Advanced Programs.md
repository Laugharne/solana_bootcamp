# [](https://youtu.be/XiA_pBftFt4?t=0)

Section Overview: In this section, the speaker introduces the concept of arbitrage trading and its relevance in the cryptocurrency market.

## What is Arbitrage Trading?

- Arbitrage trading involves taking advantage of price discrepancies between different markets or over time to make a profit.
- It can be applied to various financial instruments, including stocks, foreign currency pairs, and cryptocurrencies.
- In crypto, arbitrage trading has found a suitable environment due to its decentralized nature.

## Types of Arbitrage Trading

- Spatial Arbitrage: Exploiting price differences in different geographical regions.
- Temporal Arbitrage: Taking advantage of price differences at different points in time.
- Statistical Arbitrage: Profiting from price inefficiencies by analyzing statistical relationships between securities.

## Example Scenario

- Consider two liquidity pools with assets A and B.
- Pool 1 offers a ratio of 5 A for 10 B, while Pool 2 offers a ratio of 5 A for 5 B.
- By executing an arbitrage opportunity, one can swap assets between the pools and increase their holdings.

# [03:02](https://youtu.be/XiA_pBftFt4?t=182)

Section Overview: This section focuses on building an arbitrage program using liquidity pools as an example.

## Liquidity Pools and Ratios

- Liquidity pools offer trade-for-trade value based on their liquidity ratios.
- If two pools have different ratios for the same assets, an arbitrage opportunity arises.

## Executing the Arbitrage Opportunity

- Start with asset A in Pool 1 and swap it for asset B to increase holdings.
- Then swap asset B from Pool 2 back into asset A to further increase holdings.
- By executing this sequence, one can double their assets through arbitrage trading.

Note: The success of arbitrage opportunities depends on factors such as timing, fees, and the stability of price differences.

# Conclusion

Arbitrage trading is a strategy that takes advantage of price discrepancies to make a profit. In the cryptocurrency market, it has become popular due to its decentralized nature. By understanding different types of arbitrage trading and building an arbitrage program using liquidity pools as an example, individuals can explore opportunities for maximizing their holdings. However, it's important to consider various factors that may affect the success of these opportunities.
# [06:11](https://youtu.be/XiA_pBftFt4?t=371) Understanding Asset Movement in Arbitrage Trading

Section Overview: In this section, the speaker discusses how assets are moved between pools in arbitrage trading and the factors that influence asset movement.

## Asset Movement between Pools

- Assets are pulled out of Pool 1 and put into Pool 2 to make profitable trades.
- Pool 1 is willing to provide more of asset B because it has a surplus of asset A but lacks asset B.
- Pool 2 might have a surplus of asset A but lacks asset B.
- As more asset B is added to Pool 2, it offers more of asset B over time.
- This creates a difference in the constant product value of r between the two pools, encouraging arbitrage trading.

# [07:50](https://youtu.be/XiA_pBftFt4?t=470) Encouragement and Risks of Arbitrage Trading

Section Overview: This section highlights the benefits and risks associated with arbitrage trading.

## Benefits of Arbitrage Trading

- Earn risk-free profits by taking advantage of price differences.
- Make efficient use of capital by diversifying portfolios through arbitraging different assets.
- Low market exposure as trades are quick and can be automated with bots.

## Risks of Arbitrage Trading

- Unexpected price changes can lead to losses.
- Errors or delays in execution can result in financial losses.
- Inability to exit positions when desired due to various factors.
- Lack of clarity on regulations adds uncertainty to arbitrage trading.

# [09:50](https://youtu.be/XiA_pBftFt4?t=590) Setting Up the Swap Program for Testing

Section Overview: The speaker explains how to set up the swap program for testing purposes.

## Steps for Setting Up Swap Program Testing

1. Copy the program ID from the previously deployed swap program.
2. Navigate to the tests for our program and paste the program ID into the designated field.
3. Ensure that the assets used in the previous session are still available and do not recreate them.
4. Clear out any previous runs of the swap program.
5. Follow the necessary steps to initialize and run tests against the swap program.

Note: The specific steps may vary depending on individual circumstances, such as being the mint authority for certain assets.

# [10:56](https://youtu.be/XiA_pBftFt4?t=656) Deploying a New Swap Program

Section Overview: The speaker explains how to deploy a new swap program for testing purposes.

## Deploying a New Swap Program

1. Copy and paste the program ID into the designated field for the new swap program.
2. Run new swaps and initialize liquidity pools without recreating assets.
3. Ensure that all necessary configurations are in place, including addresses and decimals.

Note: It is important to maintain consistency with asset addresses when running tests on different programs.

These notes provide an overview of key points discussed in the transcript, focusing on asset movement in arbitrage trading, benefits and risks of arbitrage trading, setting up the swap program for testing, and deploying a new swap program.
# [12:42](https://youtu.be/XiA_pBftFt4?t=762) Setting up the Environment

Section Overview: The speaker discusses the steps to set up the environment for building and deploying an Arbitrage bot.

## Populating lib RS and Saving Files

- Anchor.tomml file is added to lib RS.
- Both files are saved.
- Building is done again to ensure that the declare ID has the correct value in the binary.

## Deploying to Devnet

- Anchor deploy command is used to deploy to Devnet.
- It is important to remain on Devnet during this process.

# [13:04](https://youtu.be/XiA_pBftFt4?t=784) Setting Up Swap Programs

Section Overview: The speaker explains how two live swap programs are set up for testing Arbitrage opportunities.

## Deploying Second Swap Program

- A new ID for the second swap program is obtained after deployment.
- The ID is added to "swap program 2".
- Two swap programs are now available for arbitrage trading.

## Installing Dependencies and Running Tests

- Yarn install command is used to install dependencies quickly.
- Swap tests will be run against the deployed swap program later.
- An unfinished UI for Arbitrage Trading is mentioned, but it lacks some features and CSS styling.

# [14:30](https://youtu.be/XiA_pBftFt4?t=870) Introduction to Arbitrage Bot

Section Overview: The speaker introduces the concept of an Arbitrage bot and its purpose in evaluating liquidity pools for potential arbitrage opportunities.

## Design of the Arbitrage Bot

- The bot evaluates all possible pairings of liquidity pools offered mints.
- It looks for arbitrage opportunities between these pools based on differences in price.
- All combinations of assets within each pool are considered.
  
## Configuration Parameters
  
### Concurrency
  
- Determines how many assets at once should be checked for all combinations.
  
### Temperature
  
- Controls how aggressive the bot will be when placing trades.
- A higher temperature value triggers trades for smaller price differences.

# [18:12](https://youtu.be/XiA_pBftFt4?t=1092) Running Tests and Reviewing the ARB Program

Section Overview: The speaker reviews the deployed swap program and runs tests to ensure its functionality.

## Checking Swap Program Deployment

- The swap program has been successfully deployed.
- Anchor run test command is used to verify the functionality of the second swap program.

## Reviewing ARB Program

- The code for the Arbitrage bot is opened in VS Code.
- The liquidity is moved around using swaps to simulate different scenarios.
- The ARB program will evaluate these scenarios for arbitrage opportunities.
# [18:55](https://youtu.be/XiA_pBftFt4?t=1135) Introduction and Disclaimer

Section Overview: In this section, the speaker introduces the topic of building an Arbitrage bot using on-chain programs. They clarify that it is not necessary to write a program for this purpose and that there may be faster alternatives off-chain.

- Building an Arbitrage bot using on-chain programs is not mandatory.
- There might be faster alternatives to building an Arbitrage bot off-chain.

# [19:13](https://youtu.be/XiA_pBftFt4?t=1153) Entry Point

Section Overview: The speaker explains the entry point of the program and how it processes instructions.

- The entry point macro from Solana program is used to declare `process` as the entry point processor.
- Instructions are loaded from the data argument.
- If the instruction is "try Arbitrage," the program proceeds with processing Arbitrage. Otherwise, it throws an error.

# [19:28](https://youtu.be/XiA_pBftFt4?t=1168) Instruction Details

Section Overview: The speaker provides details about the "try Arbitrage" instruction.

- The instruction requires two swap program IDs and concurrency and temperature configs.
- This instruction triggers the program to search for an Arbitrage opportunity between two pools.

# [20:22](https://youtu.be/XiA_pBftFt4?t=1222) Processing Arbitrage

Section Overview: The speaker explains how accounts are read in and processed during Arbitrage.

- Accounts are read in by setting up an iterator over a slice of accounts.
- Proper order of accounts when passed into the program is crucial.
- Swap programs and pool PDAs are loaded, addresses are validated, and loops are run.
- Loops load token accounts for users, swap pool 1, swap pool 2, and mints based on concurrency value.

# [22:21](https://youtu.be/XiA_pBftFt4?t=1341) Serializing Partial Token Account State

Section Overview: The speaker discusses the purpose of serializing partial token account state.

- Serializing partial token account state helps maximize the number of accounts checked at once.
- Solana programs are limited to 200,000 compute units, and exceeding this limit halts program execution.
- By minimizing compute usage, more accounts can be processed within the limit.
# [24:46](https://youtu.be/XiA_pBftFt4?t=1486) Understanding the Return Type

Section Overview: In this section, the speaker explains the return type used in the code and how it is an aggregation of different fields. The use of lifetimes in the code is also mentioned.

## Return Type Explanation

- The return type is set up as an aggregation of fields in a tuple.
- The purpose of this return type is to make the code more readable, although lifetimes still pose a challenge.

# [25:04](https://youtu.be/XiA_pBftFt4?t=1504) Serialization with Bite Muck

Section Overview: This section focuses on the serialization process using a crate called Bite Muck. The speaker explains how Bite Muck allows direct interaction with buffer bytes and enables zero-copy serialization.

## Serialization Process with Bite Muck

- Bite Muck is used for interacting directly with buffer bytes.
- Zero-copy serialization means that changes made to a struct are reflected directly in the underlying bytes.
- Unlike traditional deserialization methods, which involve copying bytes into a data structure, partial serialization is performed by only serializing the required fields.
- A check is made to ensure that at least 72 bytes are available for serialization.
- If there are fewer than 72 bytes, an error is thrown.
- If there are at least 72 bytes, partial deserialization using Bite Muck is attempted by borrowing the first 72 bytes of account data.

# [26:22](https://youtu.be/XiA_pBftFt4?t=1582) Partial Deserialization and Validation

Section Overview: This section covers partial deserialization and validation of token accounts. The speaker explains how only specific fields are deserialized and validated before returning relevant account information.

## Partial Deserialization and Validation Process

- Partial deserialization using Bite Muck helps save computational resources when dealing with multiple accounts.
- For token accounts, only the first three fields need to be deserialized and validated.
- The owner of the account is checked to ensure it matches the expected value.
- If validation is successful, the account info, including the token account's mint, owner, and amount, is returned separately.
- This separation allows for efficient CPI calls and data checks.

# [27:44](https://youtu.be/XiA_pBftFt4?t=1664) Repeating Serialization Process

Section Overview: This section highlights how the serialization process is repeated for different types of accounts. The speaker emphasizes the benefits of partial deserialization in terms of computational efficiency.

## Repeating Serialization Process

- The same serialization process is applied to various types of accounts (e.g., user token accounts, swap token accounts).
- By partially deserializing multiple accounts, computational resources are saved.
- The process is repeated for each type of account within a loop.
- For mints, partial deserialization includes only the first two fields.
- However, due to limitations with Bite Muck, an additional u8 field cannot be included alongside a u64 field in a pod or zeroable type.
- To overcome this limitation, only the 32-byte Pub Key and 8-byte u64 fields are included as an option in partial mint State serialization.

# [29:06](https://youtu.be/XiA_pBftFt4?t=1746) Handling Additional Fields in Mint Serialization

Section Overview: In this section, the speaker explains why certain fields are not included in partial mint State serialization due to limitations with Bite Muck.

## Handling Additional Fields in Mint Serialization

- Including both a u8 and a u64 field together requires padding when using Bite Muck for serialization.
- To avoid this complication and make use of Bite Muck's capabilities effectively, only specific fields are included in partial mint State serialization.
- The first 40 bytes (32-byte Pub Key + 8-byte u64) are deserialized from the data buffer.
- The last byte is saved separately to account for the additional u8 field.
- This approach ensures efficient serialization while accounting for the necessary fields.

Note: The transcript provided does not include any further sections or timestamps.
# [30:59](https://youtu.be/XiA_pBftFt4?t=1859) Partial Deserialization and Optimization

Section Overview: The speaker discusses partial deserialization as a way to optimize compute. They explain that the account info for the mint and the decimals are returned in this process.

- Partial deserialization is used to save on compute.
- Account info for the mint and decimals is returned during partial deserialization.
- Optimization techniques are implemented to improve performance.

# [31:20](https://youtu.be/XiA_pBftFt4?t=1880) Introduction to Try Arbitrage

Section Overview: The speaker introduces the concept of try arbitrage and opens the "try Arbitrage" file. They mention setting up a struct to organize the arguments for the try Arbitrage function.

- The try Arbitrage function is introduced.
- A struct is used to organize the arguments for better readability.
- Token accounts, mints, payer, token program, system program, social token program, and configs are included as arguments.

# [31:43](https://youtu.be/XiA_pBftFt4?t=1903) Structuring Arguments in Try Arbitrage Function

Section Overview: The speaker explains how they structured the arguments in the try Arbitrage function using a struct. They highlight that each argument corresponds to specific elements mentioned earlier.

- Arguments in the try Arbitrage function are structured using a struct.
- The names of the arguments match with previously mentioned elements such as token accounts, mints, payer, etc.
- Using a struct helps maintain order and legibility of arguments.

# [32:03](https://youtu.be/XiA_pBftFt4?t=1923) Nested For Loop in Try Arbitrage Function

Section Overview: The speaker describes a nested for loop used in the try Arbitrage function. This loop checks all possible combinations of mint accounts by iterating through indexes I and J.

- A nested for loop is used to check all possible combinations of mint accounts.
- Indexes I and J are used to iterate through the accounts.
- R values for swap one and swap two are calculated for each iteration.

# [32:41](https://youtu.be/XiA_pBftFt4?t=1961) Checking for Arbitrage in Try Arbitrage Function

Section Overview: The speaker explains the process of checking for arbitrage in the try Arbitrage function. They mention calculating R values, checking their validity, and determining if an arbitrage opportunity exists.

- R values for swap one and swap two are calculated.
- A check is performed to ensure the validity of the R values.
- If everything checks out, a check for arbitrage is performed.

# [33:42](https://youtu.be/XiA_pBftFt4?t=2022) Invoking Arbitrage Trade

Section Overview: The speaker discusses invoking an arbitrage trade in the try Arbitrage function. They explain how instructions are set up using CPI invokes between swap one and swap two.

- Instructions are set up to invoke an arbitrage trade.
- CPI invokes are used between swap one and swap two.
- Indexes from nested loops determine the sequence of trades.

# [35:08](https://youtu.be/XiA_pBftFt4?t=2108) Check for Arbitrage Function

Section Overview: The speaker briefly covers the check for arbitrage function, which calculates percent differences between R values and determines whether a trade should be executed based on thresholds.

- The check for arbitrage function calculates percent differences between R values.
- It considers thresholds, such as temperature, to determine if a trade should be executed.
- If a trade is available, it triggers CPI invokes.

# [36:05](https://youtu.be/XiA_pBftFt4?t=2165) Reusing Functions from Swap Program

Section Overview: The speaker mentions reusing functions from the swap program in their current program. They highlight that both swaps run similar constant functions.

- Functions from the swap program are reused in the current program.
- Assumptions are made that both swaps run similar constant functions.
- This allows for code reuse and optimization.


# [36:48](https://youtu.be/XiA_pBftFt4?t=2208) Understanding the Concept of Asset Swapping

Section Overview: In this section, the speaker explains the concept of asset swapping and how it can be achieved using native and anchor programs.

## Asset Swapping with Anchor Programs

- To perform asset swapping, a swap instruction is placed in both the buy and sell transactions.
- By importing instructions into an anchor program using `anchor CPI context`, one can easily call them.
- If the crate of the anchor program is not publicly available, a new instruction can be created.
- The `build instruction data` function is used to generate swap instruction data for both buy and sell transactions.
- The `new` function with Borsch is used to serialize the data into a buffer for passing it as an argument.
- Account infos are mapped into account metas to include them in the instruction and invoke call.

## Building Instruction for an Anchor Program

- When building an instruction for an anchor program, it is necessary to use Borsch to serialize the data correctly.
- The instruction data consists of a 16-byte buffer containing the instruction discriminator and other relevant information.
- The hash of the global namespace for the program's instruction is used along with other bytes to create a 16-byte length array as instruction data.

# [37:26](https://youtu.be/XiA_pBftFt4?t=2246) Creating Instructions for Native Programs

Section Overview: This section focuses on creating instructions for native programs using specific data structures.

## Creating New Instructions

- To create new instructions for native programs, initialize arrays or variables required by those instructions.
- Use functions like `discriminator hash input` to determine the name of the new instruction.
- Convert relevant values into bytes using Borsch's serialization methods.
- Combine different byte arrays to form a 16-byte length array that represents the complete instruction data.

# [41:44](https://youtu.be/XiA_pBftFt4?t=2504) Simulating Transactions and Placing Arbitrage Trades

Section Overview: The speaker discusses the process of simulating transactions and placing arbitrage trades.

## Simulating Transactions

- Solana transactions are checked ahead of time through simulation.
- If a transaction fails during simulation, it will not be sent, saving transaction fees.
- By repeatedly simulating a transaction until it returns an "okay" value, one can ensure its success before proceeding.

## Placing Arbitrage Trades

- After successful simulation, an arbitrage trade can be placed using the `invoke Arbitrage` function.
# [43:28](https://youtu.be/XiA_pBftFt4?t=2608) Overview of the Program

Section Overview: The speaker discusses interesting information about the program itself, highlighting the use of native instead of anchor. The program is designed to be lighter.

## Client-Side Features and Functionality

- Utilizing partial state serialization.
- Implementing the constant product algorithm locally.
- Employing a deterministic order of accounts.
- Utilizing concurrency and temperature configs.
- Taking advantage of PreFlight checks.

# [44:11](https://youtu.be/XiA_pBftFt4?t=2651) Address Lookup Tables

Section Overview: The speaker introduces address lookup tables as a key component in making the program work efficiently.

- Address lookup tables are special accounts on Solana that function as hash maps.
- When building a transaction in Solana, all keys for involved accounts must be included, adding 32 bytes to the transaction size each time.
- Address lookup tables allow for including only the index of an address in a lookup table (a single byte number), reducing transaction size significantly.
- A hash map with u8 keys and 32-byte public key values can be used for efficient address lookups at runtime.
  
# [45:36](https://youtu.be/XiA_pBftFt4?t=2736) Runtime Behavior with Lookup Tables

Section Overview: The speaker explains how address lookup tables work at runtime and their impact on transaction size.

- When using a lookup table, the runtime will access the table instead of directly accessing addresses from transactions.
- By utilizing address lookup tables, significant reduction in transaction size can be achieved when multiple accounts are involved.
  
# [46:21](https://youtu.be/XiA_pBftFt4?t=2781) Using Address Lookup Tables

Section Overview: The speaker discusses how they plan to utilize address lookup tables in their program.

- Due to needing multiple accounts (including concurrency), using an address lookup table becomes necessary to minimize transaction size.
  
# [47:05](https://youtu.be/XiA_pBftFt4?t=2825) Deploying the Program

Section Overview: The speaker demonstrates the process of deploying the program on devnet.

- Building the Solana program using `cargo build`.
- Deploying the program to devnet using `solana program deploy`.
  
# [47:38](https://youtu.be/XiA_pBftFt4?t=2858) Creating Address Lookup Table

Section Overview: The speaker explains how to create an address lookup table and its configuration.

- Using web3js, a function called `create address lookup table` is used to create a lookup table.
- A transaction v0 is built without a lookup table, while providing optional config for an address lookup table when needed.
  
# [49:00](https://youtu.be/XiA_pBftFt4?t=2940) Benefits of Address Lookup Tables

Section Overview: The speaker highlights the benefits of utilizing address lookup tables in terms of space efficiency.

- By converting multiple accounts into u8 indexes within address lookup tables, significant space can be saved.
- Packing numerous accounts into lookup tables can greatly reduce transaction size.
# [49:38](https://youtu.be/XiA_pBftFt4?t=2978) Preparing Tokens and Assets

Section Overview: In this section, the speaker discusses the initial steps required before performing the swapping process. This includes ensuring that there are enough tokens in the token account for swapping and updating the assets JSON file.

## Checking Token Account and Updating Assets JSON

- Before starting the swapping process, it is important to have enough tokens in the token account.
- The assets JSON file needs to be updated by replacing a specific entry with one from the swap program.
- This step ensures that the necessary mints are present for minting tokens.

# [50:01](https://youtu.be/XiA_pBftFt4?t=3001) Minting Tokens and Gathering Token Accounts

Section Overview: This section focuses on minting tokens and gathering all token accounts required for arbitrage trading.

## Minting Tokens

- To have enough tokens for placing arbitrage trades, it is necessary to mint some of these tokens.
- By minting tokens, there will be a sufficient supply available for trading purposes.

## Gathering Token Accounts

- In addition to minting tokens, all token accounts need to be gathered.
- The pool address can be obtained using a function called "get pool address."
- The speaker mentions using an assets JSON file instead of querying the pool directly.
- All token accounts are aggregated into lists based on concurrency value.

# [51:04](https://youtu.be/XiA_pBftFt4?t=3064) Creating Lookup Table and Extending Address Lookup Table

Section Overview: This section covers creating a new lookup table and extending the address lookup table with public keys.

## Creating Lookup Table

- After having all necessary accounts ready, a new lookup table is created.
- An inline extend function is used to extend the address lookup table with every public key.

## Extending Address Lookup Table

- The address lookup table is extended by adding 11 token account addresses for swap one, swap two, and the mints.
- The speaker mentions the possibility of adding other accounts as well.

# [52:06](https://youtu.be/XiA_pBftFt4?t=3126) Adding Keys to Lookup Table

Section Overview: This section explains how to add new keys to the lookup table using an instruction from the program.

## Adding Keys to Lookup Table

- An instruction is used to add new keys to the lookup table.
- A list of addresses is passed as a parameter to extend the lookup table with these keys.

# [53:10](https://youtu.be/XiA_pBftFt4?t=3190) Building Transaction and Resolving Indexes

Section Overview: This section discusses building a transaction and resolving indexes for keys in the address lookup table.

## Building Transaction

- To build a transaction, keys are pushed into an instruction using "Keys push" statements.
- The address lookup table is not explicitly included in this process.

## Resolving Indexes

- The address for the lookup table is included in the compiled v0 message function call.
- Indexes of keys in the address lookup table are automatically resolved during execution.

# [54:26](https://youtu.be/XiA_pBftFt4?t=3266) Sending Arbitrage Instruction and Iterative Looping

Section Overview: This section covers sending an arbitrage instruction and implementing an iterative loop on both client-side and program-side.

## Sending Arbitrage Instruction

- An instruction for performing arbitrage is created and sent using a function called "send Arbitrage instruction."
- A logging mechanism is set up to handle trade errors during execution.

## Iterative Looping

- A loop is implemented on the client-side to iteratively go through a list based on concurrency value.
- The size of concurrency determines how many combinations need to be processed by the program-side.
# [55:50](https://youtu.be/XiA_pBftFt4?t=3350)

Section Overview: In this section, the speaker discusses setting up a lookup table on devnet for arbitrage trading. They also mention adding addresses to the lookup table and demonstrate placing trades between swap pools. The speaker encourages viewers to try building their own arbitrage bot.

## Creating a Lookup Table and Placing Trades

- A lookup table is created on devnet for arbitrage trading. (t=3350s)
- Addresses are added to the lookup table, with a total of 44 addresses ranging from 0 to 43. (t=3350s)
- Arbitrage trades are placed between two swap pools using the lookup table. (t=3350s)
- The transaction size is printed out, showing a smaller number when using the lookup table compared to without it. (t=3370s)

## Benefits and Considerations

- Using a lookup table helps optimize arbitrage trading by reducing transaction size. (t=3370s)
- However, pushing the maximum size of a uint8 array can cause errors. (t=3370s)

## Encouragement to Build Your Own Arbitrage Bot

- The speaker highlights that setting up an arbitrage bot can be fun and encourages viewers to try building their own. (t=3388s)
- Various optimizations, such as using byte marks, can be explored during the process. (t=3388s)
- Viewers are encouraged to test their bots on Main net and see if they can make some profit. (t=3405s)

# [57:00](https://youtu.be/XiA_pBftFt4?t=3420)

Section Overview: In this concluding section, the speaker wraps up by expressing their enjoyment in building an arbitrage bot and suggests trying it out for oneself.

## Final Thoughts

- Building an arbitrage bot has been a fun experience for the speaker. (t=3405s)
- The speaker suggests trying out the bot on Main net and seeing if it can generate some profit. (t=3420s)
- The video concludes with a farewell message, indicating that more content will be available in the future. (t=3420s)

[Generated with Video Highlight](https://videohighlight.com/video/summary/XiA_pBftFt4)
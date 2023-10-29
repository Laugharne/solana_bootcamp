# [00:00](https://youtu.be/s8kMrMi3J5g?t=0) Introduction and Overview

Section Overview: In this section, the speaker introduces the topics to be covered in the tutorial, including Clockwork threads, randomness, zero copy, and a C battle on the Seven Seas program.

## Turning on the Wind on the Seven Seas
- The speaker mentions that in previous days, participants were able to stake their gold and equip their ships with cannons.
- The ship is deployed and an avatar is chosen.
- When the wind is resumed, all ships on the map start moving automatically due to a Clockwork thread.

## Clockwork Threads
- Clockwork threads are used to trigger transactions automatically based on certain triggers.
- A worker network listens for these triggers and calls transactions when necessary.
- Different triggers can be used such as crown notation (e.g., firing at 12 noon every day), specific slots or epochs, timestamps, or using an Oracle for price changes.
- Examples of use cases for Clockwork threads include recurring payments, token distribution, dollar cost averaging, and subscriptions.

## Idle Game Example
- The speaker suggests exploring an idle game example provided in Solana's game starter kits.
- Instructions are given to open the idle game folder in Visual Studio, install npm packages, build Anchor, and test the program.

# [02:30](https://youtu.be/s8kMrMi3J5g?t=150) How Clockwork Threads Work

Section Overview: This section provides an explanation of how Clockwork threads function.

## Creating a Thread
- To create a Clockwork thread:
  - Create a thread that calls a specific instruction in your program repeatedly based on certain triggers.
  - The worker network listens for these triggers and executes transactions accordingly.
  - Each instruction costs 1000 lampards.

## Triggering Threads
- Triggers can be set based on various conditions:
  - Account changes: Triggered when a certain account changes.
  - Crown notation: Allows for triggering at specific times of the day.
  - Slots, epochs, or timestamps: Triggered at specific slots, epochs, or timestamps.
  - Oracle: Can be used to listen for price changes or other events.

## Use Cases
- Clockwork threads can be used for various purposes:
  - Recurring payments
  - Token distribution
  - Dollar cost averaging
  - Listening to price changes for buying/selling decisions
  - Subscriptions

# [05:07](https://youtu.be/s8kMrMi3J5g?t=307) Examples and Use Cases

Section Overview: This section provides examples and additional use cases for Clockwork threads.

## Example Use Cases
- Hello Clockwork example: A basic example demonstrating how Clockwork works.
- Counter example: Counts up a value using Clockwork threads.
- Recurring payments: Used to automate recurring payments.
- Dollar cost averaging: Automates regular token purchases at set intervals.
- Serum crank: Utilizes Clockwork threads in a Serum-based application.
- Subscriptions: Automatically transfers tokens on a recurring schedule.

# [06:17](https://youtu.be/s8kMrMi3J5g?t=377) Idle Game Example Setup

Section Overview: This section provides instructions on setting up the idle game example.

## Setting Up the Idle Game Example
- Open the idle game folder in Visual Studio Code.
- Install npm packages and build Anchor.
- Test the program in CDF by installing the necessary packages.

Note that this summary is based solely on the provided transcript and may not capture all details from the video.
# [07:06](https://youtu.be/s8kMrMi3J5g?t=426) Initializing the Game

Section Overview: The speaker discusses how to initialize the game and explains the various functions available in the game.

## Game Initialization

- The game account is created and approved.
- A thread is running, providing one word every 10 seconds.
- Functions include upgrading teeth, buying a new Lumberjack, and trading wood for gold.

# [07:31](https://youtu.be/s8kMrMi3J5g?t=451) Upgrades and Functions

Section Overview: The speaker explains the effects of buying another Lumberjack and upgrading teeth in the game.

## Upgrades and Functions

- Buying another Lumberjack increases votes per 10 seconds.
- Upgrading teeth improves wood-to-gold conversion rate.
- The thread can be stopped at any time.

# [07:54](https://youtu.be/s8kMrMi3J5g?t=474) Game Data Structure

Section Overview: The speaker introduces the structure of the game data account and its important components.

## Game Data Structure

- The game data account holds information for each player.
- Components include authority, Lumberjacks, gold, teeth upgrades, and last update time.
- Last update time is crucial for calculating time until next update in the client.

# [08:18](https://youtu.be/s8kMrMi3J5g?t=498) Time Calculation

Section Overview: The speaker explains how to calculate time until the next update based on last update time.

## Time Calculation

- Current time minus last updated time gives the remaining time until next update.
- Updates occur every 10 seconds when triggered by a tick from the thread.
- Error codes, wood requirements, gold conversion rates, teeth multiplier upgrades are defined constants.

# [08:35](https://youtu.be/s8kMrMi3J5g?t=515) Thread Configuration

Section Overview: The speaker discusses thread configuration parameters such as tick time and authority.

## Thread Configuration

- Thread tick time is set to 10 seconds.
- PDA (Program Derived Address) and seed are defined for game data.
- The thread authority is the player's own authority, allowing control over starting, stopping, or pausing the thread.

# [09:19](https://youtu.be/s8kMrMi3J5g?t=559) Game Initialization Process

Section Overview: The speaker explains the process of initializing the game and creating the game data account.

## Game Initialization Process

- The game data account is created using a normal PDA.
- Initial values for player position, Lumberjacks, upgrades, and updated add time are set.
- Current Unix timestamp is used as the updated add time value.

# [09:57](https://youtu.be/s8kMrMi3J5g?t=597) Importing Clockwork SDK

Section Overview: The speaker demonstrates how to import and use the Clockwork SDK in the program.

## Importing Clockwork SDK

- The Clockwork SDK is imported into the program.
- It is added as a dependency in project settings.

# [10:16](https://youtu.be/s8kMrMi3J5g?t=616) Thread Instruction Creation

Section Overview: The speaker explains how to create instructions for triggering thread ticks.

## Thread Instruction Creation

- Instructions are created for thread tick triggers.
- A CPI (Cross Program Invocation) call is made to the Clockwork program using worker network.
- On each thread tick (every 10 seconds), wood amount increases based on Lumberjack count and updated add time is set in game data account.

# [11:02](https://youtu.be/s8kMrMi3J5g?t=662) Trigger Configuration

Section Overview: The speaker discusses trigger configuration parameters and costs associated with running threads.

## Trigger Configuration

- Crown trigger type is used with specified thread tick time in seconds.
- Triggers can be skipped by players if they want to stop their threads.
- Running threads can be expensive due to lamports cost per instruction execution.

# [11:43](https://youtu.be/s8kMrMi3J5g?t=703) Thread Creation

Section Overview: The speaker explains the process of creating a new thread using CPI to the Clockwork program.

## Thread Creation

- A CPI call is made to the Clockwork program for thread creation.
- Context, accounts (including system program), and seeds are provided.
- Signers are defined as thread seeds.

# [12:25](https://youtu.be/s8kMrMi3J5g?t=745) Conclusion and Final Steps

Section Overview: The speaker concludes the explanation of thread creation and provides final steps.

## Conclusion and Final Steps

- The instruction for triggering thread ticks is ready.
- The trigger type is crown with specified tick time in seconds.
- CPI call is made to create the thread using context, accounts, and seeds.
- Thread creation can be costly, so consider cost implications when running threads frequently.
# [13:32](https://youtu.be/s8kMrMi3J5g?t=812) Cheating the System

Section Overview: The speaker discusses how to cheat the system by maximizing instructions and triggers in Clockwork. This method is easier than randomness.

## Cheating the System

- By adding as many instructions as possible and using triggers, it is possible to cheat the system in Clockwork.
- This approach is straightforward and simpler compared to implementing randomness.
- Clockwork offers a variety of possibilities for creating instructions.

# [13:52](https://youtu.be/s8kMrMi3J5g?t=832) Trading Wood for Gold

Section Overview: The speaker explains how to trade wood for gold in Clockwork, allowing players to acquire more resources.

## Trading Wood for Gold

- With 40 units of wood, players can trade some of it for gold.
- By obtaining 25 gold, another lumberjack can be purchased.
- Having two lumberjacks allows players to generate two gold every five seconds.
- The process of trading wood for gold is demonstrated in the Seven C's program.

# [14:21](https://youtu.be/s8kMrMi3J5g?t=861) Using Threads in Seven C's Program

Section Overview: The speaker demonstrates how threads are used in the Seven C's program, showcasing similarities and differences compared to Idle Game.

## Threads in Seven C's Program

- In the Seven C's program, there are instructions such as star thread, pause thread, and resume thread.
- The star thread instruction functions similarly to what was seen in Idle Game, creating a threaded tick account with a trigger that occurs every two seconds instead of ten seconds.
- The thread authority belongs to the program rather than the player in this case.

# [15:03](https://youtu.be/s8kMrMi3J5g?t=903) Moving Players on the Board

Section Overview: The speaker explains how players are moved on the board within threads using specific functions and conditions.

## Moving Players on the Board

- The "on thread tick" function is called when a thread ticks.
- Within this function, players on the board are identified and stored in a vector.
- Each live player's direction is determined, and if the new board state is empty, the player is moved to that position.
- The previous state of the tile where the player was located is set to empty.

# [16:14](https://youtu.be/s8kMrMi3J5g?t=974) Dynamic Threads and Collecting Gold

Section Overview: The speaker mentions the possibility of dynamic threads in Clockwork and discusses collecting gold from chests.

## Dynamic Threads and Collecting Gold

- Dynamic threads allow for passing dynamic data into threads, but it requires further research and exploration.
- In the current implementation, players stop when they reach another ship or chest since their token account is not accounted for.
- If someone wants to automate ships collecting gold from chests, it would be an interesting challenge.

# [17:11](https://youtu.be/s8kMrMi3J5g?t=1031) Importance of Randomness in Games

Section Overview: The speaker emphasizes the significance of randomness in games, particularly gambling games like coin flips or card games.

## Importance of Randomness in Games

- Randomness plays a crucial role in games, especially gambling games like coin flips or card-based games.
- Implementing randomness on-chain can be challenging due to public visibility and potential exploitation by players trying to manipulate outcomes.

# [17:57](https://youtu.be/s8kMrMi3J5g?t=1077) XOR Shift as a Randomness Method

Section Overview: The speaker introduces XOR Shift as a method for generating random values with low computational cost.

## XOR Shift as a Randomness Method

- XOR Shift is a mathematical function used for generating random values based on a seed value.
- It involves bit shifting operations to produce new random values each time it is called.
- This method is commonly used in gaming applications due to its simplicity and efficiency.
- In Seven C's, XOR Shift is used for tasks such as determining ship positions and calculating damage.

# [19:08](https://youtu.be/s8kMrMi3J5g?t=1148) Limitations of XOR Shift and Usage in Seven C's

Section Overview: The speaker discusses the limitations of XOR Shift and its usage in the Seven C's program.

## Limitations of XOR Shift and Usage in Seven C's

- XOR Shift may not meet all statistical randomness tests, but it can be improved by implementing variations.
- The speaker mentions that JavaScript 8 in Chrome uses XOR Shift 1024 for random number generation.
- In Seven C's, XOR Shift is utilized for determining the damage inflicted by Cthulhu, adding randomness to the base damage value.

# [19:34](https://youtu.be/s8kMrMi3J5g?t=1174) Adding Randomness to Damage Calculation

Section Overview: The speaker demonstrates how randomness is incorporated into damage calculation using XOR Shift in Seven C's.

## Adding Randomness to Damage Calculation

- In the example shown, a new instance of XOR Shift is created.
- The base damage value for Cthulhu is set at 10.
- A portion (30%) of this base damage (3) is obtained.
- Randomness is added to the calculated damage using modulo with the damage variant plus one.
- This ensures that each time Cthulhu attacks, there is some variation in the inflicted damage.
# [20:21](https://youtu.be/s8kMrMi3J5g?t=1221) Spawning Ships and Predictable Positions

Section Overview: The spawning of ships in the game is based on the number of items on the board, resulting in predictable positions for new ships. This predictability allows for easy testing.

## Spawning Mechanism

- Ships always spawn in the same position when there are already two ships on the board.
- The number of items on the board determines the position of the next ship.
- This predictability facilitates writing tests for ship spawning.

# [20:38](https://youtu.be/s8kMrMi3J5g?t=1238) Implementing XR Shift for Randomness

Section Overview: An alternative implementation called XR Shift is used to introduce randomness into the game. It involves multiplying a u64 by a u128 and then cutting off unnecessary bits.

## XR Shift Implementation

- XR Shift uses different values and multiplies a u64 by a u128.
- Unnecessary bits are then removed from the result.
- This implementation provides more statistical variation but requires additional compute power and memory.

# [21:02](https://youtu.be/s8kMrMi3J5g?t=1262) Combining Randomness with Block Hash or Slot

Section Overview: Randomness can be combined with either the current block hash or slot to generate a more random value that is not related to fixed values.

## Combining Randomness Sources

- The randomness value can be combined with either the current block hash or slot.
- Using these sources ensures a more random outcome.
- The seat for randomness can be obtained by passing in either the current slot or block hash modulo Max value desired.

# [21:26](https://youtu.be/s8kMrMi3J5g?t=1286) Security Considerations for Randomness

Section Overview: While random values generated using block hash or slot are statistically random, they may not be 100% secure. Malicious validators could potentially exploit predictable block hashes to attack the randomness value.

## Security Risks

- Malicious validators could manipulate the block to create a specific block hash structure.
- Exploiting predictable block hashes has occurred in the past, leading to exploits in games and other applications.
- Relying solely on block hash or slot for randomness is not recommended when significant amounts of money are involved.

# [22:09](https://youtu.be/s8kMrMi3J5g?t=1329) Using Hashing Functions for Randomness

Section Overview: Hashing functions can be used as an alternative source of randomness. They provide a high level of randomness but still have some security considerations.

## Utilizing Hashing Functions

- Hashing functions are highly random and can be used as a source of randomness.
- The slot or block hash can be hashed, and the first few bytes can be converted into u64 for generating random values.
- While hashing functions offer good randomness, they may not provide 100% security against attacks.

# [22:29](https://youtu.be/s8kMrMi3J5g?t=1349) Limitations of Block Hash and Slot Randomness

Section Overview: Block hash and slot-based randomness have limitations in terms of security. Although unlikely, malicious validators could exploit predictable block hashes to manipulate random outcomes.

## Exploitation Risks

- Malicious validators could collude with switchboard Oracle providers to break the randomness system.
- Historical examples include exploits in games like Trash Pandemic and Cope Roulette where attackers predicted the next random value.
- When significant amounts of money are at stake, relying solely on block hash or slot for randomness is not advisable.

# [23:22](https://youtu.be/s8kMrMi3J5g?t=1402) Partial Solution: Using an Oracle for Randomness

Section Overview: To enhance security, using an Oracle such as Switchboard can provide a more secure source of randomness by requesting random values from an external entity.

## Using an Oracle for Randomness

- Oracles like Switchboard can be used to request random values.
- The Oracle provides a random value that can be used in the program.
- This approach adds an extra step and complexity to the randomness generation process.

# [23:48](https://youtu.be/s8kMrMi3J5g?t=1428) Collusion Risks with Oracle-based Randomness

Section Overview: While using an Oracle for randomness improves security, there is still a small risk of collusion between malicious validators and Oracle providers.

## Collusion Risks

- Malicious validators working with switchboard Oracle providers could potentially break the randomness system.
- Although this risk exists, using an Oracle is still more secure than relying solely on block hash or slot for randomness.

# [24:19](https://youtu.be/s8kMrMi3J5g?t=1459) Implementation of Switchboard Oracle

Section Overview: The implementation of the Switchboard Oracle is explored, providing a practical example of how it can be used for generating random values.

## Implementation Details

- The video provides resources for implementing a Rust program that includes various randomness functions.
- A coin flip example using the Switchboard implementation is demonstrated.
- Additional resources and tutorials are provided for further exploration.

# [25:03](https://youtu.be/s8kMrMi3J5g?t=1503) Considerations for Secure Randomness Usage

Section Overview: When significant amounts of money depend on random values, it is crucial to research and implement secure methods to ensure fairness and prevent exploitation.

## Secure Usage Considerations

- Various hacks and workarounds exist, such as using other Oracles or obtaining current soil prices from Pith.
- Extensive research is necessary when dealing with high-stakes scenarios reliant on random values.
# [27:13](https://youtu.be/s8kMrMi3J5g?t=1633) Implementing the Lip RS File

Section Overview: In this section, the speaker discusses how to implement the Lip RS file using the Switchboard SDK. They mention that they are currently using version 0.123 of Switchboard V2.

## Implementing the Lip RS File

- The Lip RS file is obtained from the Switchboard SDK in the Cargo terminal.
- The speaker mentions that there is a Switchboard V2 and they are currently using version 0.123.

# [27:31](https://youtu.be/s8kMrMi3J5g?t=1651) Initializing the Game

Section Overview: This section focuses on initializing the game and explains various parameters involved in setting up different types of games.

## Initializing the Game

- To initialize the game, they start a bump and a rear F switchboard key.
- The maximum result is saved, which in their case is set to two.
- The speaker provides examples of how to set different max results for different games (e.g., 10 for a 10-sided dice roll gambling or 52 for a card game).
  
# [27:53](https://youtu.be/s8kMrMi3J5g?t=1673) Requesting Randomness

Section Overview: Here, the speaker explains how to request randomness and describes important accounts involved in this process.

## Requesting Randomness

- To request randomness, they transfer 0.1 soil into a PDA (Program Derived Address).
- The state is set based on what the player guessed (e.g., one or zero for coins or heads/tails).
- The result is initially set to zero.
- A large randomness request is made involving several important accounts:
    - Oracle queue
    - VIF account
    - Authority of VRF account
    - Data buffer account
    - Permissions
    - Escrow account funded by Repsol from player to pay for fees
    - Player wallet authority
    - Recent blockhash
    - Program state from the game
    - Token program for interaction with Repsol

# [28:21](https://youtu.be/s8kMrMi3J5g?t=1701) Randomness Accounts and Functionality

Section Overview: The speaker provides an overview of various accounts involved in randomness functionality.

## Randomness Accounts and Functionality

- The speaker explains the purpose of different accounts:
    - Oracle queue: Provides random values.
    - Q Authority: Authority for the queue.
    - Data buffer account: Contains data related to randomness.
    - Escrow account: Funded by Repsol from the player to pay for fees.
- The speaker mentions that understanding this process can be complicated, but it is necessary when money is involved. They also mention a potential easier random function being developed by Clockwork using their worker network.

# [29:10](https://youtu.be/s8kMrMi3J5g?t=1750) Additional Accounts and Usage

Section Overview: This section covers additional accounts involved in the randomness process and their usage.

## Additional Accounts and Usage

- The speaker discusses more accounts related to randomness:
    - Player key (seeds)
- They invoke a signed randomness function, which involves a CPI (Cross-Program Invocation) from Switchboard back into their program.
- They check if the VF account contains a random value. If it's empty, there is no randomness result.
- The game state includes the maximum result parameter.
- Depending on whether they won or not, they transfer soil to the player.

# [31:01](https://youtu.be/s8kMrMi3J5g?t=1861) Coin Flip Game Example

Section Overview: In this section, the speaker demonstrates how to build a coin flip game using randomness functionality.

## Coin Flip Game Example

- After explaining all the randomness functions and accounts, they proceed to build a coin flip game as an example.
- The speaker mentions that all the accounts have comments and detailed explanations, making it easier to understand and use in one's own program.

# [31:56](https://youtu.be/s8kMrMi3J5g?t=1916) Zero Copy and Big Accounts

Section Overview: This section introduces zero copy and big accounts, which will be explored further in the next tutorial.

## Zero Copy and Big Accounts

- The speaker mentions that they will now discuss zero copy and big accounts.
- They refer to a playground tutorial where these concepts are explained in detail.
- A local validator is needed for this tutorial, which can be started using "Solana test validator" command.
- They demonstrate how to connect to the local validator through the playground interface.

# [32:43](https://youtu.be/s8kMrMi3J5g?t=1963) Deploying and Testing Zero Copy Example

Section Overview: This section covers deploying and testing the zero copy example from the playground tutorial.

## Deploying and Testing Zero Copy Example

- The speaker explains how the web platform works by sending code to a server for building before returning the result.
- They deploy the zero copy example, mentioning a warning about potential stack size limitations.
- Running tests reveals an error related to hitting the stack size limit, indicating a need for more stack space.

Note: Due to limited information provided in this transcript, further details about zero copy and big accounts are not available.
# [34:02](https://youtu.be/s8kMrMi3J5g?t=2042) Account Size Limits

Section Overview: In this section, the speaker discusses the size limits for Solana accounts and how they can be exceeded.

## Account Size Limits

- Solana accounts have a maximum size limit of 10 gigabytes.
- The account size is limited by the amount of memory that can be allocated during a cross-program invocation (CPI) to create or increase the size of an account.
- The anchor framework creates an account and performs a CPI in the background when interacting with Solana.
- If an account exceeds the stack size limit, it can be boxed to allocate more space on the heap.

# [35:01](https://youtu.be/s8kMrMi3J5g?t=2101) Running Out of Stack Size

Section Overview: This section explains how running out of stack size can cause errors and demonstrates how to solve this issue.

## Running Out of Stack Size

- When an account hits the stack size limit, it results in errors such as exceeding timeouts.
- To demonstrate this issue, a test is run where an account is initialized with a struct that exceeds the stack size limit.
- The struct used for initialization has 10 kilobytes of data, including four public keys with each key having 32 kilobytes.
- To solve this problem, boxing the account is recommended. Boxing involves creating a pointer on the stack that points to data stored on the heap, allowing for more space.

# [37:43](https://youtu.be/s8kMrMi3J5g?t=2263) Increasing Account Size

Section Overview: This section explains how to increase account sizes beyond their initial limits using anchors.

## Increasing Account Size

- Anchors provides a function that allows direct use of data passed into instructions for initializing structs.
- By passing in new sizes through instruction data, accounts can be increased in size beyond their initial limits.
- The payer and real lock are specified as signers for reallocating accounts.
- Increasing account sizes incurs additional costs, with a 10 kilobyte account costing around 0.07 Sol.

# [40:01](https://youtu.be/s8kMrMi3J5g?t=2401) Account Size Limitations

Section Overview: This section discusses the limitations of account sizes and potential issues when exceeding them.

## Account Size Limitations

- Accounts can be created up to 10 megabytes in size.
- Larger accounts may hit the heap size limit, which is set at 32 kilobytes.
- If an account exceeds both the stack and heap size limits, it will need to be boxed and stored on the heap.
- Increasing account sizes beyond their initial limits incurs additional costs.
- It is important to consider these limitations when working with larger accounts in Solana.

Note: The transcript provided does not contain any timestamps for some sections.
# [40:48](https://youtu.be/s8kMrMi3J5g?t=2448) Understanding Zero Copy Accounts

Section Overview: In this section, the speaker discusses the concept of zero copy accounts and how they can be used to overcome memory limitations in runtime.

## Zero Copy Accounts

- Zero copy accounts allow for efficient memory usage by only loading a pointer to a certain amount of memory instead of loading the entire account.
- By using mem copy operations, developers can directly interact with this memory.
- Adding the flag "zero copy" and specifying the wrap type (e.g., C) enables the use of zero copy accounts.
- Different wrap types are available, but it's important to consider their impact on options and enums.

# [41:11](https://youtu.be/s8kMrMi3J5g?t=2471) Implementation of Zero Copy Accounts in Seven Seas Program

Section Overview: The speaker explains how zero copy accounts are implemented in the Seven Seas program, specifically focusing on the game data account.

## Game Data Account Structure

- The game data account in Seven Seas is a zero copy account.
- It contains a two-dimensional array representing a 10x10 tile board.
- Each tile is represented by a zero copy struct containing various attributes such as current player, state of the tile, health, damage, range, collect reward, and Avatar Pub Key (NFT).

# [42:10](https://youtu.be/s8kMrMi3J5g?t=2530) Importance of Start Health in Zero Copy Account

Section Overview: The speaker highlights the significance of start health in the game data account and its relevance to individual player ships.

## Start Health Consideration

- The start health attribute is crucial because each player ship may have different starting health based on acquired tokens or other factors.
- By saving start health in the zero copy account, clients can calculate and display accurate health information during gameplay.

# [43:22](https://youtu.be/s8kMrMi3J5g?t=2602) Building the Seven Seas Program

Section Overview: The speaker explains the process of building the Seven Seas program, including different client options.

## Multiple Clients in Seven Seas Program

- The Seven Seas program supports multiple clients, including a JavaScript client and a Unity WebGL client.
- The JavaScript client is still under development and has limited functionality compared to the more visually appealing Unity WebGL client.

# [44:28](https://youtu.be/s8kMrMi3J5g?t=2668) Interacting with the Game in Different Clients

Section Overview: The speaker demonstrates how both the JavaScript and Unity WebGL clients can interact with the same game program.

## Client Interaction

- Both the JavaScript and Unity WebGL clients can connect to the game program.
- Players can log in using their preferred wallet or backpack.
- The game representation is synchronized between both clients, allowing for seamless gameplay experience across platforms.

# [45:27](https://youtu.be/s8kMrMi3J5g?t=2727) Features of Seven Seas Program

Section Overview: The speaker provides an overview of various features implemented in the Seven Seas program.

## Feature Highlights

- Zero copy board account with a two-dimensional array representing tiles on a grid.
- On-chain movement functionality that allows players to move their ships within the game board.
- Collecting chests and transferring rewards (Soul tokens, gold tokens) to players who collect them.
- Killing enemy ships to gain Soul tokens and gold tokens.

Note: Due to limitations on bullet points per section, not all features are covered. Please refer to the full transcript for complete details.
# [47:14](https://youtu.be/s8kMrMi3J5g?t=2834) Pirate NFT and Ship Upgrades

Section Overview: In this section, the speaker explains how Pirate NFTs work and how ship upgrades are implemented using PDAs (Program Derived Accounts) and SPL tokens.

## Pirate NFTs and Ship Levels

- A PDA is created for each spawned ship, with the mint of the NFT serving as a unique identifier.
- The ship starts at level zero, and a PDA saves the current ship level.
- Upgrading the ship is done by using gold tokens to upgrade the PDA.

## Saving Data on NFTs

- Any NFT can have data saved on it by deriving a PDA from its mint.
- The ship is upgraded using SBL tokens for damage and health.
- Token accounts of players are checked when spawning a ship to determine available cannons and extra health.

## Cannons, Damage, and Health

- Cannons obtained from Canon tokens in the player's token account are used to calculate extra damage.
- The number of cannons determines the additional damage inflicted by the ship.

# [48:10](https://youtu.be/s8kMrMi3J5g?t=2890) Features: Auto Approve Wallet, Clockwork Weather Effects, NFT Avatars

Section Overview: This section covers various features in the game including auto approve wallets, clockwork weather effects, and NFT avatars.

## Auto Approve Wallet

- An auto approve wallet allows for seamless transactions within the game.
- More details about auto approve wallets will be discussed in subsequent slides.

## Clockwork Weather Effects

- Clockwork weather effects were previously mentioned but not elaborated on further.

## NFT Avatars

- Players can select an NFT as their character/avatar in the game.
- The selected NFT avatar appears on their deployed ship.

# [49:19](https://youtu.be/s8kMrMi3J5g?t=2959) Animations via Game Action Account

Section Overview: This section explains how animations are implemented in the game using a game action account.

## Implementing Animations

- To show animations to clients, a new account is created called the "game action account."
- Whenever an action occurs in the game, a corresponding game action is created.
- Examples of game actions include shooting and taking damage.

# [50:08](https://youtu.be/s8kMrMi3J5g?t=3008) Surprise Cthulhu Attack

Section Overview: The speaker mentions a surprise Cthulhu attack that will be discussed further in the next session.

## QR Code Activation

- Players will be able to scan a QR code to trigger an attack by a big monster on the side of the map.
- This attack will be facilitated through Solana patrons' action request.

# [50:48](https://youtu.be/s8kMrMi3J5g?t=3048) Auto Approve Wallet Options

Section Overview: This section explores different options for implementing auto approve wallets in the game.

## In-Game Wallet with Soil Transfer

- Upon deploying a ship, a small amount of SOL (Soil) is transferred into an in-game wallet.
- This wallet is used to pay for transaction fees within the game.
- Players can withdraw this amount or manually add more SOL if desired.

## Other Auto Approve Wallet Options

- Gum session keys: A video explaining gum session keys and their implementation is provided as additional resources.
- Burner key pair: Similar to what was done in Seven Seas program.
- Solflare wallet: Offers auto proof functionality per app but has security concerns.

# [52:09](https://youtu.be/s8kMrMi3J5g?t=3129) Seeking Solutions for Auto Approve Wallets

Section Overview: The speaker discusses ongoing efforts and potential solutions for auto approve wallets.

## Clockwork's Solution Proposal

- Clockwork is working on potential solutions to facilitate auto approve wallets but it remains an unsolved problem.
- Collaboration and contributions from developers are encouraged to improve this aspect of the ecosystem. 

# [52:53](https://youtu.be/s8kMrMi3J5g?t=3173) Conclusion and Farewell

Section Overview: The speaker concludes the session and invites participants to engage in a final activity.

## Final Activity: Sea Battle

- Participants are invited to log in and engage in a sea battle.
- Wind effects can be activated to observe their impact on gameplay.
- Resources, including the link to the session keys video, are provided for further reference.

Note: The transcript is already in English.

[Generated with Video Highlight](https://videohighlight.com/video/summary/s8kMrMi3J5g)
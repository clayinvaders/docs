# Explore

### Description

There are 5 discover missions per epoch, 1 per day

### Objective

Discover new Elements & Knowledge

### Main Actors

Explorer, Engineer & Doctor

### Gameplay

* When epoch start
  * **Crew Explorers** receive a notification to inform them they are **in charge** of the **Explore Mission**
*   Once per day

    * **Crew Explorers** receive a notification **asking** for a new **coordinate** to explore, and the type of exploration (Elements or Knowledge)
    * **Crew Explores** set the **coordinates** for the mission
    * At least **1 Engineer & 1 Doctor** start the mission

    `/ci-game start-exploration`

    * **Space Unit** **Members** **vote** on the action to choose (DISCORD pool)
    * The mission **start**
      *   Element founds

          * **All Space Unit Members** set the contribution for the mission

          `/ci-game set collect-element`
      *   Knowledge found

          * **All Space Unit Members** set the contribution for the mission

          `/ci-game set collect-knowledge`
      * Randomly, the users in the SpaceUnit receive small missions to complete:&#x20;
        * (v1) DISCORD bot messages with puzzles
        * (v2) Web Minigame link to play
      * Randomness (coordinates deviation)
        * Blockchain Random seed
        * Fulfilled Crew vs. Available Roles
        * Number of Passengers
        * NFT Traits
        * Small Missions Results
        * **Number of** Space Units **members** that set the proper collect&#x20;
* When epoch ends
  * The result of the mission is **published**
    * **Points** added to the Leaderboard
  * Rewards
    * New Elements
    * New Knowledge

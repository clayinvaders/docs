# Build

### Description

There are 5 discover missions per epoch, 1 per day

### Objective

Build new elements or upgrade existing ones

### Main Actors

Engineer, Scientist

### Gameplay

* When epoch start
  * **Crew Engineers and Scientists** receive a notification to inform them they are **in charge** of the **Build Mission**
*   Once per day

    * **Crew Engineers and Scientists** receive a notification **asking** for a selection of elements and knowledge from previous explorations
    * **Crew Engineers and Scientists**  set the **elements and knowledge to use** for the mission
    * At least **1 Engineer & 1 Scientist** start the mission

    `/ci-game start-build`

    * **Space Unit** **Members** **vote** on the action to choose (DISCORD pool)
    * The mission **start**
      *   Element creation

          * **All Space Unit Members** set the contribution for the mission

          `/ci-game new-element`\
          `/ci-game upgrade-element`
      * Randomly, the users in the SpaceUnit receive small missions to complete:&#x20;
        * (v1) DISCORD bot messages with puzzles
        * (v2) Web Minigame link to play
      * Randomness (coordinates deviation)
        * Blockchain Random seed
        * Fulfilled Crew vs. Available Roles
        * Number of Passengers
        * NFT Traits
        * Small Missions Results
        * **Number of** Space Units **members** that set the proper create-element&#x20;
* When epoch ends
  * The result of the mission is **published**
    * **Points** added to the Leaderboard
  * Rewards
    * Elements Upgrades
    * New Elements

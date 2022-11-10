# Build

### Description

There are 5 discover missions per epoch, 1 per day

### Objective

Build new elements or upgrade existing ones

### Main Actors

Engineer, Scientist

### Gameplay

* When epoch start
  * **Crew Engineers and Scientists** receive a notification to inform them they are **in charge** of the **Explore Mission**
*   Once per day

    * **Crew Engineers and Scientists** receive a notification **asking** for a new **coordinate** to explore, and type of exploration (Elements or Knowledge)
    * **Crew Engineers and Scientists**  set the **elements and knowledge to use** for the mission
    * At least **1 Engineer & 1 Scientist** start the mission

    `/ci-game start-build`

    * **Space Unit** **Members** **vote** on the action to choose (DISCORD pool)
    * The mission **start**
      *   Element created

          * **All Space Unit Members** set the contribution for the mission

          `/ci-game set save-element`
      * Randomness (coordinates deviation)
        * Blockchain Random seed
        * Fulfilled Crew vs. Available Roles
        * Number of Passengers
        * NFT Traits
        * **Number of** Space Units **members** that set the proper save-element&#x20;
* When epoch ends
  * The result of the mission is **published**
    * **Points** added to the Leaderboard
  * Rewards
    * New Elements

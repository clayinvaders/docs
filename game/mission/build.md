# Build

### Description

There are 5 discover missions per epoch, 1 per day

### Objective

Discover new Galaxies & Planets

### Main Actors

Engineer, Scientist

### Gameplay

* When epoch start
  * **Crew Engineers and Scientists** receive a notification to inform they are **in charge** of the **Explore Mission**
*   Once per day

    * **Crew Engineers and Scientists** receive a notification **asking** for a new **coordinate** to explore, and type of exploration (Elements or Knowledge)
    * **Crew Explores** set the **coordinates** for the mission
    * At least **1 Engineer & 1 Doctor** start the mission

    `/ci-game start-exploration`

    * **Space Unit** **Members** **vote** the action to choose (DISCORD pool)
    * The mission **start**
      *   Element founds

          * **All Space Unit Members** set the contribute for the mission

          `/ci-game set collect-element`
      *   Knowledge found

          * **All Space Unit Members** set the contribute for the mission

          `/ci-game set collect-knowledge`
      * Randomness (coordinates deviation)
        * Blockchain Random seed
        * Fulfilled Crew vs. Available Roles
        * Number of Passengers
        * NFT Traits
        * **Number of** Space Units **members** that set the proper collect&#x20;
* When epoch ends
  * Result of mission is **published**
  * Rewards
    * New Elements
    * New Knowledge

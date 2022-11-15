# Invade

### Description

There are 5 **Invade** missions per epoch, 1 per day.

Conditions to start the mission:

* The planet was not Invaded yet
* You have the exact coordinates or a Planet Coordinates Key (NFT)
  * Coordinates are readable only by the owner

### Objective

Invade a Planet

### Main Actors

Commander, Pilot & Doctor

### Gameplay

* When epoch start
  * **Crew Pilots** receive a notification to inform them they are **in charge** of the **Invasion Mission**
* Once per day
  * **Crew Pilots** receive a notification **asking** for a new **coordinate** to discover
  * **Crew Pilots** set the **coordinates** for the mission
  * **Crew Commander** starts the mission
  * **Space Unit** **Members** **vote** the coordinate to choose (DISCORD pool)
  * The mission **starts**
    * **All Space Unit Members** need to react before the day's end
    *   **Forced** Invasion: the planet is close enough to the settled coordinates, but not 100% precise

        * **All Space Unit Members** set the **forced invasion mode** for the mission

        `/ci-game set forced-invasion`
    *   **Pacific** Invasion: 100% precise coordinates

        * **All Space Unit Members** set the **pacific invasion mode** for the mission

        `/ci-game set pacific-invasion`
    * The mission **starts**
      * Randomly, the users in the SpaceUnit receive small missions to complete:&#x20;
        * (v1) DISCORD bot messages with puzzles
        * (v2) Web Minigame link to play
    * Randomness (coordinates deviation)
      * Blockchain Random seed
      * Fulfilled Crew vs. Available Roles
      * Number of Passengers
      * NFT Traits
      * **Number of** Space Units **members** that set the proper invasion type (forced or pacific)
      * Small Missions Results
      * Forced Invasion
        * A random number of **members** injured
        * The number of **Doctors** in the Crew reduce injures
* When epoch ends
  * The result of the mission is **published**
    * **Points** added to the Leaderboard
  * Rewards
    * Planet Portal Key

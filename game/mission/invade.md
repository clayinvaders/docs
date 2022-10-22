# Invade

### Description

There are 5 **Invade** missions per epoch, 1 per day.

Conditions to start the mission:

* Planet was not Invaded yet
* You have the exact coordinates or a Planet Coordinates Key (NFT)
  * Coordinates are readable only by the owner

### Objective

Discover new Galaxies & Planets

### Main Actors

Commander, Pilot & Doctor

### Gameplay

* When epoch start
  * **Crew Pilots** receive a notification to inform they are **in charge** of the **Invasion Mission**
* Once per day
  * **Crew Pilots** receive a notification **asking** for a new **coordinate** to discover
  * **Crew Pilots** set the **coordinates** for the mission
  * **Crew Commander** start the mission
  * **Space Unit** **Members** **vote** the coordinate to choose (DISCORD pool)
  * The mission is **performed**
    *   Forced Invasion: planet is close enough of the settled coordinates, but not 100% precise

        * **All Space Unit Members** set the **forced invasion mode** for the mission

        `/ci-game set forced-invasion`
    *   Pacific Invasion: 100% precise coordinates

        * **All Space Unit Members** set the **forced invasion mode** for the mission

        `/ci-game set pacific-invasion`
    * Randomness (coordinates deviation)
      * Blockchain Random seed
      * Fulfilled Crew vs. Available Roles
      * Number of Passengers
      * NFT Traits
      * **Number of** Space Units **members** that set the proper invasion type (forced or pacific)
      * Forced Invasion
        * Random number of **members** injured
        * Number of **Doctors** in Crew reduce injures
* When epoch ends
  * Result of mission is **published**
  * Rewards
    * Planet Portal Key

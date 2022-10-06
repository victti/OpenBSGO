# OpenBSGO

#### None of the repo, the tool, nor the repo owner is affiliated with, or sponsored or authorized by, BigPoint or its affiliates.
##### This server is for learning more about C# and Networking. I am not responsible for other people's Forks.
###### Feel free to open Issues or do Pull requests.
###### This is a rewrite of <a href="https://github.com/victti/BSGO-Private-Server" target="_blank">this repository</a>.
###### No code will be available until a stable release is finished.
###### This repo has little to none code from BigPoint. Although you are required to have the original game files in order to run the server, since the server uses the game's dll for essential run code.

## About
OpenBSGO is an open source server emulator of the Massive Multiplayer Online game known as Battlestar Galactica Online that was created by BigPoint. It's an emulation of the original server, that tries to bring back the original essence of the game. It is written in C# (.NET Core 6.0) and uses SQLite to save the player data. It still is in its initial stages so bugs and missing protocols are expected when using it.

## Features
- Supported version:
  - Latest released by BigPoint. I'm not sure if it works for other versions.
###### TBD

## Why and what was fixed/improved?
This is something that people might wonder, why rewrite instead of fix what was broken? Answer is simple: I was not satisfied with the old project. It has broken stuff I couldn't fix or in order to fix I'd have to remove too much essential stuff that would break more things. Rewritting is the easiest way. So, what was improved?
- Collisions were added.
  - The last version didn't have a collision, but the closed source rewrite I made back when BSGOPS existed had collisions. The old collision system was improved so much that now it has little to none impact on CPU time. Recent tests showed that the old collision system could handle 1000 objects before start lagging, and the new collision system can handle 100000 objects and not even start lagging yet.
- Shop items were added.
- Skills were added.
- Each ship has its on FTL time like the original server.
- After a FTL jump or join the game, you are no longer targetable/visible for about ~1 sec.
- Outposts were improved.
  - Sector Levels were added.
  - They now keep spawned on the sector after jump/dock. (Bugfix)
  - Combat modules were added.
    - They can now target and kill you.
    - Upgraded OP have a passive computers to buff allies damage. (QoL)
    - Fortified OP have a passive computer to buff allies armor. (QoL)
- All ships are playable.
- Buff and Debuffs were added. (Partially)
- AI was added.
  - OP targetting system is considered an AI.
    - It decides which target is the best to shoot at depending on distance, health and ship tier.
  - A dumb AI was also added. The "dumb" is because all the AI does is turn to the target direction every X seconds. This is the behavior AI had on BSGO.
  - 2 new AIs will be added in the future:
    - Smart AI:
      - These bots will have better equipment.
      - They will better use their weapons.
    - Player like AI:
      - These bots will have player like equipment.
      - They (possibly) will use Neural Networking.
- Sector bounds was added.
  - Now reaching the sector bounds will trigger radiation.
- Radiation Zones (QoL)
  - Now when nukes explodes, they leave behind a radiation zone for a few seconds.
  - Random radiation zones with better loot can be found on sectors close to the Nebula.
- Mining (WiP)

## Quality of Life (QoL)
These features are totally optional on the server and can be disabled with a simple change on the server config file. They are meant to improve the game's life from the server side, since we can't touch the original game files. Be aware that the changes listed above that are marked as (QoL) are not final and might be changed any time in the future.

## Screenshots
###### TBD

## Usage
###### TBD

## Credits
- aeroson (For the implementation of UnityEngine.Quaternion).
- bubisnew.
- Mementomori (aka FLOREK BGO).

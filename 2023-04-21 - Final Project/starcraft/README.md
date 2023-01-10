# StarCraft Project Feature Checklist
- [x] Chosen speciality is: _____
  - [ ] Specialty implemented successfully and demonstrated in video
- [ ] Resource Gathering Basics
  - [ ] All idle workers sent to gather minerals
  - [ ] 3 workers placed in each gas refinery
  - [ ] Max 2.5 workers per mineral patch in base
- [ ] BuildOrder Production
  - [ ] BuildOrder class parses text file
  - [ ] BuildOrder queue works properly
    - [ ] Loop monitors queue for next item to be built
    - [ ] If resources available, check for builder unit
    - [ ] If builder unit found, check build location (if required)
    - [ ] If build location found, built unit and remove from queue
    - [ ] Be sure to 'reserve' resources so items don't get skipped while building
- [ ] Scouting
  - [ ] All enemy units and their last positions recorded / drawn
  - [ ] If enemy base is not known:
    - [ ] Move toward next possible enemy location
  - [ ] If enemy base is known:
    - [ ] If outside enemy base, go toward it with scout
    - [ ] If inside enemy base, attack enemy worker
    - [ ] If worker attacks back or has defenses, retreat scout
- [ ] Defense
  - [ ] Enemy units in base detected, circle drawn around them
  - [ ] Static defense structure constructed
- [ ] Attack Timings
  - [ ] Army units rallied after production
  - [ ] Condition for attack calculated successfully
  - [ ] Attack sent toward known enemy location
  - [ ] Final enemy buildings found and destroyed
- [ ] Expanding
  - [ ] Natural Expansion location calculated and drawn to map
  - [ ] Expansion built and demonstrated at least once for video
- [ ] Succesfully default built-in AI sometimes

# StarCraft Project Feature Requirements

Here you will find a list of all the requirements for the StarCraft project. These are listed somewhat in order of how they should be implemented, since later features probably require the previous features to be working first in order to function properly. The goal of this project is not simply to make the highest win rate bot by rushing your opponent with Zerglings, but to focus on an interesting AI topic specialty (listed below) and implement it in a real-time game setting.

## Feature 0: Chosen Specialty

- You cannot simply make a zergling rush bot and submit it for the project, it must be more complex than that
- Your bot must have a chosen specialty, which is an area of focus that makes your bot unique from others
- This chosen specialty must be detailed in the project proposal
- A list of possible areas to focus on for your specialty are as follows:
  - Improved building placement using some clever geometric algorithm
  - Making spell-casting units and doing clever target selection
  - Siege-Tank push with clever positioning of units
  - Strategic use of Zerg burrowing 
  - Fast expansion build with initial static defenses 
  - Improved multi-unit path-finding with vector fields
  - Mutalisk bot with superhuman kiting micro behavior
  - Drop strategy with loading units into transport then unloading at enemy base
  - Any other map related algorithmic or geometric processing task
- This speciality does not need to be executed perfectly or win all the time, but a significant effort does need to be made

## Feature 1: BuildOrder Production 

- Your bot must be able to successfully execute a build-order list from a text file located in `bin\BuildOrder.txt`. 
- Your build order file must support up to [Tier 2 basic buildings and units](https://www.cs.mun.ca/~dchurchill/starcraftaicomp/files/game_info/) of your chosen Race
- You do not have to support add-on buildings, upgrades, or tech types in the build-order file
- You must build each item in the order specified, and not go to the next item until the previous one is built
- Once the build order list from the file is exhausted, a rule-based system in your bot then takes over
- If a non-unit type needs to be built for your specialty, it can be done outside of the build order file
- If your chosen specialty requires add-on buildings, they can go in the build-order file
- You may use the [BuildOrderQueue](https://github.com/davechurchill/ualbertabot/blob/master/UAlbertaBot/Source/BuildOrderQueue.h) and [ProductionManager](https://github.com/davechurchill/ualbertabot/blob/master/UAlbertaBot/Source/ProductionManager.h) from UAlbertaBot as inspiration for this feature, but do not simply copy and paste the code. You should implement it yourself, and it does not need to be nearly as complex since it will only use `BWAPI::UnitType` items, and does not require a priority system, just build things from start to finish

## Feature 2: Basic Scouting
- Your bot must be able to successfully scout the enemy base and keep track of the last known position of enemy units
- Your should draw a circle on the map where each enemy unit was last seen, including the type of unit
- A custom data structure needs to be used for tracking hidden units, since their unit pointer is not valid when in the fog of war
- After scouting enemy base, your scout should try to harass enemy workers

## Feature 3: Basic Defense
- If an enemy unit is detected in your base, it should be attacked
- If an enemy scout worker is detected in your base, send a worker or other unit to attack it
- At least one static defense unit should be built in your base (bunker, cannon, or sunken colony)

## Feature 4: Attack Timing

- Your bot must implement a condition under which your attack against the enemy begins, such as after:
    - A specific number of units have been created
    - A specific time has been reached
    - A specific map condition or expansion has been created
- It is important to build up a number of units before attacking the enemy, so that you don't simply throw units one by one into the enemy base to die
- As army units are produced, they should rally together at a centralized point near the entrance to your base
- Once the attack condition is true, army is sent to attack enemy base
- Often times, the enemy may have buildings placed around the map that have not yet been scouted. Any remaining enemy buildings should be found and attacked by the bot to actually end the game

## Feature 5: Expanding

- In order to keep gathering minerals, your bot must expand to a new location to harvest more resources
- You must calculate the closest possible "natural" expansion location in order to build there
- You must create at least 1 expansion at some point in the game based on some game condition trigger
- This won't always happen in every game, but you must show your bot successfully expand at least once in the video
- I would like you to try to calcualte the location for an expansion on your own, however you can use existing libraries like [StarDraft](https://github.com/davechurchill/stardraft) for inspiration. Your calculated location does not need to be pixel perfect

# Starcraft Code Structure

- The above checklist should be updated as features are completed, so I can see them with the final submission
- All instructions should be removed from this file for the final submission with only the checklist remaining
- This folder should the following 3 directories:

```
bin/ 
  - must contain your compiled StarterBot.exe
  - must contain any additional files you need in your bin dir
  - do not include any visualstudio output debugging files such as .pdb files

src/ 
  - must contain your bot source code
  - copy all files from your STARTcraft windows/c++/src/ directory here

visualstudio/
  - must contain your visual studio project files
  - copy all files from your STARTcraft windows/c++/visualstudio/ directory here
  - delete all temporary output vs directories, they contain massive files
    - visualstudio/Release
    - visualstudio/Debug
    - visualstudio/.vs
```

Simply copy your `bin`, `src`, and `visualstudio` directories from your STARTcraft project into this directory.

This entire submission should be no more than a few megabytes at most. 

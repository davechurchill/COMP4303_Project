
# Minecraft Project Feature Checklist
- [x] Specialty chosen: __________
- [ ] Adaptivity
  - [ ] Settlement avoids 'steamroller' approach
  - [ ] At least 2 structures adapted to terrain features
    - [ ] Near or on steep cliff
    - [ ] Near or on water or ice
    - [ ] In or around trees
    - [ ] Flat terrain
  - [ ] One specific feature for at least 4 biomes
- [ ] Functionality
  - [ ] Building count and placement randomized, does not create the exact same city twice
  - [ ] Settlement contains 4 'types' of building
  - [ ] Buildings randomized in size / shape
  - [ ] Building interiors accessible and decorated  
  - [ ] Building interiors randomized
  - [ ] Paths between major builings / attractions
  - [ ] Paths generated via M.S.T. or other algorithm
  - [ ] At least one "moving" feature (minecart, elevator, lift, etc)
  - [ ] Some CA / Noise / other generative algorithm used in some form
  - [ ] Defensive structure(s) created
- [ ] Narrative
  - [ ] Include the 'story' of your village
  - [ ] Construction must make sense within that narrative
- [ ] Aesthetics
  - [ ] Color of blocks chosen based on biome
  - [ ] Building types constructed with different materials
  - [ ] Decorations places where appropriate
  - [ ] At least 1 outdoor feature (farm, etc)


# Minecraft Project Feature Requirements

Here you will find a list of all the requirements for the Minecraft project. The goal of this project to create an entry for the [Generative Design in Minecraft Competition (GDMC)](https://gendesignmc.wikidot.com/wiki:2022-settlement-generation-competition). In 2020 [an entry by 3 students from COMP4303 (Troy, Ryan, and Trent) won the GDMC](https://gazette.mun.ca/student-life/3d-world-builders/) with their [self-titled entry](https://gendesignmc.wikidot.com/wiki:2020-settlement-generation-competition) - an excellent feature to add to a resume.

According to the GDMC website: "The Settlement Generation Challenge is about writing an algorithm that can create a settlement for a given, unknown Minecraft map. The challenge is to produce an algorithm that is adaptive towards the provided map, creates a settlement that satisfies a range of functional requirements - but also looks good and evokes an interesting narrative. The goal is to basically produce an algorithm that can rival the state of the art of what humans can produce"

The project should follow the [rules for the GDMC](https://gendesignmc.wikidot.com/wiki:2022-settlement-generation-competition), closely adhering to the 4 main judging criteria: Adaptivity, Functionality, Narraitive, and Aesthetics. I highly recommend watching the [2021 Winner Presentation Video](https://youtu.be/uYUIZUGPNX8) to become a little more familiar with the project before proceeding further, since it explains many of these concepts. You can also [watch some of the past student project video trailers](https://www.youtube.com/watch?v=X9VV-F9465U&list=PL_xRyXins849F8QIw5s1ID8FOR2cdPMzH&index=1) for inspiration.

As the judging criteria are quite abstract, in order to create a more concrete set of project requirements, you will find above a checklist of required functionality that I would like to see in your final project. Below is a more detailed explanation for each feature. You will also be required to choose a 'specialty' which will make your settlement unique from others.

## Chosen Specialty

- You are required to choose a specialty for your village that will make it stand out from others in a signficant way.
- Examples of specialties can be:
  - Heavy use of villagers, farms, or outdoor features
  - Advanced path-finding or building placement algorithms
  - Theme or style of decoration that heavily plays into narrative
  - Special large features or buildings 

## Adaptability

- Your settlement must adapt to the surrounding area that is chosen by the GDMC competition. It cannot simply taken any given input area, flatten it like a construction site, and then build on top of it
- You may flatten some areas in order to build the basis for a building, etc, but it must blend in naturally with the surroundings
- You must have 2 structures which are specifically adapted to specific terrain types. For example, maybe you have a fishing hut with a dock near the edge of the water, or a tree house when placed near a forest. There is a chance that a given location does not include these features, but your final project video must include examples where these are demonstrated
- You must contain 4 features which are biome-specific. For example, it doesn't make sense to make an igloo out of ice in the middle of a desert. Choose 4 biomes from the [list of all possible minecraft biomes](https://help.minecraft.net/hc/en-us/articles/360046470431-Minecraft-Types-of-Biomes) and demonstrate one feature or building that is specific to those biomes in your settlement. That feature MUST appear when you are in that biome, and cannot appear in other biomes. Your presentation should show off these features.

## Functionality

- You must make sure that your buildings and structures are not simple copy and paste of each other. They must be paramaterized in some way to account for difference sizes and locations, and then those parameters must be randomized when creating your settlement. 
- Your settlements must contain at least 4 "types" of buildings. Some examples of building types might be a house, church, barn, store, etc.
- All buildings must have doors so that they can be entered 
- All buildings must have decorated interiors that demonstrate the relevant function of that building (ex: houses have beds)
- You must use some sort of path-finding algorithm in order to create a road/path system between the major features of your town. For example, you could create paths on the ground based on a [Minimum Spanning Tree](https://en.wikipedia.org/wiki/Minimum_spanning_tree) graph of all the buildings in your town.
- Your settlement must have at least one major 'moving' feature, such as a minecart, elevator lift, etc)
- Some part of your settlement, either building placement or decoration, must be generated by a PCG algorithm such as cellular automata, Perlin noise generator, etc
- You must include some sort of defensive structure either within or surrounding your settlement that fits into the narrative of your building. Examples of defensive structures can be: walls or a moat surrounding the city, towers or turrets, bunkers, etc.

## Narrative

- You must create and describe a 'narrative' or story for your settlement that is reflected somehow in its design and construction
- Utilize NPCS such as villagers, animals, etc to help drive this narrative in some way

## Aesthetics

- Your settlement should look nice! Make sure you put some time and effort into your settlement not looking like a bunch of grey rectangular buildings
- The colors and materials of blocks chosen to construct your settlement should somewhat match the biome they are in
- Decorations should be placed outside and inside buildings in order to make the settlement look nicer and provide a sense of being lived in
- You should include at least 1 major outdoor feature in your settlement such as a farm, etc

# Minecraft Code Structure

- All of the code used to generate your project should be placed in this folder
- The above checklist should be updated as features are completed, so I can see them with the final submission
- All instructions should be removed from this file for the final submission with only the checklist remaining

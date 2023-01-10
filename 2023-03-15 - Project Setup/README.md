# Starcraft Setup Requirement

- You must install Starcraft, BWAPI, and compile and run the StarterBot from STARTcraft. 
- Using the example code in StarterBot, you must construct 8 Probes using the Protoss Race
- Once 8 probes have been constructed, you must tell them to stop gathering Minerals, and give them move commands so that they are positioned in a straight line near your Nexus
- You must also print the names of your group members to the screen using drawTextScreen
- All of your code must be contained within the StarterBot.cpp file for this Assignment
- Take a screenshot of the final result of the line of Probes and your names 
- Place the screenshot and your StaterBot.cpp file in this directory
- Edit this README.md file to remove the instructions and replace with your embedded screenshot

# Starcraft Setup Instructions

The Starcraft / BWAPI / STARTcraft setup process is very well documented. 
I will be demonstrating it extensively in class, but you can also follow these written instructions:
- https://github.com/davechurchill/STARTcraft
- https://github.com/bwapi/bwapi

# Minecraft Setup Requirement
- You must install one of the 2 GDMC API options presented on the following page
- You must use the sample code to place blocks which spell out “CS4303” somewhere in the Minecraft which is visible above the ground level at position x=0, z=0 (y is height)
- Take a screenshot of your spectacular CS4303 Minecraft creation 
- All of your code must be contained with a single python file
- Place the screenshot and your single python file in this directory
- Edit this README.md file to remove the instructions and replace with your embedded screenshot

# Minecraft Setup Instructions

- All instructions can be found on the GDMC wiki: https://gendesignmc.wikidot.com/
- You can also find more information on the [GDMC Discord Server](http://discord.gg/ueaxuXj)
- There are two main ways of setting up the GDMC framework. 

### 1) Setting up GDMC with HTTP Server (Recommended)

Using this method, an HTTP server automatically starts when the game is run, and you get/set block types via HTTP GET and PUT requests. It allows you to edit blocks of a Minecraft world in real-time, which the other method does not allow you to do. This method uses an HTTP server connected to Minecraft using a Forge Mod. I set everything up and got it running in less than 15 minutes. You just have to install the current retail version of Minecraft, then install the Forge mod loader, then copy the http server jar to a specific folder, and run Minecraft. It comes with example python3 code which is extremely easy to use to get started, however any language can be used if you really want to. The problem with using another language is that you need to be able to send http requests, as well as decode the Minecraft chunk data, which is already done for you with the example python code. 

- https://gendesignmc.wikidot.com/wiki:submission-httpserver
- https://files.minecraftforge.net/
- https://github.com/nilsgawlik/gdmc_http_interface/releases/tag/v0.3.1
- https://github.com/nilsgawlik/gdmc_http_client_python (sample python code)
- https://github.com/yhirose/cpp-httplib (if you really want to try C++)

### 2) Setting up GDMC with MCEdit

This method is historically more popular, and was what people used for last year’s projects. However, it is a little more cumbersome to set up. I have never personally used it, but it involves installing Minecraft, MCEdit, Anaconda, and ends up using older python 2.7 code, so I’m not a huge fan. Also, this method does not allow you to edit an actual running Minecraft game in real-time. You must run your entire algorithm to completion in order to see any changes. You can use this method if you wish, but I will not be able to personally offer any help with setting it up or running it.

- https://gendesignmc.wikidot.com/wiki:submission-mcedit


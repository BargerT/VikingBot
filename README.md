# StarCraft BroodWar AI
A bot that uses AI Planning for general strategy management and Reinforcement ML.Learning for combat management.

## Requirements
 - Java 1.8
 - StarCraft: BroodWar patch 1.16.1
 - BWAPI / JavaBWAPI
 - Chaos Launcher
 
Refer to [SSCAI Tutorial](https://sscaitournament.com/index.php?action=tutorial) for a full setup guide

## Resources
* One Tutorial: https://github.com/JavaBWAPI/Java-BWAPI-Tutorial/wiki/Setup 
* Another Tutorial: https://sscaitournament.com/index.php?action=tutorial
* Starcraft AI Page: http://www.starcraftai.com/wiki/Main_Page
* The Java implementation we use: https://github.com/JavaBWAPI/JBWAPI
* It's Documentation: https://javabwapi.github.io/JBWAPI/
* The AI Planner Library we used: http://burlap.cs.brown.edu/
* The IEEE 2020 Conference Published Paper: http://bit.ly/Viking-Bot
* ALSO, we have generated java docs for the project you can read.


## Components
There are agents which interact with starcraft, knowledge which is some quick huristics for efficiency, listeners for the machine learning, ml (the machine learning), planning (the AI planning)< and then a few classes that actually run the bot.

# Agents
## Intelligence Agent
Singleton for knowledge about starcraft, and telling the AI Planning about the game

## Strategy Agent
Handles executing AI Planning actions, and normal actions every frame.

## Combat Agent
Handels combat information, and Machine Learning/AI Planning interaction.

## Economy Agent
Handles building buildings, and the economy.

### ML
The Machine Learnign controlls the Units movement and fighting, it consists of the ML package, and is used by the agents via the Combat Agent. 

### Planning
The planning package handles the AI Planing, based on burlap. It consists of a few different actions, helper classes for parsing them in the agents, and other classes needed for BURLAP to work. 


## Replays
A list of replays recorded at the end of each milestone


# Making the Bot Play Itself
## Ideal version
1. in intellij, compile the bot into a jar. (https://www.jetbrains.com/help/idea/compiling-applications.html#package_into_jar)
2. Convert the jar to a .exe https://www.genuinecoder.com/convert-java-jar-to-exe/
3. move the file to a place bwapi can find it (so basically into the bapi data folder)
4. set up the config to work for multiple ai http://www.starcraftai.com/wiki/Multiple_instances_of_StarCraft
5. use the Chaoslauncher - MultiInstance.exe rather than normal chaos launcher, launch it twice
6. multiplayer -> local pc, and join the game (make sure the config is expecting the right races and game mode)
7. start the match

## If That Fails
Same process as above almost, but when making the .exe in Launch4j, go to the header section and change the header type from GUI to console.
1. in intellij, compile the bot into a jar. (https://www.jetbrains.com/help/idea/compiling-applications.html#package_into_jar)
2. Convert the jar to a .exe https://www.genuinecoder.com/convert-java-jar-to-exe/
3. start the Chaoslauncher - MultiInstance.exe rather than normal chaos launcher
4. Run the .exe file, and a console should open up. Then run an instance of starcraft using the chaos launcher. The ai should connect to the instance of starcraft
5. repeat step 4 for as many instances of the bot as you want to run,
6. multiplayer -> local pc, and join the game (make sure the config is expecting the right races and game mode)
7. start the match


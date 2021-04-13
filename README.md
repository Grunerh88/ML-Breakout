Introduction:

The goal of our project was to create a Breakout clone utilizing Unity and Unity-ML to train a neural net to play and compete against a player. We had to find a way to create a working adaptation of the classic game using the C# language -- while also familiarizing ourselves with the Unity tools and assets, as well as Unity-ML agents. 
On the Unity side, we had to learn how to create game objects and canvases while learning how to combine those with assets such as sounds and artwork. With Unity-ML, we had to learn to see things from the perspective of the neural net so that we could determine what values we needed to track. In training, we had to experiment and observe with which parameter settings worked best, while also determining how the rewards should be applied and determined. These were all aspects that all team members had very little to no experience in to begin with, but learned and adjusted to as the project progressed.

Description:

When the game starts, the user is presented with the main menu which lets them decide to play the game or quit. If the user decides to play, the game instantly loads into a split screen view where the neural net plays on the left side, and the user plays on the right side utilizing mouse controls.

The game progresses until either one of three conditions is met:
Win via higher score than losing side
The losing side is in a game over state (ball out of bounds), score frozen
The winning side is able to surpass the losing side’s score
Win via reaching high score limit
The winning side achieves the current high score limit of 1500 first
The losing side is still in play, but current score is less than 1500
The game ends in a draw
Both sides are in a game over state (ball out of bounds) and the score is equal

Instructions:

Move the paddle:
Move the mouse to control the paddle. The paddle will follow the mouse exactly on the horizontal axis.

Launch the ball:
		Mouse left click

Software and Systems Function:

Unity is a powerful game engine tool that serves as the core of the project. The software allows for the creation and manipulation of objects with a myriad of physics and kinematic settings. Attached scripts in C# dictate object and element behavior in a scene. The game was fully developed using Unity.
In order to create and subsequently train agents to play the game, we used the ML Agent ToolKit. After installing and adding the ML Agent ToolKit, options for creating agents and machine learning environments become available within Unity. These options tangibly take the form of new components such as decision requesters and behavior parameters that can be attached to agent objects.
A couple other components are needed to undergo training with the ML Agent ToolKit Package. PyTorch, an open source machine learning library provides the necessary functionality needed to implement training. Pytorch and the ML Agent ToolKit communicate to set up and run training iterations with desired settings.
The mlagents python package contains the machine learning algorithms needed to train behavior in a scene. Installation and running of mlagents requires a Python 3.7 virtual environment. After running python mlagents, it waits and listens for the associated Unity project scene to begin by pushing the play button. At this point the python mlagents program manages the training of the agents in the desired scene via the desired training configuration settings.
Software Libraries, Languages, APIs, Tools

Languages:

C# (Unity)
Python (Unity-ML)

Software / Software Libraries / APIs / Tools:
Unity
Unity Collab
Unity ML-Agents
Visual Studio / Code
PyTorch
GitHub (game hosting)

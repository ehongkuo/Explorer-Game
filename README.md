# Explorer-Game

This is an exploration game created with C++ that is meant to be run directly from the terminal. The user plays the game with user input provided with 'W', 'A', 'D' keys to move and can either run the game in **print** mode or **curses** mode.

![Gameplay Demo](/images/demo.gif)


Print mode requires the user to type in input (*For Example: 'W'*) and then press *Enter* to make a move. This is shown below:

![Print-Mode Demo](/images/print-mode.gif)

Curses mode makes this game much easier to play by eliminating a need to press *Enter* for every move. This mode is activated by simply passing in an additional argument to the call to ./main [arg] which in the demo below, is simply a '1'. (User input is no longer printed to terminal in this mode) From there, Curses Mode enables the holding down of a key to move rapidly, speeding up gameplay.

![Curses-Mode Demo](/images/curses-mode.gif)

## How to Play

### Setup

Thanks to our Makefile, upon loading this game to your computer, compile this game on your local device by simply typing 'make' into your terminal, and our game is ready to go! After this, we play the game by running the main.cpp file which is done in C++ with ./main. 

Running the following command: [ ./main ] will result in the game running in **print** mode

Running the following command: [ ./main 1 ] will result in the game running in **curses** mode

### Movement

Regardless of mode, the user moves forward and thus uses up a 'move' when pressing 'W'. The 'A' and 'D' keys are for directional rotation, rotating the player left and right 90 degrees respectively. These two keys do not use up 'moves'.

### Rules/Gameplay

The goal of the game is to find and collect all of the items before you run out of moves! The number of moves you have will be updated live and printed to your screen at all times. You must navigate your way through the map to search for items (that appear as dollar signs '$'). There can be multiple map segments on each level which can be accessed through portals (that appear as 'at' signs '@'). Traveling through these will 'teleport' your character to a portal on a different map segment. You are allowed to travel back through the portal you came out of. There will be building obstacles throughout the maps that you cannot move through so make sure to go around those!

### Customizability

Game information is loaded in via the folder 'game_files' and though pre-made levels are included to provide an overall understanding of the game, the player is free to create their own levels by adding new files to the 'game_files' folder and loading them into the main.cpp file!

Just make sure that game and level files follow the following syntax:

#### Game Files

[Height of screen (px)] [Width of screen (px)]
[Number of levels]
[Relative path to file corresponding to level 1]
[Relative path to file corresponding to level 2]
...
[Relative path to file corresponding to level n]

**Example Game File**

45 60
3
level1.txt
level2.txt
boss_level.txt

#### Level Files

[Index of map segment player starts]
[Vertical position at which player starts] [Horizontal position]
[Player starting direction]
[Map Segment data with format: M 'height' 'width'] (index: 0)
[M 'height' 'width'] (index: 1)
...
[M 'height' 'width'] (index: n - 1)



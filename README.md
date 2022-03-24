# Explorer-Game

This is an exploration game created with C++ that is meant to be run directly from the terminal. The user plays the game with user input provided with 'W', 'A', 'S', 'D' keys to move and can either run the game in **print** mode or **curses** mode.

![Gameplay Demo](/images/demo.gif)


Print mode requires the user to type in input (*For Example: 'W'*) and then press *Enter* to make a move. This is shown below:

![Print-Mode Demo](/images/print-mode.gif)

Curses mode makes this game much easier to play by eliminating a need to press *Enter* for every move. This mode is activated by simply passing in an additional argument to the call to ./main [arg] which in the demo below, is simply a '1'. (User input is no longer printed to terminal in this mode) From there, Curses Mode enables the holding down of a key to move rapidly, speeding up gameplay.

![Curses-Mode Demo](/images/curses-mode.gif)

## Movement 

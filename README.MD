# WoW Classic - Character Age

## What does the addon do?

This Addon creates a small movable/ draggable frame in your WoW Classic UI to continously display the information you obtain using the `/played` command in the common chat frame.

The time on the left side is the total game time for the character, the time on the right side it's the time on the current level follwed by the level (as the level will not always be displayed in cout common unit frame, i.e. when in combat or resting in a city or an inn).

The basic idea behind the addon was to help streamers and let's players to inform their viewers.

## How to install from GitHub

* click the `Clone or download` button to open a dialog popup
* click on the `Download ZIP` area to start downloading the project
* open the zip file from your browsers download destination
* copy the `CharacterAge` folder and its contents from the zip file to your `Addons` directory of your WoW Classic installation
* if you are not shure where you installed your WoW Classic programm files have a look at your Battle.net-launcher

## How does the addon work?

In order to continously display your time played with that current character the addon will visibly request the time played everytime when you log in to the world with your character, do something like teleports or simply force the games UI to reload.

At that point the game client fires an `TIME_PLAYED_MSG` event the addon can evaluate in order to optain the time in seconds, for total time played for the character and additionaly the time at the current level.

Taking in account the current system time we got us an offset for displaying the time values without continously requesting the system.

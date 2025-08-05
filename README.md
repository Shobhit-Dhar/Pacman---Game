
# Pygame Pac-Man 

A classic Pac-Man arcade game recreation built from scratch using Python and the Pygame library. This project faithfully implements the core mechanics of Pac-Man, including pellet-chomping, ghost-hunting, and level navigation.


## Table of Contents
- [About the Game](#about-the-game)
- [Features](#features)
- [Gameplay & Controls](#gameplay--controls)
- [Requirements](#requirements)
- [Setup and Installation](#setup-and-installation)
- [Project Structure](#project-structure)
- [How to Play](#how-to-play)
- [Ghost AI](#ghost-ai)

## About the Game

This is a comprehensive Pac-Man clone that demonstrates key game development concepts using Pygame. It includes player and ghost movement, collision detection, unique AI for each ghost, a scoring system, power-ups, and sound effects, all wrapped in the familiar maze environment.

## Features

-   **Classic Gameplay:** Navigate the maze, eat all the pellets, and avoid the ghosts.
-   **Four Unique Ghosts:** Face off against Blinky, Pinky, Inky, and Clyde, each with their own movement AI.
-   **Power-Ups:** Eat the large pellets to turn the tables on the ghosts and hunt them for extra points!
-   **Scoring System:** Gain points for eating pellets and bonus points for eating ghosts.
-   **Life System:** Start with three lives. Lose a life if a ghost catches you.
-   **Animated Characters:** Smooth animations for Pac-Man's movement.
-   **Dynamic Ghost States:** Ghosts can be chasing, spooked (vulnerable), or eaten (returning to the ghost box).
-   **Sound and Music:** Includes background music and iconic sound effects for chomping, eating ghosts, and player death.
-   **Game State Management:** Clear "Game Over" and "Victory" screens with an option to restart.

## Gameplay & Controls

The goal is to clear the level by eating all the white pellets in the maze while avoiding the four ghosts.

| Action        | Key(s)                               |
| ------------- | ------------------------------------ |
| **Move**      | <kbd>↑</kbd> <kbd>↓</kbd> <kbd>←</kbd> <kbd>→</kbd> Arrow Keys |
| **Restart Game**  | <kbd>Spacebar</kbd> (on Game Over/Win screen) |
| **Quit Game**     | <kbd>Esc</kbd>                       |

## Requirements

To run this game, you will need:
-   Python 3.x
-   Pygame library

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/pygame-pacman.git
    cd pygame-pacman
    ```

2.  **Install Pygame:**
    If you don't have Pygame installed, open your terminal and run:
    ```bash
    pip install pygame
    ```

3.  **Verify Project Structure:**
    Ensure all the asset files and folders are in the correct place as described in the [Project Structure](#project-structure) section below. The game will not run without the required images, sounds, and the `board.py` file.

## Project Structure

For the game to work correctly, your files and folders must be organized as follows:

```
.
├── your_main_game_file.py    # The main python script for the game
├── board.py                  # Contains the level layout data
├── freesansbold.ttf          # Font file
|
├── player_images/
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   └── 4.png
|
├── ghost_images/
│   ├── blue.png
│   ├── orange.png
│   ├── pink.png
│   ├── red.png
│   ├── powerup.png
│   └── dead.png
|
└── *.mp3, *.wav              # All sound and music files in the root directory
    ├── pmt.mp3
    ├── nad.mp3
    ├── ser.mp3
    ├── cc.mp3
    ├── mm.mp3
    ├── l.mp3
    ├── pacman-chomp_1.wav
    ├── pacman_eatfruit.wav
    ├── pacman_death.wav
    └── pacman_eatghost.wav
```

## How to Play

Once you have completed the setup, run the main Python file from your terminal:

```bash
python your_main_game_file.py
```

## Ghost AI

Each ghost has a distinct personality and targeting mechanism, making the game challenging and dynamic. When a power-up is active, their goal changes to run away from Pac-Man. If eaten, their goal becomes returning to the central ghost box.

-   **Blinky (Red):** The Hunter. In his normal state, Blinky is the most aggressive ghost, directly targeting Pac-Man's current position.

-   **Pinky (Pink):** The Ambusher. Pinky tries to outsmart the player by targeting the space just in front of Pac-Man, attempting to cut him off. Her AI favors horizontal movement when seeking the player.

-   **Inky (Blue):** The Wildcard. Inky's behavior is more unpredictable. His AI favors vertical movement, making his pathfinding less direct but creating tricky situations for the player.

-   **Clyde (Orange):** The Distracted. Clyde's AI is the most complex. He will chase Pac-Man directly like Blinky, but will strategically change direction at intersections if it provides a better path, making his movements seem more calculated.

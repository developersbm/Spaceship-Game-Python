<div id="readme-top"></div>

  <h1 align="center">Python Space Battle Game</h1>

  <h4 align="center">
This is my first project and I completed it in 2022. I used Python & PyGame to create a game and learn the language.
    <br />
</h4>

## About The Project

- Experience Space battles in this Python-based game in 1v1s.
- Battle against your friends spaceship with lasers.
- Enjoy the controls and smooth gameplay.
- Built using Pygame library for graphics, movements and sound effects.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Built With

* [![Python][Python.com]][Python-url]
* [![Pygame][Pygame.com]][Pygame-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## How is it built

### Bullets
To handle spaceship movement, I set up event handlers for both the yellow and red spaceships. For the yellow ship, I created a function called yellow_handle_movement which interprets keyboard inputs ('A', 'D', 'W', 'S') to control its movement within defined boundaries. Similarly, for the red ship, I created a function called red_handle_movement which interprets arrow key inputs. These functions adjust the positions of the spaceships smoothly, considering velocity factors to ensure the movement feels natural.

### FPS & Shooting
This part of the game updates the positions of bullets fired from the spaceships and manages shooting mechanics. The handle_bullets function iterates through both yellow and red bullets, updating their positions based on their respective velocities. It also detects collisions between bullets and the opposing player's spaceship. If a collision occurs, it triggers an event to indicate that the respective player has been hit (RED_HIT for the red player and YELLOW_HIT for the yellow player) and removes the corresponding bullet from the game. Additionally, it removes bullets that move off-screen to prevent unnecessary processing.

### Game Loop

The game loop is the central mechanism that controls the flow of the game. It establishes a loop using Pygame, ensuring that the game continues running (run = True) until certain conditions are met. Within the loop, the frame rate is controlled using clock.tick(FPS), where FPS defines the desired frames per second. The loop checks for user events, particularly for quitting the game (pygame.QUIT), and if detected, it sets run to False, ending the loop and quitting the Pygame application using pygame.quit().


### Player Movement For Bullets

This aspect of the game manages player actions related to firing bullets. When players press certain keys, such as 'E' or the spacebar (pygame.KEYDOWN), bullets are fired from their positions and added to their respective bullet lists (yellow_bullets or red_bullets). These bullets, represented as rectangles, are used for collision detection and are essential for the ongoing gameplay mechanics. Potential sound effects for firing bullets are indicated in the code but are commented out.

### Health Feature
This feature tracks and manages player health during the game. Upon collision events (RED_HIT or YELLOW_HIT), the respective player's health decreases by one. If a player's health drops to zero or below, the game declares the winner based on who has remaining health: "Yellow Wins!" if the red player's health drops to or below zero, or "Red Wins!" if the yellow player's health reaches the same condition. The game concludes by displaying the winner and stopping the loop.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[Python.com]: https://img.shields.io/badge/Python-blue?logo=python&logoColor=white&style=flat-square
[Python-url]: https://www.python.org/

[Pygame.com]: https://img.shields.io/badge/PyGame-green?logo=python&logoColor=white&style=flat-square
[Pygame-url]: https://www.pygame.org/docs/
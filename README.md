# Unity Obstacle Course Game

A fun and challenging obstacle course game built with Unity where you navigate a player character through a course filled with moving obstacles while avoiding collisions.

## Overview

This project is a 3D obstacle course game where the player must skillfully maneuver through a course filled with various obstacles, including spinners, rollers, and droppers. The goal is to reach the finish line while minimizing collisions with obstacles.

## Game Features

- **Player Movement**: Control a player character using WASD or arrow keys
- **Dynamic Obstacles**: Navigate through several types of moving obstacles:
  - **Spinner**: Rotates to block the player's path
  - **Roller**: Moves back and forth across the course
  - **Dropper**: Falls from above to create moving hazards
- **Collision Detection**: Real-time collision system that tracks hits with obstacles
- **Scoring System**: Keeps count of how many times you bump into obstacles
- **Material System**: Visual distinction between player, obstacles, and course elements

## Project Structure

```
Assets/
├── Scripts/              # Game logic and player control
│   ├── Mover.cs         # Player movement controller
│   ├── Scorer.cs        # Collision tracking and scoring
│   ├── ObjectHit.cs     # Obstacle hit detection
│   ├── Dropper.cs       # Dropper obstacle behavior
│   ├── Spinner.cs       # Spinner obstacle behavior
│   └── Dropper.cs       # Roller obstacle behavior
├── Prefabs/             # Reusable game objects
│   ├── Player (Boxy).prefab
│   ├── Spinner.prefab
│   ├── Roller.prefab
│   ├── Dropper.prefab
│   └── Obstacle.prefab
├── Scenes/
│   └── SampleScene.unity  # Main game scene
└── Materials/           # Visual materials
    ├── Player Material.mat
    ├── Obstacle Material.mat
    ├── Spinner Material.mat
    └── Start-Finish Material.mat
```

## Controls

| Key | Action |
|-----|--------|
| **W** or **↑** | Move Forward |
| **A** or **←** | Move Left |
| **S** or **↓** | Move Backward |
| **D** or **→** | Move Right |

## Game Mechanics

### Movement
- The player moves in real-time based on keyboard input
- Movement speed and height offset are configurable in the Mover script

### Collision System
- When the player hits an obstacle, the obstacle turns red and is tagged as "Hit"
- The scoring system counts collisions, displaying results in the console
- Obstacles that have been hit don't count as additional collisions

### Obstacles
- **Spinner**: Rotating obstacle that blocks paths
- **Roller**: Moving obstacle that travels across surfaces
- **Dropper**: Falls from above, creating dynamic hazards

## Getting Started

### Prerequisites
- Unity (2020.3 or later recommended)
- C# knowledge for script modifications

### Running the Game
1. Open the project in Unity
2. Navigate to `Assets/Scenes/SampleScene.unity`
3. Press the Play button or press `Ctrl+P`
4. Use the controls above to navigate the obstacle course

## Scripts Overview

### Mover.cs
Handles player movement and input. Responds to horizontal and vertical input axes and moves the player accordingly.

### Scorer.cs
Tracks collisions between the player and obstacles, incrementing a hit counter and logging results to the console.

### ObjectHit.cs
Detects when an obstacle is hit by the player, changing its color to red and tagging it as "Hit" to prevent duplicate collision counts.

## Customization

You can easily customize the game by modifying:
- **Player Speed**: Adjust `moveSpeed` in Mover.cs
- **Obstacle Behavior**: Modify the individual obstacle scripts (Spinner.cs, Roller.cs, Dropper.cs)
- **Materials**: Change material colors in the Materials folder
- **Course Layout**: Redesign the scene in SampleScene.unity

## Future Enhancements

- Timer system to challenge players to complete the course
- Sound effects and background music
- UI for displaying score and time
- Additional obstacle types
- Difficulty levels with varying obstacle speeds
- Leaderboard system

## License

This project is open-source and available for personal and educational use.

## Author

Created as a learning project for game development with Unity.

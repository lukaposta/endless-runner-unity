# Endless Runner - Unity 3D Game

3D endless runner game developed in Unity using C#.
Final thesis project - Faculty of Organization and Informatics, University of Zagreb.

---

## Project Overview

![Game Overview](https://github.com/user-attachments/assets/a4192cc6-5a98-405f-9a59-33e201b17ed3)


This project demonstrates the complete development cycle of a 3D endless runner game built in Unity.

The objective was to design and implement a fully functional prototype that integrates:

* Player movement and physics
* Procedural level generation
* Dynamic obstacle spawning
* Real-time scoring system
* Time-based survival mechanics
* Difficulty scaling
* Camera control using Cinemachine
* Modular object-oriented architecture

The result is a stable, extensible game prototype that reflects practical knowledge of game development and software architecture principles.

---

## Gameplay

The player controls a character that continuously moves forward through a dynamically generated environment.

Main mechanics:

* Avoid obstacles
* Collect coins for points
* Reach checkpoints to extend remaining time
* Pick up apples to increase movement speed and difficulty

The game ends when:

* The timer reaches zero
* The player can no longer recover from critical gameplay mistakes

Each session challenges the player to survive longer and achieve a higher score.

---

## Core Systems

### Player Controller

* Rigidbody-based movement
* Collision detection using BoxCollider
* Animation control via Animator
* Smooth input handling

### Procedural Level Generation

* Dynamic chunk spawning and removal
* Optimized scene management
* Randomized lane-based object placement


<p>
  <img alt="Chunk spawning" src="https://github.com/user-attachments/assets/6f97031a-d2d6-444f-8967-3158acd926ab" width="600">
</p>


### Obstacle System

* Coroutine-based spawning
* Controlled spawn intervals
* Balanced lane distribution

### Scoring System

* Centralized in `ScoreManager`
* Coin pickup adds 100 points
* UI updated in real time using TextMeshPro
* Protected against post-GameOver score changes

### Time Management System

* Managed by `GameManager`
* Initial time: 40 seconds
* Checkpoints extend time by 5 seconds
* Frame-rate independent countdown using `Time.deltaTime`
* Clean state transition to Game Over

### Difficulty Scaling

* Speed modification through Apple pickups
* Speed clamped between defined min and max limits
* Gravity dynamically adjusted
* Camera FOV reacts to speed changes


<p>
  <img alt="Speed" src="https://github.com/user-attachments/assets/2c8a518f-9c2c-41eb-8773-0e4f78818ad3" width="800">
</p>


### Camera System

* Cinemachine integration
* Dynamic Field of View adjustments
* Smooth visual feedback during speed transitions


<p>
  <img alt="Cinemachine" src="https://github.com/user-attachments/assets/938ac697-9ecc-4b23-80ec-d26e4f3a98a0" width="600">
</p>


---

## Architecture & Design Principles

The project follows modular and object-oriented design principles.

Pickup System Hierarchy:

```
Pickup (abstract base class)
├── Coin
├── Apple
└── Checkpoint
```

<p>
  <img alt="Pickups" src="https://github.com/user-attachments/assets/0a941cb6-e09a-4f55-bf4a-c1effbe073a5" width="800">
</p>

Responsibilities are clearly separated:

* `ScoreManager` handles score logic
* `GameManager` handles time and game state
* `LevelGenerator` controls world generation
* `ObstacleSpawner` controls obstacle logic
* UI updates are decoupled from gameplay logic

This structure enables scalability and future feature expansion.

---

## Technologies Used

* Unity (3D)
* C#
* Visual Studio
* TextMeshPro
* Cinemachine
* Unity Physics System

Audio:

* Background track: "Heroic Demise" (OpenGameArt.org)

---

## Project Structure

Assets
Scripts

* PlayerController
* LevelGenerator
* ObstacleSpawner
* Pickup
* Coin
* Apple
* Checkpoint
* ScoreManager
* GameManager

Scenes

* MainMenu
* GameScene


<p>
  <img alt="Scenes" src="https://github.com/user-attachments/assets/3bf37036-a924-4f1d-89e6-07b6b0a57d48" width="800">
</p>


---

## Key Learning Outcomes

* Implementation of procedural world generation
* State management in real-time applications
* Game loop design and time-based mechanics
* Object-oriented architecture in Unity
* Balancing gameplay systems
* Integration of third-party Unity components


---

## Academic Context

Final thesis project:

**"IZRADA TRODIMENZIONALNE VIDEOIGRE BESKONAČNOG TRČANJA U PROGRAMSKOM ALATU UNITY"**

Author: Luka Pošta, Faculty of Organization and Informatics, University of Zagreb, 2025

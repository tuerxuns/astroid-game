# Astroid Game

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pygame](https://img.shields.io/badge/Pygame-2.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A modern take on the classic **Asteroids** game, built with Python and Pygame. Navigate a spaceship, destroy asteroids, and survive as long as possible!

---

## 📌 Table of Contents
- [Features](#-features)
- [Installation](#-installation)
- [How to Play](#-how-to-play)
- [Game Controls](#-game-controls)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Logging](#-logging)
- [Future Improvements](#-future-improvements)
- [License](#-license)

---

## ✨ Features

- **Player Spaceship**: Control a triangular spaceship with smooth movement and rotation.
- **Asteroid Field**: Asteroids spawn randomly at the edges of the screen and move toward the player.
- **Collision Detection**: Destroy asteroids by shooting them or avoid collisions with them.
- **Asteroid Splitting**: Large asteroids split into smaller ones when hit.
- **Score Tracking**: (Coming soon!) Track your score as you destroy asteroids.
- **Logging**: Game state and events are logged for debugging and analysis.

---

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- Pygame 2.0 or higher

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/tuerxuns/astroid_game.git
   cd astroid_game
   ```

2. Install dependencies:
   ```sh
   pip install pygame
   ```

3. Run the game:
   ```sh
   python main.py
   ```

---

## 🎮 How to Play

- **Objective**: Destroy asteroids to survive as long as possible.
- **Game Over**: The game ends if your spaceship collides with an asteroid.
- **Scoring**: (Coming soon!) Earn points for destroying asteroids.

---

## ⌨️ Game Controls

| Key          | Action                     |
|--------------|----------------------------|
| **W**        | Move forward               |
| **A**        | Rotate counter-clockwise   |
| **D**        | Rotate clockwise           |
| **S**        | Move backward              |
| **SPACE**    | Shoot                      |
| **R**        | Restart (after game over)  |
| **Q**        | Quit (after game over)     |

---

## 📂 Project Structure

```
astroid_game/
│
├── main.py               # Entry point for the game
├── player.py             # Player spaceship logic
├── asteroid.py           # Asteroid logic
├── shot.py               # Player shots logic
├── asteroidfields.py     # Asteroid spawning logic
├── circleshape.py        # Base class for circular game objects
├── constants.py          # Game constants (screen size, speeds, etc.)
├── logger.py             # Logging utilities for game state and events
├── README.md             # Project documentation
└── .gitignore            # Git ignore rules
```

---

## ⚙️ Configuration

Game settings are defined in `constants.py`. You can customize the following:

| Constant                     | Description                                  | Default Value |
|------------------------------|----------------------------------------------|---------------|
| `SCREEN_WIDTH`               | Screen width in pixels                       | 1280          |
| `SCREEN_HEIGHT`              | Screen height in pixels                      | 720           |
| `PLAYER_RADIUS`              | Player spaceship radius                      | 20            |
| `PLAYER_SPEED`               | Player movement speed                        | 300           |
| `PLAYER_TURN_SPEED`          | Player rotation speed                        | 300           |
| `PLAYER_SHOOT_COOLDOWN`      | Cooldown between shots (seconds)             | 0.3           |
| `PLAYER_SHOOT_SPEED`         | Speed of player shots                        | 500           |
| `ASTEROID_MIN_RADIUS`        | Minimum radius of asteroids                  | 20            |
| `ASTEROID_KINDS`             | Number of asteroid size variants             | 3             |
| `ASTEROID_SPAWN_RATE_SECONDS`| Time between asteroid spawns (seconds)       | 0.8           |
| `SHOT_RADIUS`                | Radius of player shots                       | 5             |

---

## 📝 Logging

The game logs two types of data:
1. **Game State**: Logged every second to `game_state.jsonl`. Includes:
   - Timestamp
   - Elapsed time
   - Screen size
   - Player and asteroid positions, velocities, and radii
   - Shot positions and velocities

2. **Game Events**: Logged to `game_events.jsonl`. Includes:
   - Player collisions (`player_hit`)
   - Asteroid splits (`asteroid_split`)
   - Asteroid shots (`asteroid_shot`)

Logs are stored in JSON Lines format (`.jsonl`), where each line is a valid JSON object.

---

## 🔮 Future Improvements

Here are some ideas for future enhancements:
- **Score System**: Track and display the player's score.
- **Sound Effects**: Add sound effects for shooting, collisions, and asteroid destruction.
- **Visual Effects**: Add particle effects for explosions and shots.
- **Power-Ups**: Introduce power-ups like shields, speed boosts, or multi-shot.
- **High Scores**: Save and display high scores.
- **Difficulty Levels**: Adjust asteroid spawn rates and speeds.
- **Multiplayer**: Add local or online multiplayer support.

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

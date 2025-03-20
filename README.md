# Top-Down RPG Game (Work in Progress)

Welcome to the repository for my **top-down RPG-style game** built in **Godot Engine**! This project is currently a work in progress, but it already features a robust foundation for player and enemy mechanics, state machines, animations, and interactions. Below is an overview of the project, its features, and the technologies used.

## Project Overview

This game is a **top-down RPG** where players control a character in a 2D world, exploring environments, interacting with objects, and engaging in combat with enemies. The project is designed with modularity and scalability in mind, allowing for easy expansion as development progresses.

### Key Features Implemented So Far:
- **Player Movement and Animation**: The player can move in four cardinal directions (up, down, left, right) with smooth animations. The player's sprite flips based on the direction of movement.
- **State Machine for Player and Enemies**: Both the player and enemies use a **state machine** to manage behaviors such as idle, walking, attacking, and more. This allows for clean and modular code, making it easy to add new states or modify existing ones.
- **Combat System**: The player can attack enemies, and enemies can take damage. The combat system uses **HitBox** and **HurtBox** areas to detect collisions and apply damage.
- **Enemy AI**: Enemies have basic AI behaviors, including idle and wandering states. They can move randomly within the environment and transition between states based on timers and conditions.
- **Tilemap and Camera Bounds**: The game uses **Tilemaps** for level design, and the camera is constrained to the bounds of the current tilemap, ensuring the player stays within the visible area.
- **Sound Effects**: The game includes sound effects for actions like attacking, with pitch variation to add variety.

### Planned Features:
- **Expanded Enemy AI**: More complex enemy behaviors, such as chasing the player or patrolling specific areas.
- **Player Abilities**: Additional abilities or skills for the player, such as ranged attacks or special moves.
- **Inventory System**: A system for the player to collect and manage items.
- **Dialogue System**: Interactions with NPCs and dialogue trees.
- **Level Progression**: Multiple levels with increasing difficulty and unique challenges.

## Technical Details

### Core Systems:
- **Player Mechanics**:
  - The player's movement is controlled using a **state machine** with states for idle, walking, and attacking.
  - The player's direction and animations are updated dynamically based on input.
  - The player can attack enemies, triggering damage calculations and animations.
  
- **Enemy Mechanics**:
  - Enemies use a similar **state machine** to manage behaviors like idle and wandering.
  - Enemies can take damage from the player's attacks and are destroyed when their health reaches zero.
  - Basic AI allows enemies to move randomly within the environment.

- **Combat System**:
  - The combat system uses **HitBox** and **HurtBox** areas to detect collisions and apply damage.
  - When the player attacks, a **HurtBox** is activated to detect collisions with enemy **HitBoxes**, triggering damage events.

- **Tilemap and Camera**:
  - The game uses **Tilemaps** for level design, with bounds that constrain the camera's movement.
  - The camera dynamically updates its limits based on the current tilemap's bounds.

- **Sound and Animation**:
  - Sound effects are played during actions like attacking, with randomized pitch to add variety.
  - Animations are tied to the player's and enemies' states, ensuring smooth transitions between actions.

### Code Structure:
- **State Machines**: Both the player and enemies use state machines to manage their behaviors. This modular approach makes it easy to add new states or modify existing ones.
- **Signals and Events**: The game uses Godot's signal system to handle events like direction changes, damage, and state transitions.
- **Modular Design**: The code is designed to be modular, with separate scripts for player, enemy, and state behaviors. This makes it easy to extend or modify the game.

### Technologies Used:
- **Godot Engine**: The game is built using the Godot Engine, a powerful open-source game engine for 2D and 3D games.
- **GDScript**: The primary scripting language used for game logic.
- **Tilemaps**: Used for level design and environment creation.
- **State Machines**: Used to manage player and enemy behaviors.
- **Signals and Events**: Used for communication between different game systems.

## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
2. Open in Godot

3. Open the Godot Engine and import the project by selecting the project.godot file.

4. Run the Game:

5. Open the main scene and click the "Play" button to run the game.

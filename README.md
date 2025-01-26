# Socket.ai

## Multiplayer Survival Game with Ghost

This project is a simple multiplayer network game where players connect to a server and try to survive for 60 seconds while avoiding being caught by a ghost. The game is played on a 16x16 grid, where players move around and try to avoid the ghost. The game supports up to 3 players and allows real-time interaction through a server-client architecture using Python's socket programming and threading.

## Features
- **Multiplayer Support:** Up to 3 players can connect and play the game.
- **Survival Mechanics:** Players must avoid the ghost for as long as possible.
- **Ghost AI:** The ghost hunts down players and doubles its speed every time it catches a player.
- **Leaderboard:** Players are ranked by their survival time at the end of the game.
- **Grid-Based Movement:** Players move around a 16x16 grid using the `W`, `A`, `S`, `D` keys.
- **Real-Time Updates:** The game state is updated in real-time and displayed on all connected clients.

## How It Works
The game consists of two parts:
1. **Server:**
   - The server listens for incoming connections from players, manages game logic, and sends updates (like the game grid and timer) to clients.
   - The server controls the ghost's movement and checks if players are caught.
   - The game ends either when all players are caught or after 60 seconds, and a leaderboard is displayed.

2. **Client:**
   - Players connect to the server, enter their name, and control their in-game character using `W`, `A`, `S`, `D` keys.
   - The client receives real-time updates from the server, such as the current grid, player positions, and ghost's actions.
   - Players can exit the game at any time by typing `EXIT`.

## Requirements
- Python 3.x
- `socket` and `threading` libraries (included in Python's standard library)

## Running the Game

### 1. **Run the Server:**
   - Open a terminal and navigate to the directory containing the `server.py` file.
   - Run the following command to start the server:
   ```bash
   python server.py


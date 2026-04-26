# Multiplayer CHESS

A multiplayer chess game built in Python using sockets and pygame.  
The project uses a client server architecture to synchronize game state across players in real time.

## Overview

This system runs chess as a networked application with one authoritative server.  
The server manages game state, validates moves, and keeps both clients synchronized during gameplay.

## Core Features

- Multiplayer gameplay using sockets
- Server authoritative game state
- Real time move synchronization
- Full chess rule handling
- Turn based system with validation
- Basic UI built with pygame
- Check, checkmate, and forfeit states

## Screenshots

![Menu](Assets/Screenshots/menu.png)
![Lobby](Assets/Screenshots/lobby.png)
![Game](Assets/Screenshots/game.png)
![Check](Assets/Screenshots/check.png)
![Checkmate](Assets/Screenshots/checkmate.png)
![Forfeit](Assets/Screenshots/forfeit.png)

## Technical Details

### Networking

- Uses Python socket library for communication
- Client server model with one host controlling game state
- JSON based message exchange between clients and server
- Continuous update loop for synchronization

### Game Logic

- Move validation handled before state updates
- Turn enforcement handled server side
- Game end detection for check and checkmate

### Architecture

- Server manages all game rules and state
- Clients render board and send input actions
- Separate logic for UI and game state

## Requirements

- Python 3.9 or higher
- pygame

## Run

Start server:

```
python server.py
```

Start client:

```
python main.py
```

For multiplayer setup:

- Run server on one machine
- Run clients on same network using server IP

## Controls

- Mouse click: select and move pieces

## Project Structure

```
server.py  game server and state management
main.py    client UI and input handling
assets/    game visuals and sprites
```

## Limitations

- Network lag affects responsiveness
- Requires manual server connection
- Large packet flow may cause instability

## Future Work

- Better move prediction
- Matchmaking system
- Reconnect handling

## Notes

- Designed for local network play
- Server holds full authority over game state

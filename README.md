# Persistent World Network
Persistent World Network is a proposed suite of open-source software for use in the development and deployment of persistent open-world multiplayer experiences. This is not intended to be an all-purpose "game engine", rather a narrowly-focused effort to close some of the tooling gap that seems to exist in the game development industry. 

## Requirements:
- Low-latency multiplayer netcode
- server-side physics and projectiles with smooth client-side prediction
- Open-world traversal across connected zone servers
- Data transfer across servers
- Persistent world state that can be manipulated by users
- Persistent user state between sessions
- User auth
- Developer API

## Components:
- Login server
    - Authenticate users
    - Route authenticated users to world server
- World server
    - Stores worldwide persistent data
    - Routes authenticated or "lost" users to zone servers
    - Communicates with Zone Servers to sync data across zones
    - Manages zone server lifecyle, spawns new zone servers as needed
- Zone server
    - Stores persistent data for a fixed area in the World
    - Routes users to adjacent Zone servers
    - Communicates with world server and adjacent zone servers to sync data across zones
    - Simulation loop driven by shared class library
- Shared class library
    - A set of shared functions used to drive the simulation loop
- Client library
    - Simulation loop driven by the shared class library
    - rollback prediction
    - Client-Specific functionality

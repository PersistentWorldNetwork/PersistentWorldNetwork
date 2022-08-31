# Persistent World Network
Persistent World Network is a proposed suite of open-source software for use in the development and deployment of persistent open world networked experiences. This is not intended to be an all purpose engine, rather a focused effort to create high performance virtual worlds that can be explored and manipulated by many users simultaneously. 

## Objectives:
- Low latency netcode
- Server-side physics and projectiles with smooth client-side prediction
- Open world traversal across connected zone servers
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
    - Manages zone server lifecycle, spawns new zone servers as needed
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
    - Client Specific functionality

## Milestones
[Networked](Networked.md)
- Single zone server
- Basic networked movement
- Basic networked gravity simulation

[Simulated](Simulated.md)
- Physics Projectile simulation
- Smooth client-side physics prediction (static world)
- non-persistent user state

[Open-World](Open-World.md)
- Multiple zone servers
- World Server to store global user locations
- Communicate user positions and state across zone lines

[Persistent](Persistent.md)
- User authentication
- World server routing
- Persistent global user state
- World server: Manage zone server life cycles
- Any other back-end infrastructure

[Dynamic](Dynamic.md)
- Dynamically change world objects
- Physics with dynamic objects
- Physics with moving objects
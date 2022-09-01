# Networked
[Milestone](https://github.com/PersistentWorldNetwork/PersistentWorldNetwork/milestone/1)
- Single zone server
- Basic networked movement
- Basic networked gravity simulation

The first milestone is a simple networked 3D chatroom. 

## Components
- web-client
    - three.js cube world
    - webrtc plumbing code
    - chat UI
    - chat plumbing code
    - scene graph
- zone-server
    - WebRTC plumbing code
    - scene graph
    - client management (anonymous auth)
- chat-server
    - matrix?

TODO:
- basic three.js cube world scene
- figure out data structure for scene replication
- client pawn movement
- client pawn collision
- client pawn gravity
- zone server data structure for scene replication
- zone server webrtc host
- zone server manage clients
- client connect to zone server
- zone server webrtc stream scene graph to all clients (random updates)
- client stream position updates to zone server (fully trusted client)
- zone server update scene graph from all clients
- chat server host
- chat server manage clients
- client connect to chat server
- client chat UI
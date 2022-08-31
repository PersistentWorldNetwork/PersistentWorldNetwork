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
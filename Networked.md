# Networked

The first milestone is a simple multiplayer networked chatroom. 
- Single zone server
- Basic networked movement
- Basic networked gravity simulation

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
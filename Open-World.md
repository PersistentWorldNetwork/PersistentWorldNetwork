# Open-World
[Milestone](https://github.com/PersistentWorldNetwork/PersistentWorldNetwork/milestone/3)
- Multiple zone servers
- World Server to store global user locations
- Communicate user positions and state across zone lines

## Misc Notes
- At some point after a user crosses zone lines, their local 3d simulation origin has to shift over to the new tile (0,0,0). We probably don't want to do this at the zone border or else users could flicker back and forth causing their local simulation to rebuild repeatedly. We can instead increase a border around each zone tile and only change them over when they cross that border. There will still be a double change-over scenario at the corners but it won't be at the same point as the network switchover so it will be less apparent if it happens. 
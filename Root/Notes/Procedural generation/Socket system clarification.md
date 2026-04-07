You asked if it’s like lazy loading.

Not exactly.

It’s more like **connection rules**.

Think of Lego pieces with connectors.

Example room:

```id="d16qax"
   N
W [ ] E
   S
```

Each side is a **socket**.

Generator logic:

```id="cwb9v5"
roomA.east_socket
connects_to
roomB.west_socket
```

Then the generator decides what piece goes between them:

```id="33yts3"
wall
door
corridor
stairs
```

---

### Your current idea

You described:

```id="dsr3vh"
Room A → DoorWall → Room B
```

This is already **compatible with sockets**.

Example socket rule:

```id="hy4fbn"
Room socket connects to DoorWall socket
DoorWall connects to another room
```

So your plan is good.

#proceduralGeneration 
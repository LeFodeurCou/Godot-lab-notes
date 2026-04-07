# 1️⃣ The 3 main ways to build mazes in a game engine

These are **engine-level approaches**, not the algorithms themselves.

## A — Grid / Tile Based Maze (most common)

Concept:

```
+---+---+---+
| S |   |   |
+---+---+---+
|   | # |   |
+---+---+---+
|   |   | E |
+---+---+---+
```

You store the maze as **a grid in memory**:

```gdscript
var maze = [
[0,1,0],
[0,1,0],
[0,0,0]
]
```

Then generate geometry from it.

Example:

```
0 = floor
1 = wall
```

Godot then instantiates:

```
FloorFactory.create()
WallFactory.create()
```

### Advantages

✔ Extremely simple  
✔ All classic algorithms work with it  
✔ Easy to debug  
✔ Easy to store / save

### Disadvantages

✖ Naturally square  
✖ Harder to make organic shapes

### Used by

- roguelikes
    
- dungeon crawlers
    
- many indie procedural games
    

**Rating for your lab:** ⭐ **9/10**

---

## B — Graph / Node Maze (rooms connected by graph)

Instead of grid cells you store **rooms as nodes**.

Example:

```
RoomA --- RoomB --- RoomC
   |                   |
 RoomD ------------- RoomE
```

Structure in code:

```gdscript
class Room:
    var position
    var connections = []
```

Maze generation builds the **graph**, then you spawn rooms and corridors.

### Advantages

✔ More natural layouts  
✔ Easy multi-floor structures  
✔ Easy portals / teleports  
✔ Good for procedural worlds

### Disadvantages

✖ Slightly harder to implement  
✖ Harder to visualize in debug

### Used by

- Diablo
    
- Binding of Isaac
    
- many procedural dungeon games
    

**Rating for your lab:** ⭐ **10/10**

Because you already use **rooms + portals**.

---

## C — Incremental / Streaming Maze (on-the-fly)

Maze **doesn't exist fully in memory**.

It grows while the player explores.

Example:

```
Player enters room
↓
Generator creates adjacent rooms
↓
Old rooms unload
```

Typical structure:

```
Player
  ↓
Room Manager
  ↓
Generate neighbors
```

### Advantages

✔ Infinite worlds  
✔ Very low RAM  
✔ Perfect for exploration games

### Disadvantages

✖ Hardest architecture  
✖ Harder to debug  
✖ Requires world manager

### Used by

- Minecraft
    
- No Man’s Sky
    
- procedural infinite games
    

**Rating:** ⭐ **8/10**

Very powerful but **complex early**.

---

# 2️⃣ Maze generation algorithms

Here are the **most important ones**.

---

## Recursive Backtracker (DFS)

### Description

Start at a cell.

```
visit
pick random neighbor
dig path
repeat
backtrack if stuck
```

Example:

```
S -> -> ->
     ↓
     → → E
```

### Best with

Grid approach.

### Game quality

⭐ **9/10**

Produces **long corridors** and natural mazes.

### Complexity

⭐ **7/10 easy**

---

## Prim’s Maze Algorithm

Maze grows like **spreading moss**.

```
start cell
add neighbors to frontier
pick random frontier
connect it
repeat
```

### Best with

Grid.

### Game quality

⭐ **8/10**

Very organic feeling.

### Complexity

⭐ **6/10**

---

## Kruskal Maze

Treat maze like **graph edges**.

```
connect random cells
avoid loops
until all connected
```

### Best with

Graph / grid hybrid.

### Game quality

⭐ **7/10**

More uniform.

### Complexity

⭐ **5/10**

---

## Binary Tree Maze

Simplest algorithm.

Each cell chooses:

```
open north
or open east
```

Example pattern:

```
always diagonal bias
```

### Best with

Grid.

### Game quality

⭐ **4/10**

Predictable.

### Complexity

⭐ **10/10 easy**

---

## Cellular Automata (cave generator)

Used for **caves** rather than classic mazes.

Example:

```
random walls
simulate rules
smooth shapes
```

### Best with

Grid.

### Game quality

⭐ **9/10** for caves  
⭐ **5/10** for mazes

### Complexity

⭐ **6/10**

---

## Wave Function Collapse

Advanced procedural generation.

Rules decide what tiles can neighbor each other.

### Best with

Tile worlds.

### Game quality

⭐ **10/10**

Extremely flexible.

### Complexity

⭐ **2/10 (hard)**

---

# 🧠 For your lab I recommend

Start with:

**Recursive Backtracker + Grid**

Because:

✔ easy  
✔ visual  
✔ you already have walls/floor factories

Then later evolve to:

**Graph rooms generator**

---

# 3️⃣ Your 3 ideas analysis

Your intuition is actually **very good**.

---

## a) Array based maze

Your idea:

```
array or matrix
generate path
fill rest
```

This is literally **how most maze algorithms work**.

Example structure:

```gdscript
var maze = []
maze.resize(width)

for x in width:
    maze[x] = []
    maze[x].resize(height)
```

Cells contain:

```
wall
floor
visited
```

✔ Good idea  
✔ Standard approach

---

## b) Tree structure

Your idea:

```
rooms = nodes
connections = branches
```

That is exactly **graph generation**.

```
RoomA
  ├── RoomB
  └── RoomC
```

✔ Very flexible  
✔ Great for 3D multi-floor

This is how **many modern dungeon generators work**.

---

## c) Generate rooms on the fly

Your idea:

```
place room
add corridor
place next room
repeat
```

That’s **incremental procedural generation**.

Same idea used in:

- Binding of Isaac
    
- many roguelikes
    

✔ Good idea  
✔ slightly harder

#proceduralGeneration
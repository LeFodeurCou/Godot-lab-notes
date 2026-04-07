Two main approaches exist:

### Modular pieces (recommended)

Environment built from reusable modules.

Examples:

```id="0i5l0x"
floor
wall
door wall
stairs
rooms
corridors
```

Used by:

- Diablo
    
- Skyrim dungeons
    
- Dark Souls
    

Advantages:

```id="f0xcr9"
flexible shapes
procedural placement
artist control possible
```

---

### Voxel worlds

World stored as 3D grid.

Example:

```id="l6ydrh"
world[x][y][z]
```

Used by:

- Minecraft
    
- Enshrouded
    
- Teardown
    

Advantages:

```id="x89fwi"
terrain destruction
fully editable worlds
```

Disadvantages:

```id="j7o8ma"
more complex engine
mesh generation required
```

---

## Chunk meshing (voxel optimization)

Voxel engines store **data**, not meshes.

Example:

```id="b9azxg"
chunk[16][16][16]
```

When world changes:

```id="uh7n6f"
update chunk mesh
```

Optimization:

```id="9lgy24"
generate only visible faces
```

Hidden faces between blocks are removed.

#proceduralGeneration 
You said:

> the game load one mesh only instead of X and apply it to identical entities

Yes. Exactly.

More precisely:

Normal approach:

```id="o0ik3g"
1000 MeshInstance3D nodes
1000 draw calls
```

MultiMesh approach:

```id="p8qj7e"
1 mesh
1000 transforms
1 draw call
```

So GPU draws all instances **in a single batch**.

Example:

```id="5hngjb"
forest
grass
rocks
coins
```

All identical meshes.

---

### Limitation

MultiMesh instances **cannot easily have unique scripts**.

So it’s great for:

```id="s53yt9"
decorations
vegetation
repeated props
```

Not ideal for:

```id="zqkgm3"
NPCs
doors
interactable objects
```

  #mesh #optimization 
>A revisit of walls, or even the base building block we need. Can lead to a Minecraft / Hytale world

# 4️⃣ Your cube vs wall concept

Your thinking:

> cube with same dimensions = wall

Yes.

Mathematically:

```
Cube = special case of rectangular prism
```

In Godot terms:

```
BoxMesh(size = Vector3(x,y,z))
```

So:

```
cube  = x=y=z
wall  = x≠y≠z
floor = flat box
```

Meaning you could have **one component**:

```
BlockFactory.create(size)
```

Examples:

```
create(Vector3(2,20,60)) → wall
create(Vector3(60,2,60)) → floor
create(Vector3(2,2,2)) → cube
```

Many voxel engines work exactly like this.

So yes:

✔ conceptually correct  
✔ very flexible

#component 

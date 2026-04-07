>A wall with a space inside like a door

- Can contains a real door later
- For now, just a whole in the whole to let the player pass through
Use a centered [[Door]] to let the player pass through

Inherit from [[Root/Notes/Godot/RoadMap/Done/Components/Orientable]]
# 5️⃣ Wall with a door opening

Your intuition was also correct.

You need **multiple meshes**.

Example wall:

```
█████   █████
█████   █████
█████   █████
```

Structure:

```
Wall
 ├ left_block
 ├ right_block
 └ top_block
```

In code:

```
left wall
right wall
top wall
```

Example door dimensions:

```
wall width = 10
door width = 3
door height = 4
```

Then compute:

```
side_width = (wall_width - door_width)/2
```

Example:

```
[ left ][door][ right ]
```

And above:

```
[ top block ]
```

So you spawn **3 boxes**.

#component 
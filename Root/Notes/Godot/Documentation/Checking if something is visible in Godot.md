### A — Camera frustum culling (automatic)

Godot automatically stops rendering objects **outside the camera view**.

Example:

```id="xlg2ot"
Camera view
   ↓
[object] inside → rendered
[object] outside → not rendered
```

This is **automatic** and you don’t need to code it.

But:

```id="nqv5j4"
object behind another object
```

is **still rendered** unless special techniques are used.

---

### B — Occlusion (hidden behind something)

Example:

```id="w6qpu7"
Wall
|
Object behind wall
```

Some engines detect this and skip rendering.

Godot **does limited occlusion** automatically depending on settings, but not aggressively like voxel engines.

Voxel engines remove hidden faces **during mesh generation**, which is much more efficient.

---

### C — Manual visibility checks

Godot gives tools like:

```id="mx60bp"
VisibleOnScreenNotifier3D
```

Example use:

```id="gk59e0"
object enters screen → activate logic
object leaves screen → disable logic
```

Useful for:

```id="ufv4er"
NPC AI
particles
expensive effects
```

#camera #optimization
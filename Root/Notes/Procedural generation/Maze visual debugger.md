```
extends Node3D

func render(cells):

    for cell in cells:

        var cube = MeshInstance3D.new()
        cube.mesh = BoxMesh.new()

        cube.position = Vector3(
            cell.position.x * 4,
            0,
            cell.position.y * 4
        )

        add_child(cube)
```
# Visualizing Frontier Cells
```
var material = StandardMaterial3D.new()

if cell in frontier:
    material.albedo_color = Color.RED
else:
    material.albedo_color = Color.WHITE

cube.material_override = material
```

```
white = finished cells
red   = frontier cells
```
# Visualizing Connections (Sockets)
```
var mesh = ImmediateMesh.new()
```

```
var line = MeshInstance3D.new()  
line.mesh = CylinderMesh.new()
```

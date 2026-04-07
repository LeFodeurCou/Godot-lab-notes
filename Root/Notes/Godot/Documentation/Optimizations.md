
# 1) Replacing Objects (Vectors) by primitives (integers)

By example for [[Cells]] instead using `var position: Vector2i`, use instead `var x :int, var y:int`

Avoid to create 1 or more position Vector by Cell, lighter the RAM usage

# ~~2) Remove dictionary sockets

~~Instead of having Directions.someVectors we use instead a representation made by integers and basics array

# ~~3) Flatten the grid

~~Instead using an Array of Array for a 2D Map we just use an Array as flatten grid for more velocity

# 4) Avoid array erase in frontier

`.erase()` is a O(n) method

replacing it by a swap-ramove (O(1)) is far better
By example :

```
var last = frontier.size() - 1  
frontier[i] = frontier[last]  
frontier.pop_back()
```

# 5) Replace `pop_front()` queue

```
queue.pop_front()
```

This is **very slow** because arrays shift.

Fast queue

```
var queue = []  
var qi = 0  
  
queue.append(start)  
  
while qi < queue.size():  
  
var current = queue[qi]  
qi += 1
```

This is **10x faster** for BFS.

# ~~6) Avoid frequent `duplicate()`

~~Instead shuffle indexes :

```
var order = []

for i in cells.size():
	order.append(i)

rng.shuffle(order)
```

# ~~7) Preallocate arrays
When possible : 
```
cells.resize(config.cellNumber)
```
Then fill them.

Avoid dynamic growth.

# 8) Reduce object creation (cell pool)

Each `Cell.new()` costs memory + GC.

Later you can use **cell pools**, but not necessary yet.
May be only for objects, not for SoA

# 9) cyclic direction loop

Like this : 

```
	var startDir = rng.randi(0, 3)
	for i in 4:
		var dir = (startDir + i) & 3
		if currentCell.direction != -1 \
		and i == 0 \
		and rng.randf() < config.directionMomentum:
			dir = currentCell.direction
```

Insted of shuffling
# 10) Replace Cell by flat arrays : SoA (Structure of Arrays)
By replacing cells[]
By cellsX[]
cellsY[]
cellsDir[]
etc.
Avoid objects at all cost
# 11) Store indexes instead references
Far lighter
# 12) Use bitmask and bit operations
Avoiding to store arrays of referecences like for sockets
Replacing 1 array per cell containing 4 references is a big improvement
# 13) Using a sparse grid (hash grid)
Storing coordinates as key and idexes as value in one dictionary avoid making an oversized grid and remove the boundaries constraints.
For the key, using a bit operation to store x on the 32 left bits of an int and y on the 32 right bits make a unique key without storing it as string
# 14) Function inlining
Instead of calling a function x times (could be a million of times), making it inline (use the cose from inside the function instead the function itself) can avoit memory stack overhead
# 15) Division by 2
Use a bit operation instead like that :
```
var number = 4
number = number >> 1 (also number >>= 1)
print(number) # will print 2
```

# 16) Use good typing
Instead of making an array like that :
`var array = []`
Which stores in GDScript a Variant (16 bytes)
Use
`var array = PackedInt32Array` which stores only int (8 bytes)
Or even 
`var masks = PackedByteArray` which stores one one byte (8 bits)

Better with fixe sized arrays, else will reallocate more often with `.append()` and `.pop_back()`
# 17) Local affectation
Use as possible local variables from outside classes to avoid many dereferences
# 18) Resize arrays
If the array size is know in advance, use `Array.resize(size)` to make it the wanted size, avoiding reallocation each time using `Array.append(item)`. And then instead of `append`, use indexes from a counter (by example) to store `item`


#optimization
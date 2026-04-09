#roadmap 

# TODO

- Random frontier remover based on the neighbors number
	- 4 : Always removes
	- 3 : Often removes
	- 2 : Sometimes removes
	- 1 : Rarely removes
- Look at more advanced concepts
	- noise fields
	- wave collapse
	- BSP
- Look at : Direction Map
- Add a way to create snapshots that can be reused later
- Make a 3D algorithm
	- Need [[Stairs]] and [[Roof]]
- Make the algo compatible with a chunk generation
	- Look at : border handshake ?
- Cell type can also be an ID (like room-ze6f4ze64) to differenciate each instance from others
- Voronoi biome implementation
	- Biomes can generate some meta data like temperatuer, humidity, height, weridness, magic concentration, corruption etc.
		- Then choosing a biome can become a "simple" mapping from those caracteristics
- **Poisson Disk Sampling**
	- To a more natural distribution of POI (Points Of Interests) like loot, special ennemies, structures etc.
		- Can also be used to place some rooms
- Flow-field vs Direction Bias
	- Each position as it's own direction, dependant by an angle (TAU)
- multi-source generation
	- Instead of 1 starting point → multiple seeds growing and colliding.
		- unlocks
			- continents
			- multiple dungeons merging
			- natural borders
			- faction territories
		- And it plugs directly into the frontier system
- Graph layers
	- Layer 1 — Structure graph
		- current generator
		- topology
	- Layer 2 — Field maps
		- noise
		- flow
		- biome
		- height
	- Layer 3 — Masks
		- rivers
		- mountains
		- zones
	- Layer 4 — Semantics
		- POI
		- gameplay
		- AI zones

# Next step

- 3D algorithm
	- Better room placement
		- may be making the algorithm room first
		- Room must not only be squared (like 3x3 or 5x5)
			- They can collapse to make bigger rooms and allow fancy shapes
	- Compatible chunks
	- Can be multi-source
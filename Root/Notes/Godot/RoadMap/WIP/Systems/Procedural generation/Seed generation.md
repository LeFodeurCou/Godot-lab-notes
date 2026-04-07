>TODO Find a way to make the generation based on a seed
>In Goto it's absurdly simple :

`var inputSeed = 123`
`seed(inputSeed)`
# We can also make a local random generator like
```
var rng = RandomNumberGenerator.new()
rng.seed = seed_value
rng.randf()
rng.randi()
For local randomness like terrain / structures / dungeons / maze etc.
And let the global (or another local) random generator decide for loot, mobs etc.
```
#proceduralGeneration
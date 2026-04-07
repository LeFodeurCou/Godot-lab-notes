For now, my not totally working portals use a direct collision to function, allowing some problems, especially two :
- Infinite loop for some reasons
- Misplacement (like directly going into the void at the arrival)

What about other kind of portals ?

- Minecraft style
	- Player can pass through the portal without any collision or teleport
	- Player have to stay a few seconds (with an animated fading effect) to be teleported into the output portal, at the same "portal position" and the same orientation
	- No infinite loop until the player stay in place, no misplacement
- H&S style
	- Interactable "zone" portals with click (or even a key if needed)
		- No automatic teleport then no infinite loop
		- Arrival ON the portal, then no misplacement
	- "Back" portals, clicable (or with a key)
		- No automatic teleport then no infinite loop
		- Arrival on defined spawn zone (I guess) in towns, then no misplacement
			- However need a place to go back
- World map teleport style
	- Open the world (or local map sometimes), choose a marker and be teleported at or near the choosen position
		- No infinite loop since teleportation happen from a context
		- Misplacement could be a thing if the spawn zone must be in a procedural generation (like check points in any dungeon). However if a spawn is in a fixed zone (like town etc.), the spawn placement avoid that
- Player teleport style
	- As a skill
		- Teleport like a big dash
			- No infinite loop because the player is trigerring it
			- May allow misplacement if we can't check the arrical is ok (travel collisison between some thing like walls, but not like mobs etc., ground check during the teleportation too)
		- Teleport to specific place
			- Like "back portals", or "mark and recall" from morrowind
				- No infinite loop
				- No misplacement (we still have to be careful with the "mark and recall" effects)
- Cinematic teleport
	- Already handled because a "Spawn point" can actualy be extended by anything, thant let the cinematic teleport the player to a next zone
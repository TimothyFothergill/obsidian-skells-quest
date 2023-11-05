
*Start time:* 21:38
**Tags:** #Dungeon #ChestSpawn #Loot

**Story:** 
As the developer, I want to give dungeon chests loot tables,
So that the players have a reason to try to find the chests.

**Acceptance Criteria (as appropriate):**
- Chests have randomised loot.
- Chests drop loot.

**Comments:** 
Created a new data class for LootTables, which contains a list of items and a float value for the chance of getting on that loot table, which is then randomised which item you get from said table.

Also added another int for gold rewards.

Then I added a sphere collider as a trigger and added a script to give the loot on trigger enter.

I added a little bit of flair, by making it so it sends a notification to the scene to show when you've entered and exited the area to loot. This seems to work a treat and has been completed.

*Finish time:* 22:27

*Start time:* 23:29

**Story:** 
As a player, I would like to be able to see quests around me in the game world,
So that I don't need to look at the minimap to understand if the NPC has a quest

**Acceptance Criteria (as appropriate):**
- Quest Icons appear above NPCs heads.

**Comments:** 
First I investigated the existing script used for the minimap. I noticed that, apart from this being on a GameObject that is on the minimap layer, this handles the code for quest icons already.

This ended up being a surprisingly difficult task. The NPC script needed slight tweaking to register the new icon GameObject, but this took a while. In the end, it turned out the way I was trying to initialise the variable was not being read.

The last task on this was to make sure it always faced the player. I created 

*Finish time:* 00:43
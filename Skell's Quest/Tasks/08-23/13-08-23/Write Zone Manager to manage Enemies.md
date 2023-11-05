
*Start time:* 13:40
**Tags:** #ZoneManager #Enemy #Performance 

**Story:** 
As the developer, I want to have a central reference of all of the enemies,
So that I can begin to address some performance issues

**Acceptance Criteria (as appropriate):**
- Write ZoneManager singleton.

**Comments:** 
Wrote a small script that checks all enemies transforms within an infinite squared distance.

Added this to the `DungeonLayout` GameObject and called the new singleton via the `PlayerMovement` script, which needs to be converted to `PlayerController`

*Finish time:* 15:03
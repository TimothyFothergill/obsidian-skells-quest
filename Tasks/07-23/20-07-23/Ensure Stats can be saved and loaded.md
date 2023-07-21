
*Start time:* 22:58
**Tags:** #SaveManager 

**Story:** 
As the developer, I want to be able to save and load stats,
So that the player can resume where they left off

**Acceptance Criteria (as appropriate):**
- Save player stats, levels and xp.
- Load player stats and levels and xp.

**Comments:** 
Further work for this SaveManager system.

I had to save this as a `Dictionary<string, List<int>>` to make this work efficiently. A key of the name of the stat and a list of:
- level
- current xp
- max xp

Tested in various states, this now works.

*Finish time:* 23:23
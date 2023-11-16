---
tags:
  - CombatImprovements
  - PlayerCombat
---

*Start time:* 21:41

**Story:** 
As the developer, I want to completely revamp the player combat script and turn it into a manager,
So states of combat are easier read and controlled

**Acceptance Criteria (as appropriate):**
- Revamp the player combat script.
- Split up big methods into smaller ones.

**Comments:** 
The combat has bugged me for a while, as this one method was about 200 lines long; way too much for one method. Breaking this down will help clarity.

Currently the code works insofar as it's broken down, but animations need to be reapplied. This forms the basis of work tomorrow.

Stopped: 23:04
Started: 13:10

I decided to work on the animation clip work to make it so animations can be applied to each individual skill.

This is now working, but I need to make a couple more animations to ensure it's working correctly.
Combat script is updated, it works, but there's still some extra work to do (like occasionally the enemy apparently being out of range.)

Mostly though it is improved and a significant drop in code (nearly 300 lines removed).

*Finish time:* 15:35
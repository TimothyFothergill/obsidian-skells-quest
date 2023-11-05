---
tags:
  - TargetManager
  - CombatImprovements
---

*Start time:* 21:53

**Story:** 
As the developer, I want to make sure I understand what's happening with targeted skills,
So I can work with them easier in future

As the developer, I want to introduce new types of targeted skills,
So that I can have a more varied gameplay experience

**Acceptance Criteria (as appropriate):**
- Documented understanding of targeted skills.
- New targeted skill working as expected.

**Comments:** 

Two issues were found; terrain wasn't being considered as Terrain; rather its layer was "Default". By switching this back to Terrain and updating the getMouseButtonUp to 0 from 1, this lets me place and use the targeted skills again.

There was an issue for a long time with actually placing the target market - The reason for it was due to a single instance of an incorrect variable being called.


*Finish time:* 23:06
---
tags:
  - UI
  - Timeline
---

*Start time:* 13:46

**Story:** 
As a player, I don't want to see the UI during cutscenes,
Because it is distracting

**Acceptance Criteria (as appropriate):**
- Hide UI during and unhide on completion of a cutscene.

**Comments:** 

This was just a matter of updating the UIManager to add a new ToggleUI() method which accepts a bool. If it's true (default), then it hides all UI. If it's false, it unhides core parts of the UI (Skills, Quick Access, Minimap).

*Finish time:* 14:01
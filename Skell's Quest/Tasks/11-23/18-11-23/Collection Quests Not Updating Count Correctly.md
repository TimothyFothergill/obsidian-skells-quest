---
tags:
  - Quest
  - Fix
---

*Start time:* 00:03

**Story:** 
As the developer, I want to make sure collection quest count correctly,
So they can be handed in and the reward claimed

**Acceptance Criteria (as appropriate):**
- Collection Quests work again.

**Comments:** 
These broke as a result of the inventory changes.

This may have been a one line change...

```c#
int numObtained = PlayerManager._instance.GetInventory().Find(o => o.item == i.item).qtyStored;
```

*Finish time:* 00:10
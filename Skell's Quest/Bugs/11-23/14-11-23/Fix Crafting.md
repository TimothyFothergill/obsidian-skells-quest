---
tags:
  - Crafting
---
*Reported time:* 21:57
*Start time:* 21:57

**What I fixed:**
Crafting prefabs are not being instantiated correctly on the crafting screen.

**Comments:**
Realised this would be down to the fact that inventory is currently broken. For instance, shop loads on one side, but not the inventory side.

Fixed the inventory problem; turned out there was a missing value, which prevented any item ever being populated in the inventory.

Material drops were broken as now all items are kept in a Resources folder. This means all prefabs need to be repopulated with the ScriptableObject from the relevant places. This can take a while, but this only affects prefabbed items.

*Finish time:*
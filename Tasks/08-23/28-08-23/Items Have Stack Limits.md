
*Start time:* 09:30
**Tags:** #Inventory

**Story:** 
As the developer, I want to make sure all items have a stackable limit,
So that players can hold multiple items per slot.

**Acceptance Criteria (as appropriate):**
- Items now have stacks, with a 99 default stack limit for normal items and 1 for equipment. ✅
- Inventory Slots can hold a stack of items. ✅
- Stacks of items can be upgraded.

**Comments:** 
Some noodling through three main scripts - The `ItemBase` script handles the bulk of the work, the `Equipment` script as they are a separate entity and the `CSVToGameObject` script which is part of the tooling.

Paused: 10:21
Resumed: 21:01

Some more noodling is needed around adding and removing from each inventory stack. But this refactor is nearly done.

*Finish time:* 22:02
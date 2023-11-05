
*Reported time:* 10:35
*Start time:* 10:35
**Tags:** #Bug 

**What I fixed:**
If you have 1 of each item, if you need more than one of one of the items instead, it'll still craft and tell you that you don't have enough.

**Comments:**
This is a fiddly issue going into multiple facets:
- Player inventory count
- Player bankslot count
- Player bankslot qty
- Multi-craft

Fixed inventory-only, however it now gives the item and says "need more items to craft this" after. Stopping for a bit, but will return to this today, as this is one of the few "new" bugs to be fixed before releasing this version of the game.

Stop time: 11:15
Start time: 13:15

Toggle does not provide a boolean, rather Toggle.isOn does... Oops.

Now all checks are done in both bank and inventory, with a bool value for whether or not to use the bank.

This needs to be resumed later, as this is a large-scale bug that affects the entire crafting system.

Stop time: 15:26
Start time: 22:00

This was a very hard problem to resolve - It turned out that removing multiple of the same type of item was being held back by an issue with the item removal.

*Finish time:* 23:30

*Reported time:* 21:30
*Start time:* 21:30
**Tags:** #Bug 

**What I fixed:**
The tooltip appears over the cursor in the bank

**Comments:**
Made a temporary solution - a bool value on the InventorySlot script which by default is false. In the bank scene, they're set to true. This pushes the tooltip a bit further out.

*Finish time:* 21:31
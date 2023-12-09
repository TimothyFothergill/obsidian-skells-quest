---
tags:
  - Quest
  - Bug
  - NotStarted
---
*Reported time:* 22:12
*Start time:* 

**What I fixed:**
If you destroy an item from the inventory once a quest is ready for completion, the game will try to complete, taking all items away from you in the process. Oops!

**Comments:**
On the quest controller I added a check to flip the bool if it's not actually complete:
```c#
if(numObtained >= i.numberOfItems) {
	QuestCompleted();
} else {
	completed = false;
}
```

*Finish time:* 22:16
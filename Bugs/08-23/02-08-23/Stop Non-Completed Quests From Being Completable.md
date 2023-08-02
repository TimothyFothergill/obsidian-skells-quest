
*Reported time:* 08:14
*Start time:* 08:14
**Tags:** #Bug 

**What I fixed:**
When you complete a quest, all quests could be completed.

**Comments:**
This was a matter of just doing an extra check:

```c#
if(controller.GetQuestCompletion() && controller.quest.GetQuestTitle() == q.GetQuestTitle()) {
```

*Finish time:* 08:24
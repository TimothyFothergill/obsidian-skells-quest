*Start time:* 13:32

**Story:** 
As the developer, I want to add the quest icon to each ActiveQuest Prefab that's instantiated,
So that players can get a bit more context behind each of their active quests

**Acceptance Criteria (as appropriate):**
- Add an Image GameObject to the ActiveQuest prefab.
- Add corresponding code to ensure this icon gets populated correctly.

**Comments:** 
This was a straightforward task, where I added an Image GameObject to an existing prefab.

I then needed to add a single line to the ActiveQuestsPanel script:
```c#
obj.transform.GetChild(2).GetComponent<Image>().sprite = q.GetQuestSprite();
```

*Finish time:* 13:36
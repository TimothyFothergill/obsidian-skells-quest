
*Start time:* 13:28
**Tags:** #SaveManager 

**Story:** 
As the developer, I want to make sure that any unlocked abilities are unlocked properly,
So that players can load their abilities without having to re-unlock them.

**Acceptance Criteria (as appropriate):**
- Make sure loaded save files will load the unlocked abilities properly.
- Stop trainers from trying to train an ability unlocked by loading.

**Comments:** 
This started with a simple task of fixing last night's work - I just added a new for loop to check against every learned ability and whichever abilities were not already in the list gets added.

```c#
foreach(Ability a in loadedAbilityList) {
	if(!listToUpdate.Find(o => o.name == a.name)) {
		listToUpdate.Add(a);
	}
}
```

However this wasn't working as expected because it was adding an Ability which didn't exist. D'oh!

This ended up being because I had two versions of each ScriptableObject. One in a resources folder and one outside. The one outside was being referred to yet the one inside was being used elsewhere. Replaced all the ones outside with the ones inside to fix.

*Finish time:* 15:16
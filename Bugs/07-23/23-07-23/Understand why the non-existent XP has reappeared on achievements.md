
*Reported time:* 10:25
*Start time:* 10:25
**Tags:** #Bug #Achievements 

**What I fixed:**
A non-existent PlayerStat has appeared when getting a level via achievements:

![[Pasted image 20230723102626.png]]

**Comments:**
A few fundamental changes to the way the _\_xpReward_ value of an achievement works. I turned it into a list so you can get multiple xp rewards from an achievement. I then changed where the xp is set, taking it out of the `SerializedPlayerExperienceReward` structs constructor method.

*Finish time:* 10:34
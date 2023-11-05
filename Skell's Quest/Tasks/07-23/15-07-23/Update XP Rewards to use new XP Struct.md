
*Start time:* 10:35

**Story:** 
As the developer, I want to be able to use the new XP Struct when rewarding XP,
So that I can programmatically award players XP with less room for error.

**Acceptance Criteria (as appropriate):**
- Change XP reward scripts to use the new XP Struct.

**Comments:** 
This is a simple task - I just needed to add a new override for the AddToXP method, which would accept the struct:

```c#
    public void AddXPToStat(SerializedPlayerExperienceReward expStruct) {

        expStruct.stat.AddXP(expStruct.value);

        NotificationManager._instance.AddNotificationToQueue(new NotificationMessage("+" + expStruct.value.ToString() + " " + expStruct.stat.GetStatName(),type:NotificationType.XP,st:expStruct.stat));
	}
```

*Finish time:* 10:45
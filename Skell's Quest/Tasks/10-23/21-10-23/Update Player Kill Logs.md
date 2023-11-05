---
tags:
  - PlayerKillLogs
---
*Start time:* 23:56

**Story:** 
As a player, I want to be able to see what drops an enemy type has remaining for me to get,
So that I can focus on efficiently killing enemies and bosses as I see fit.

**Acceptance Criteria (as appropriate):**
- New Bestiary UI.
- Player Kill Log brings up notifications when new items are dropped.
- Player Kill Log brings up notifications when kill milestones are met.

**Comments:** 
At the moment, enemies are hard coded to get an EnemyLog:

```c#
    List<EnemyLog> log = new List<EnemyLog>();
	[SerializeField] Enemy gobob;
    [SerializeField] Enemy goboboss;
    EnemyLog gobobLog;
    EnemyLog gobobossLog;

	void Start(){
        EnemyLog gobobLog = new EnemyLog(gobob);
        EnemyLog gobobossLog = new EnemyLog(goboboss);
        log.Add(gobobLog);
        log.Add(gobobossLog);
    }   
```

Now the code has been updated to automatically grab all enemies from `Prefabs/Resources/Enemies`. More work is needed here, but due to how late it is, stopping for the night. Here's the updated code for all drop logs:

```c#
	foreach(Enemy e in Resources.LoadAll<Enemy>("Enemies")) {
		log.Add(new EnemyLog(e));
	}
```
**NOTE:** This does mean that Enemy data will need to be in a resources folder going forward. Another solution might be to implement a Dictionary list of all Enemies, but this solution feels simpler and less error prone.

Stop: 00:41.
Resume: 09:40

This ended up being a fairly straightforward task. 

```c#
[Serializable]
class DropLogEntry {
    ItemBase _itemBase;
    bool isUnlocked = false;

    public DropLogEntry(ItemBase i) {
        _itemBase = i;
    }

    public bool unlocked => isUnlocked;
    public ItemBase item => _itemBase;
    public void Unlock() => isUnlocked = true;
}
```

I made a `DropLogEntry` class which is just a simple class that handles whether an item has been received at least once. By passing in an ItemBase, it automatically sets it up for that enemy.

```c#
    public void DropLogEntryUnlocked(ItemBase itemBase) {
        DropLogEntry foundDropLogForItemBase = drops.Find(o => o.item.GetItemName() == itemBase.GetItemName());
        if(foundDropLogForItemBase != null && !foundDropLogForItemBase.unlocked) {
            foundDropLogForItemBase.Unlock();
        }
	}
```

I then just had to make a simple find method for the item in the list of `DropLogEntry`. If it finds it, then it checks if it's not unlocked yet - and if not, it unlocks it.


*Finish time:* 10:54
---
tags:
  - Managers
  - Singletons
---
*Start time:* 13:39

**Story:** 
As the developer, I want to minimise duplicated code by making a generic singleton,
So that I only need to extend the base manager class as a generic

**Acceptance Criteria (as appropriate):**
- Make a generic Manager singleton class.
- Test all managers work.

**Comments:** 
As an idea, I decided to turn my managers into a generic base class which can be extended by all managers.

```c#
using UnityEngine;

public class ManagerSingleton<T> : MonoBehaviour where T : Component
{
    public static T _instance {get; private set;}
    void Awake() {
        if(_instance != null && _instance != this as T){Destroy(this as T);}else{_instance = this as T;}
    }        
}
```

This then replaced the MonoBehaviours of most Singleton ('Manager') classes.

This has been tested to work; however there's some bugs around some of the features in previously working areas. This may have been caused by other problems, however - Such as Quests trying to add ItemBase to inventory, not an ItemBase added to an InventoryData's item slot.

Implementing this was as simple as:

```c#
public class ExampleManager : ManagerSingleton<ExampleManager> 
{
	// do stuff
}
```

This means that approximately 50 lines of code have been cut by this small, but significant change.

*Finish time:* 14:05

*Reported time:* 08:20
*Start time:* 08:20
**Tags:** #Bug 

**What I fixed:**
If multiple of the same notification appears, I allowed it to come up multiple times.

**Comments:**
This was as simple as changing one variable. The only downside to this approach is for some notifications that are triggered multiple times.

I then fixed this by adding a flag to the FriendlyBorderZone and HostileBorderZone scripts and an IEnumerator:

```c#    
IEnumerator ToggleNotificationFired() {
        yield return new WaitForSeconds(1);
        notificationFired = false;
    }
```
*Finish time:* 08:33
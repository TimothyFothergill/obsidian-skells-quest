
*Reported time:* 12:49
*Start time:* 12:49

**What I fixed:**
Minimap appears to have started spinning with the player again.

**Comments:**
At first I thought this meant that a script had reattached to the minimap, but this doesn't appear to be the case. Instead, there was a duplicated minimap camera which was taking priority and that one didn't have the script. Removed the duplicated minimap and made sure script was attached.

*Finish time:* 12:52
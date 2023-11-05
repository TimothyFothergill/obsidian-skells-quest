
*Reported time:* 09:01
*Start time:* 09:02
**Tags:** #Bug 

**What I fixed:**
Enemies were attacking from any distance, so I needed to find why they were attacking from everywhere.

**Comments:**
It turned out that the `distance` variable was always less than the threshold of `distance >= playerPosition +1`, because it was commented out.

*Finish time:* 09:05

*Reported time:* 10:34
*Start time:* 10:34

**What I fixed:**
There was an issue with the in-world NPC icons, where they were not correctly aligned, making for a confusing experience. 

**Comments:**

![[Pasted image 20230625105235.png]]
This was just because the child Canvas element's anchor was set to bottom left. Setting the anchor to centre middle and updating the position of x and z to 0 fixed this.

*Finish time:* 10:41
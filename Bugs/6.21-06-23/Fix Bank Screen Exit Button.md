
*Reported time:* 23:19
Start time: 08:25

**What I fixed:**
For some reason the bank screen button wasn't working. I first thought this meant the Exit button had dropped the reference to the exit script, but this wasn't the case.

**Comments:**

This ended up being a strange error caused by trying to move the UIManager into its own UIManager GameObject. However, I noticed that I never removed the old UIManager. Reenabling the old one fixed this bug. 

This is a strange one, as no functionality looks for where the UIManager is set. Will need to investigate this further in the future.

*Finish time:* 08:29
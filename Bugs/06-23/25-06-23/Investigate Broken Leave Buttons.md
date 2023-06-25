
*Reported time:* 23:23
*Start time:* 23:23

**What I fixed:**
A lot of UI Buttons that leaves a screen would no longer leave the screen they were in.

**Comments:**
First thing I checked was that the buttons correctly had the UIManager set up on them and they were utilising the correct `CloseAllPanels()` method. At some point, the UIManager script was moved, but this caused bugs so it was moved back. During this, the buttons seemed to have lost reference to the method. Readding this to all of the Leave buttons fixed this bug.

*Finish time:* 23:30
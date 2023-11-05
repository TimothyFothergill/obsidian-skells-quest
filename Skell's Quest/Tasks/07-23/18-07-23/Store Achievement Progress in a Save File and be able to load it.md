
*Start time:* 22:39
**Tags:** #SaveManager 

**Story:** 
As the developer, I want to be able to save achievements earned,
So that players can reload the game with their achievements in tact.

**Acceptance Criteria (as appropriate):**
- Save achievements to the cloud.
- Load achievements from the cloud.

**Comments:** 
I first thought the work for this was not too dissimilar to other tasks, but I was targeting the wrappers. This may, or may not be an accurate way to handle this, so needed to test the save process first. I made the achievement area a lot bigger to make this happen faster for testing.

In the end, after some testing, sending the wrapper to be collated ended up being a bad idea. Instead, I just set it so there's a list of strings, being the name of the achievement, then compared each achievement in the list to the achievement names in wrappers.

*Finish time:* 00:36
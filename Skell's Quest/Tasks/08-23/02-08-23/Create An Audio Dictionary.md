
*Start time:* 08:29
**Tags:** #Audio #Dictionary

**Story:** 
As the developer, I want to make an Audio Dictionary,
So that audio can be loaded by examining the name of the scene

**Acceptance Criteria (as appropriate):**
- Create an Audio Dictionary to allow swapping audio based on the name of the scene.

**Comments:** 
This was a strange one - Instead of making it as a Dictionary, I had to make it as a regular Array and use a struct to make this work as expected.

The struct allows me to pass through the AudioSwapper the name of the current Scene. It will also allow me to pass through a string to meet the other audio clips.

*Finish time:* 08:55
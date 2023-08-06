
*Start time:* 18:10
**Tags:** #Dungeon #Camera

**Story:** 
As the developer, I want to implement a First Person Camera system for tight spaces,
So that the players get an interesting juxtaposition of views and angles.

**Acceptance Criteria (as appropriate):**
- Implement a First Person Camera.
- Ensure FPC can be triggered with an isTrigger based collider.

**Comments:** 
This was a straightforward process.

I made a Manager to handle these types of swaps in future. I just had to create a second camera and swap the priority.

I then set up some colliders and made it so when Skell walks into one of the triggers, depending on the intent, it'll switch between modes.

*Finish time:* 18:29
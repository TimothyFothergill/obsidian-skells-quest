
*Start time:* 08:23
**Tags:** #Performance

**Story:** 
As the developer, I want to determine whether the frame rate issues I'm having are due to the game,
So I don't release an unoptimized game

**Acceptance Criteria (as appropriate):**
- Determine source of performance hit.

**Comments:** 
The source appears to be the enemies.

4 enemies are placed near one another. It could be they're all running checks.

Having looked around - I've found the issue is with the isTrigger collider. It is constantly checking for a collision it cares about.


*Finish time:* 
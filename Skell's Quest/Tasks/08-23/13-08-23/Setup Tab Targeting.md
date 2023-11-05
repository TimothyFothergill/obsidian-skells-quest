
*Start time:* 22:56
**Tags:** #Targeting #Performance #ZoneManager #TargetManager

**Story:** 
As a player, I want to be able to tab between targets,
So that I can have a much smoother gameplay experience

**Acceptance Criteria (as appropriate):**
- Make tab targeting work.

**Comments:** 
This was a pretty simple script; using the foundations of the previous script, I'm able to pass a GameObject through, which would be the current target (obtained by the `TargetManager`).

This then lets me compare the next closest that is not the main target.

This can be improved further later, but for now this lets players cycle between two targets and move closer to other targets to redirect that focus.

*Finish time:* 23:20
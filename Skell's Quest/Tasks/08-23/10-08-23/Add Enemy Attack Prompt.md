
*Start time:* 12:55
**Tags:** #Enemy #PopupUI

**Story:** 
As a player, I would like to be aware when an enemy attacks me and with what,
So that I can make an informed decision about my next move.

**Acceptance Criteria (as appropriate):**
- Popup that automatically clears itself after a period of time.
	- Popup to show icon and name of the skill.
	- Popup to appear above the enemy.

**Comments:** 
Started by putting together a simple GameObject which I turned into a prefab. This is a canvas with a TextMeshProUGUI object on it and an Image object.

Added a new method in the Enemy script to handle creating these popups.

Added a small script to make it destroy themselves after 1.5 seconds. Also an animation that makes them bounce on the screen.

*Finish time:* 13:35
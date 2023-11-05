
*Start time:* 23:19
Tags: #SaveManager 

**Story:** 
As a player, I would like the game to remember my progress when I save,
So that I don't need to restart it every time.

As the developer, I would like to add more properties to the save state of Skell's Quest,
So that players don't chase me down with a pitchfork.

**Acceptance Criteria (as appropriate):**
- Add more properties to the save game data.
- Ensure this can be loaded correctly.

**Comments:** 
Currently only the bank saves, so decided to up the ante and add inventory states tonight.

I managed to do the save implementation really quickly. This was just a matter of adding the new types to the player's save data. Accessing each part is also straight forward... However...

... When working on inventory (and even the bank), I noticed there's an issue with the data of the scriptable objects. I need to create a system that stores every saveable asset on starting runtime and can find the asset as required.

*Finish time:* 00:05
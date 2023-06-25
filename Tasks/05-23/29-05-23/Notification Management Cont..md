*Start time:* 10:15

**Story:** 
I want to write a notification management system
So that my players can have multiple notifications appear and disappear simultaneously depending on context of what the notification is.

**Notes:**
Currently I am using a UIManager to write messages to the screen. This is fine, but it looks naff and it's a lot of reliance on the UIManager, when I want to decouple in-game notifications from UI to its own manager.

**Acceptance Criteria (as appropriate):**
- A notification system that can replace the current UI Manager notification system.
- Different notification types (Standard, Level up, etc).
- Notifications that have different timings.
	- Overrides are possible.
- Notifications that have different GameObjects.
	- Overrides are possible.
- Notifications that have different animations.

**Comments:**
Yesterday I encountered an issue where the background of the Level Up Notification wasn't coming through. It turns out, the Left and Right being set to 500 was exactly big enough to hide the background.

All existing prompts have been changed into a standard notification, apart from level up which is now a working level up notification @11:47.

Need to add in a `bool` for each notification being sent via OnTriggerEnter.

Just need to make the xp notifications now.

*Finish time:* 15:30

*Breaks:*
- 10:30-11.20 (50 mins)
- 11.40-14:00 (80 mins)

Notes:
Didn't get it all complete today, but just need to fix the NPCs, Borders and then make the XP Notification type.
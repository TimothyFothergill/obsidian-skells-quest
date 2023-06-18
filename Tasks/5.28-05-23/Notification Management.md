*Start time:* 10:20

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
I started the basis of the notification management system yesterday and only spent about 15 minutes on it. The idea right now is to prove that notifications can go into the system and manage itself.

Can't use the new keyword on a class that is a MonoBehaviour. MonoBehaviour has been given to the NotificationMessage class which is being used to handle notifications and managing their state. Constructor needed.

Made an empty component called MonoScript, which allows us to derive from MonoBehaviour without the class needing to be a MonoBehaviour.

Designed the containing GameObject for standard notifications - Simple panel with a text object.
Designed the containing GameObject for Level Up notifications - Fancy box with the stat icon, "Level Up" and the stat increase.

*Finish time:* 20:35
*Breaks:* 
- 10:37-10:42 (5 mins)
- 10:52-12:12:30 (98 mins)
- 14:40-14:50 (10 mins)
- 16:30-20:15 (195 mins)

Notes:
Lots of progress made today, got it working with Standard Notifications and Level Up Notifications. Just need to make the XP Notifications and understand why Level Up isn't working as well as I'd like.
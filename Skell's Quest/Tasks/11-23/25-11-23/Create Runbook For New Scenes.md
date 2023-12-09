---
tags:
  - Scene
  - Runbook
---
*Start time:* 20:09

**Story:** 
As the developer, I want to make a runbook that will cover all of the required setup for a new scene,
So that I may later be able to easily automate the process with a Scene Template and have knowledge of what's required in each scene.

**Acceptance Criteria (as appropriate):**
- Understand process for a completed new scene.
- Create runbook.

**Comments:** 
GameObjects present in Valley of Elders:
- Banks
	- GameObjects with:
		- Sphere Collider Radius 2
		- Mesh Collider for collision detection
		- Bank Object component
- Cutscenes
	- GameObjects with:
		- PlayableDirector components - These store the Timeline animations.
- {Name-of-Scene}
	- GameObjects that make up the world space
	- Can have a dedicated GameObject for various things like:
		- Craft Stations
		- Signs
		- Lore Books
		- Craft Zones
		- NPCs
		- Location Criterias
- Spawn Points
	- GameObjects with a box collider - is picked up by other scripts currently
- Cutscene Cameras
	- Any additional cameras made for a cutscene are plopped in here
		- Name them well :(

There are also 3 objects that are passed between scenes:
- Main Camera
- Player
- Data

Data contains all the managers etc.

*Finish time:* 21:05
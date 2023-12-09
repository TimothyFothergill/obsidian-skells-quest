These GameObjects are required and the types of GameObjects that live within them:

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
- Data - Data contains all the manager objects etc.

If you need to test a new scene for collisions, testing and more, just copy those three objects over, test the scene out and make sure you can get to the scene from other scenes.

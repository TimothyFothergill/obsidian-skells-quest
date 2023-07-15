
*Start time:* 11:03

**Story:** 
As a player, I would like to see a world filled with life,
So that I don't think the world is so dull

As the developer, I want to make the impious buns move,
So that the world feels more alive.

**Acceptance Criteria (as appropriate):**
- Make the impious buns move properly.

**Comments:** 
At the moment, the Impious Buns cause warnings under the hood whenever they're spawned. This is because it doesn't recognise what they're supposed to be doing in terms of movement.

The NavMeshAgent (NMA) was too high on the object. Plus, the NMA was active when spawned and the GameObject is dropped from the air. Deactivating this in the prefab then starting it in a script.

This was a complicated problem with multiple layers:

1. NMA only appears to support humanoid?
	1. The fix may be to bake in each non-humanoid NMA - navigation > Bake.
2. The movement script was only registering one point and never continuing.
3. Too many buns makes it hard to manage.

Paused: 11:30
Started again: 12:25
*Finish time:* 14:46

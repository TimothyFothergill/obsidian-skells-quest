---
tags:
  - Skills
  - Line-of-Sight
---
*Start time:* 22:48

**Story:** 
As the developer, I want to make sure that line of sight skills and aggro is affected by obstacles,
So that skills and aggro can be affected by placement of obstacles on the map.

**Acceptance Criteria (as appropriate):**
- Ensure aggro and LoS skills are affected by obstacles.
- Introduce a new "line" skill which is affected by obstacles.

**Comments:** 
The line skill will be a simple skill that hits the ground in a line. If it encounters a wall, it must stop.

```c#
        NavMeshHit hit;
        if(!agent.Raycast(target, out hit)) {
            playerVisible = true;
        } else {
            playerVisible = false;
        }
```

For the enemy I can make use of the agent.Raycast function to determine whether it should look for the player or not. 



*Finish time:* 
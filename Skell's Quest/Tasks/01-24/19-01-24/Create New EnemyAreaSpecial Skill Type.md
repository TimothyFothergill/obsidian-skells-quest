---
tags:
  - CombatImprovements
  - Skills
  - Enemy
---
*Start time:* 22:26

**Story:** 
As the developer, I want to create a new EnemyAreaSpecial skill type,
So that enemies can utilise new, interesting mechanics for players to play against

**Acceptance Criteria (as appropriate):**
- New skill type added to the game.

**Comments:** 
The new skill type needs to have the following:
- A customisable amount of 'spikes', which are GameObjects which will have something associated to them (animation, particle etc).
- For each spike, the skill needs to sequentially work through them, taking a variable amount of time for the length of each spike.
- The ability to make the enemy invulnerable during this period.
- The ability to make the enemy disappear during this period (jump off screen, etc).

Further improvements to make after is to be able to alter the damage per spike, to change the size per spike etc.

Started by making a new class which inherits `Skill` of `EnemyAreaSpecial`.

```c#
[CreateAssetMenu(fileName = "New Enemy Area Special", menuName = "Skills/Enemy/Area Special")]
public class EnemyAreaSpecial : Skill {
    [SerializeField] int radius;
    [SerializeField] int time;
    [SerializeField] GameObject groundObject;
    [SerializeField] List<GameObject> spikes;

    public override void EnemyAttack(EnemyStats stats = null) {
        foreach(GameObject spike in spikes) {
            Instantiate(groundObject, spike.transform,true);
        }
    }
```

*Finish time:* 
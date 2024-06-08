---
tags:
  - Enemy
  - CombatImprovements
---
*Start time:* 13:06

**Story:** 
As the developer,
I want to refactor the Enemy Update method,
So that it is easier to understand in future

**Acceptance Criteria (as appropriate):**
- The Update method is fully refactored.

**Comments:** 
```
    // void Update()
    // {
    //     if(isGoingHome && CheckDestinationReached(transform.parent.position) && !isHome) { isHome = true; isGoingHome = false; } else { isHome = false; }
    //     float distanceFromHome = Vector3.Distance(homePosition, transform.position);
    //     if(distanceFromHome >= 6f) {
    //         b_inCombat      = false;
    //         isInRange       = false;
    //         isGoingHome     = true;
    //         agent.SetDestination(homePosition);
    //         return;
    //     }
    //     if (distance <= aggroRadius && distance > agent.stoppingDistance && playerVisible) {
    //         //  stats.GetAggroType() != EnemyAggroType.NEUTRAL
    //         isInRange       = false;
    //         b_inCombat      = true;
    //         if(TargetManager._instance.GetTarget() == null) { TargetManager._instance.SetTarget(this); }
    //         agent.SetDestination(target);
    //         animator.SetBool("isMoving", true);
    //         StopCoroutine(FightPlayer());
    //     } else if(distance <= aggroRadius && distance > agent.stoppingDistance && !playerVisible) {
    //         //  stats.GetAggroType() != EnemyAggroType.NEUTRAL
    //         isInRange       = false;
    //         b_inCombat      = true;
    //         if(TargetManager._instance.GetTarget() == null) { TargetManager._instance.SetTarget(this); }
    //         agent.SetDestination(lastKnownTarget);
    //         animator.SetBool("isMoving", true);
    //         StopCoroutine(FightPlayer());
    //     }
    //     if(distance > aggroRadius && !isHome && !isGoingHome) {
    //         b_inCombat      = false;
    //         isInRange       = false;
    //     }
    //     if (distance < agent.stoppingDistance && !isGoingHome) {
    //         isInRange   = true;
    //         animator.SetBool("isMoving", false);
    //         if(!b_inCombat && !gcd) {
    //             b_inCombat = true;
    //             StartAggroInteraction();
    //         }
    //         if(b_inCombat && !gcd && !is_thinking && isInRange) {
    //             b_inCombat = true;                
    //             StartCoroutine(FightPlayer());
    //         }
    //         TurnToTarget();
    //     } else {
    //         if(!b_inCombat && !isHome && !isGoingHome) {
    //             StopCoroutine(FightPlayer());
    //             StopAggroInteraction();
    //             animator.SetBool("inCombat", false);
    //         }
    //     }
    //     nextFrameTarget = PlayerManager._instance.GetPlayerPosition();
    // }
```

*Finish time:* 
---
tags:
  - Personal-Blog
---
Enemies, especially bosses, occasionally need special mechanics to make them stand out. I decided my first boss, even though it will change in the long run, needed to have at least one special mechanic. I wasn't sure of the best way to implement this, so I decided to flesh out my thinking behind a special attack for a large slime creature. The answer was Toxic Pools - Here's what I did.

# The Thinking Behind The Skill

Bosses are great because they keep us on our toes. If you're a melee user, you should always be prepared for a large hit. If you're ranged, perhaps you need to stand in a specific position in order to reach the enemy, or to just avoid big hits. Whatever style you choose, you need to think about where to stand and whether you can keep hitting the enemy.

I wanted to have a skill which players will need to react fairly quickly to, or else take damage that scales over time. This made me wonder how on earth this would best be done - and I realised I could just leverage an empty GameObject which gets a Transform component for free. From there, I could spawn some effects and treat it so if the player is standing in the AOE in that time, then the player will just take damage the longer they're in there for.

![The Hierarchy For Static Moves](https://i.ibb.co/6P10NF3/Toxic-Pools-Static-Locations.png)

## Unity Particle System

One system I've messed around with very briefly before is the particle system. It seemed pretty complicated the first time I looked at it, so I only made very simple particles. This time around, I wanted to make an actual combat effect out of the particles, so it is at least obvious what areas are going to be affected by the AOE ground static attacks. After all, a player can only react to an effect if they can see it as it's coming in.

I learned that a lot of Unity VFX designers will use several GameObjects, all of which have the Unity Particle component attached to them. This means that each effect is done separately, allowing for some of it to be static, some of it to be more random.

![Toxic Pools Particles](https://i.ibb.co/kSM4Sgg/Toxic-Pools-Particles.gif)

## How Does It Piece Together?

I already had a base for skills in the game - Enemies and the player share the concept of skills. If I make a skill and give it to an enemy, it just calculates that the damage goes to the player. So I needed to extend my existing Skills to add in an Enemy Static Special AOE type. This was an easy process I've done a few times before:

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

[CreateAssetMenu(fileName = "New Enemy Area Special", menuName = "Skills/Enemy/Area Special")]
public class EnemyAreaSpecial : Skill
{
    [SerializeField] int radius;
    [SerializeField] int time;
    [SerializeField] GameObject groundObject;
    [SerializeField] Animation warmupEffect;
    [SerializeField] List<GameObject> spikes;
    [SerializeField] bool isInstant;
    [SerializeField] float startDelay = 2f;
    
// The main thing to note here is this just overrides my base Skill class which contains all of the information for damage calculation and more. Then when the attack starts, it spawns the GameObjects responsible for handling the damage etc, which is all handled in the EnemyAreaSpecialSpike class
    public override void EnemyAttack(EnemyStats stats = null) {
        foreach(Transform spike in GameObject.Find(name).transform) {
            GameObject obj = Instantiate(groundObject, spike.position, groundObject.transform.rotation, spike);
            EnemyAreaSpecialSpike special = obj.AddComponent<EnemyAreaSpecialSpike>();
            special.StartSpike(startDelay, this);
        }
    }

    public int area => radius;
    public int        duration      => time;
    public GameObject groundEffect  => groundObject;
    public float      delay         => startDelay;
    public bool       instant       => isInstant;
}
```

## What's Next?

I've got to make a few more changes before I can say it's fully implemented, but the damage works and the particles, albeit basic, work pretty well. I'm happy with how quickly I was able to throw this together, so here's hoping the rest of the development of the boss goes well.

I just need to understand why the boss decides to spin around randomly and fail to actually attack the player... But once that's understood, then I can add a different UI for boss fights and add in invulnerable states during that static mechanic. I then need to sort out the attributes so they don't get overtuned versus the boss. A lot of work to go, a lot of which I'm hoping to blast through this weekend.

That's it for another week, thanks for keeping up with me so far. Every week this patch is getting closer and closer - and then I can begin work on making a lot of assets. There'll be a lot of problems with the game even when this version's been released, but at least I'm making progress every week.

Until next time folks, much love and happy tinkering - 
 Timlah
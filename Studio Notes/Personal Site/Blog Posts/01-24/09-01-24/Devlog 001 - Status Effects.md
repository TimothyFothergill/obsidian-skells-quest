---
tags:
  - Personal-Blog
---
I haven't really shared much about the progress of the latest patch of Skell's Quest, apart from saying "I've done some things". My goal for the year is to get the game to a fully playable state, before working on assets for a long time. It's mostly there, but there's a bunch of things to improve, such as combat. As part of a regular series I will be running here, I will go over design decisions in Skell's Quest.

# How Do My Status Effects Work?

In principle, a status effect is often listed as a buff or debuff against a target. In this case, I wanted to work on just two of the core status effects you'd expect to see in a game:

- Paralysis
- Poison

![Poison applied to a Gobob](https://i.ibb.co/XV9GmFr/Poisoned-Effect.png)

Given this, I figured I could just make these the same as skills in my game and just change the numbers based on the attributes the player has. For instance, perhaps paralysis duration could be tied to your strength, whereas poison could be tied to your constitution.

I figured this wouldn't scale well, so instead decided to change this on a skill-by-skill basis. I just needed to add a few more lines to the skills in order to set a status effect... Except there's a problem going down this approach. 
## The Way My Skills Work

I decided to use Scriptable Objects to handle being skills for me. The skill types are as follows:
- Single
- Targeted
- Buff
- Debuff
- Heal
- AOE
- Ground
There's room for other types in the future too. The problem here is only the `Buff` and `Debuff` skill types are added to the target/player. These get a coroutine added to them, checking for when those buffs and debuffs resolve. So I needed to make a field that would apply a different skill, specifically a `Debuff` in the case of `poison` and `paralysis`.

```
if(poison) {
	Debuff poisonDebuff = StatusEffectManager._instance.Poisoned(poisonDuration,poisonTickInterval,poisonTotalDamage,enemy);
	if(enemy) {
		PlayerManager._instance.SetPoisoned(true);
		BuffObject bObj = GameObject.Find("Player").AddComponent<BuffObject>();
		bObj.SetDebuff(poisonDebuff, true);
	} else {
		TargetManager._instance.GetTarget().TogglePoisoned(true,poisonDuration);
		BuffObject bObj = TargetManager._instance.GetTarget().gameObject.AddComponent<BuffObject>();
		bObj.SetDebuff(poisonDebuff, true);
	}
}
```

I created a StatusEffectManager, a singleton which handles the creation of 

```
    public Debuff Poisoned(float poisonDuration, float poisonTickInterval, int poisonDamageTotal, bool isPlayer = true) {
        int poisonDamagePerTick = (int)(poisonDamageTotal / (poisonDuration / poisonTickInterval));
        string description = $"A lingering toxin takes its toll on the target, dealing {poisonDamagePerTick} damage every {poisonTickInterval} in {poisonDuration} seconds.";
        if(isPlayer) {
            description = $"A lingering toxin takes its toll on you, dealing {poisonDamagePerTick} damage every {poisonTickInterval} in {poisonDuration} seconds.";
        }
        Debuff poisoned = ScriptableObject.CreateInstance<Debuff>();
        poisoned.MakeDebuff(
            true,
            0,
            poisonDuration,
            DebuffableStat.HEALTH,
            0,
            "Poisoned",
            description,
            poisonedSprite,
            false,
            0,
            0,
            true,
            poisonTickInterval,
            poisonDamageTotal,
            poisonDuration
        );
		return poisoned;
	}
}
```

The manager allows me to handle the creation of new Debuff. To do this, I just had to extend the Debuff class to allow me to create one programmatically by passing the variables through. With this, we now have a working way to create poisons, paralysis and more by way of a simple 
## Pros and Cons To This Approach

**Pros:**
- A Manager singleton can handle the creation of these new debuffs
- ScriptableObject.CreateInstance is a tidy way to not need to have copies of SOs made whenever needed.
- The singleton is extendable to support as many status effects as I need

**Cons:**
- The singleton will get pretty heavy with my current implementation
	- The above example, just for poison, is 29 lines long, although a lot of that is just coding style.
	- I could also introduce the named parameters, to make things easy to maintain later.

I couldn't think of many more cons, as the system seems to work pretty well. 

## The Future of Status Effects

I intend to keep extending these from just paralysis and poison to more status effects, for instance:
- Sleep 
	- This will last longer than paralysis by default but will cancel when the target's hit.
- Disease
	- This will cause a negative value to attributes.
- Slow
	- Reduce the movement speed of a target.
- Heavy
	- Reduce the movement speed and skill speed of a target.
- Snare
	- Prevents the target from moving but can still use skills.

And so on.

The other thing I'm going to do is create a messages file, which will let me store the description in English in one place and then I can reference it from there. This will mean that once the game's complete, if I were to try to support multiple languages, the messages wouldn't be hard coded into the code.

All in all, I'm happy with the approach I've taken and I think it'll add a lot of flavour to skills in the future. I've got a lot more work to make sure skills feel more fluid and fun, but that's part of what I've been working on in the game as part of this update. It's getting there - I hope this to be the best version of the game yet with plenty to see and do.

Until next time folks, much love and happy tinkering - 
Timlah

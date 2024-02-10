---
tags:
  - Personal-Blog
---
My RPG has been in development for a bit over a year now. I could have taken an easy route with the game: Buy an asset pack to cover all the fundamentals for an RPG, come up with a story and just piece it together. Get more asset packs to cover the visuals of the game and away we go. Instead, I decided I wanted this to be a project of learning, fun and skeletons. I'm currently working on the biggest single update for the game so far, so this devlog is a look back at what I've added so far and what is still to be done for this update.

# Updated Features

## Inventory

Let's start with the easy bits first. The inventory has been updated to go from just 20 slots, to... 20 slots... Of 99! Every slot can hold up to 99 of any stackable item. I'll also eventually look into ways to increase the bag slots, but for now, 20 slots of 99 means you have a carry maximum potential of 1980 - That's a pretty big increase from just 20 items! This also works in bank screens.

![The inventory shows multiple stacked items in the inventory](https://i.ibb.co/mHF0cHz/Inventory-Update.png)

## Combat Tweaks

As I wrote [last week](https://www.timlah.com/blog/slug/jan-2024-devlog-001-status-effects), I have added in Status Effects to the game, which brings about extra effects to play around with. From paralysis to poison, there's a lot of room for status effects to become more varied as time goes on. But this isn't the only tweak that's been made. Enemies now won't see you if you're obscured. If they know you're there because they watched you go behind something, they'll attempt to move around the obstacle to you, but they will give up if they can't find an easy way. This'll be important for enclosed spaces, such as dungeons.

As well as this, I fixed a couple of longstanding bugs, especially around the animation locking of some skills. This makes combat feel a lot smoother. I also fixed an issue with the global cooldowns of skills, so that you don't unlock a GCD by pressing a different move. That was a bizarre issue, simply resolved by adding a coroutine against each move that is used.

I also added in a Line Area of Effect type. This works similarly to other AoE skills, except this one travels from a source to a destination. For instance, if you are facing an enemy that is 5 meters away and you use a Line attack, then the damage takes time to traverse from the source to the destination. This will be used for dashes and skills that lock the player in place, encouraging players to think about when they're going to use these skills. I also intend to do a Ground AoE skill type and to tidy up the targeted AoE skill type a bit.

## Minigames

I added minigames to Skell's Quest because I wanted to come up with a new way to mitigate bad luck. I don't believe in giving players an easy ride; if they are going to be doing the end-game content, then they need to put in some effort. If they are completionists, they should expect to need to do some grinding. Sorry, that's just how things are. But I don't want completionists, or even more casual players to be locked behind bad luck. That's no fun for anyone.

![An example minigame](https://i.ibb.co/rffRfF4/Sliding-Puzzle-Minigame.gif)

So I added minigames to get around this. Players can do a dungeon run and get their loot. Once they've obtained their loot, they can choose whether or not to sacrifice the loot. If they choose to sacrifice it, they play through a minigame and if successful, they can choose another piece of loot from the same loot table as the item that dropped. This way, players are not going to need to do a dungeon 1000 times in order to complete a 10 item encounters log... Speaking of which...

## Encounters Log

Ever wondered how many of an enemy you've killed? Want to know if you've obtained all loot they can drop? Wonder no more, we have an Encounters Log which lets you see what items you've unlocked and how many more items that enemy can drop. This is vital for those completionists out there, as all dungeon bosses will have their own loot to drop and thus achievements, pets and more!

## A Dungeon

The next update is all about adding in a dungeon to the game; somewhere that you can run through, get some decent combat experience and big rewards in the process. It's an ambitious update which is looking to add a lot more content in a small, concentrated area, but it also needs to have extra functionality to make it act like a dungeon should.

There is a randomised location for a dungeon chest. This is configurable by me, where I just add some GameObjects to a scene that represents where a chest can spawn, then have a parent GameObject which holds a bit of code for determining where and how many should spawn. These chests contain loot specific to the dungeon they're in and the loot is random based on loot tables.

![A chest appears in random parts of the dungeon - Size to be addressed](https://i.ibb.co/GtGztJ2/Random-Chests.png)

We have Elite monsters (which are currently just a variant of the normal Gobob). These hit harder, have more health and will be more of a challenge than a normal monster will be. Be careful not to fight too many monsters at once! There are also interactable doors, levers and more.

## Cutscenes

Yep, we have cutscenes in the game now. Skell walks through doors, the boss of Gobob Bunka, Blobob, the Devourer, has an introduction animation. Skell walks through tunnels and climbs up and down stairs, all with the press of a button.

![Skell Enters the Gobob Bunka](https://i.ibb.co/3m1Gp1h/Skell-Enters-Bunka-Dungeon-Cutscene.gif)

## And more things..!

Font's been updated to be a lot smoother, XP has been smoothed and a few other things have been updated. A couple of bugs have been squashed - The list goes on and on... And we're not even done with this update yet.

# To Be Updated Before Release

## More Combat Tweaks

There are a lot more things to fix up in combat; enemies are getting stuck in place when they come to attack you in groups, so I need to be able to make them not get stuck. I need them to understand they're all there and need to move around one another (and other obstacles), in order to get to their target.

I also want to make sure the whole dungeon is a smooth, fun flow. So I need to make sure the enemies don't try to approach when they shouldn't be - And I need to make sure you can be up or downstairs in the dungeon without there being a risk of enemies targeting you from afar.

## Attributes To Mean Something

At the moment, attributes scale kind of strangely. I need to double check the attributes and ensure that you get some attributes based on levels against each stat. I'm unsure how I'm going to do that, thinking of a custom table which means that you might not get all strength from melee (as an example) - Perhaps we go like: Level 2 +2 strength, Level 3 +2 vitality, Level 4 +2 dexterity (and so on). 
## The Boss Fight

You'd think I'd have done this first, but given that a lot of this will be handled by the normal enemy script, there's only a few things I need to sort with the boss fight - Specifically how to inject special mechanics and the likes.

...

That's it!

So there's still a lot of work to go, but now that I've written down all I've done so far, I'm feeling really accomplished. The tweaks are difficult at the moment, it may require a rewrite of the combat script again, but I'm hoping I don't need to go that far. I just need to figure out a couple of bugs and to make sure that enemies can figure out how to get to the player if something is immediately in their way.

Blobob's going to be a simple encounter... But I'm hoping it's fun enough to play and I'll be looking for lots of feedback. We're getting close to the end of this update, despite how big it is, but I'm excited to see what people think about the ideas... And once this is in place, I'll be working on a lot of models for a long time.

Until next time folks, much love and happy tinkering - 
Timlah
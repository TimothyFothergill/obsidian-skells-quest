
*Start time:* 09:41

**Story:** 
As a player, I would like to have extra context that something has entered my inventory,
So that I don't get surprised when I look in my inventory.

As the developer, I would like to have a notification that displays the item's icon sprite and a message,
So that players are given all the context they need to make informed decisions whilst playing the game

**Acceptance Criteria (as appropriate):**
- Determine whether sprites outside of a single large sprite sheet can be added
- Determine how much effort adding the sprite will be.

**Comments:** 
This uses rich text and I've had it working with the current Default Spritesheet in TextMesh Pro settings.

```c#
"<sprite=\"" + itemAssetName + "\" name=\"" + itemAssetName + "\">" + " " + itemName + " added to inventory.";
```

After playing around, I managed to get this working.

![[Pasted image 20230618103831.png]]

```c#
<sprite=\"" + itemAssetName + "\" index=0>" + " " + itemName + " added to inventory."
```

I'll need to prepare a spritesheet for all icons, in which the names are correctly entered. This can then become the default spritesheet and then if they're given the same name as what's in itemAssetName, then I can use name="". The alternative is all of the sprite asset's are added there separately, where index=0 can exist.

Both of these would be a relatively big task, but it'll make the game look better.

To create the SpriteAsset's required, each item will, individually, need to be entered like this: ![[Pasted image 20230618104301.png]]

The alternative is to make one spritesheet and have a way to select the correct one (be it name or index).

*Finish time:* 10:39

Additional work:

I was considering the best way to handle this. For now, I've made all of the existing icons into Sprite Assets in the TextMesh Pro.
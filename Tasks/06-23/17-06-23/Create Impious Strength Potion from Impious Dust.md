*Start time:* 14:12

**Story:** 
As a player, I would like to be able to craft something using the Wildcraft resource Impious Dust,
So that I have an actual reason to do Wildcrafting

**Acceptance Criteria (as appropriate):**
- Create an Impious Strength Potion
- Implement the Impious Strength Potion

**Comments:** 
Started by creating the item and putting it in the Datasheets.
```csv
05-BOT-BeginnersPotionOfStrengthImpious,Beginners Potion of Strength (Impious),TRUE,50,100,75,A potion that fortifies your strength infused with Impious Dust,DRINK,Assets/Imports/Cainos/Pixel Art Icon Pack - RPG/Texture/Potion/Blue Potion.png,TRUE,{01-CRAFT-ImpiousDust;01-BOT-VialOfWater},1,55,6,UNCOMMON,BOTANY
```

Here's the Ability for the item generated by my Custom Tool:
![[Pasted image 20230617143237.png]]

Then I added it to a prefab so it could be made and potentially down as a drop. Finally, I added the new Ability to the AbilityManager.

*Finish time:* 14:38

*Start time:* 21:18

**Story:** 
As the developer, I would like to improve the UX of the Crafting Screen,
So that navigating the screen is simpler.

As a player, I would like to be able to have more options within the Crafting Screen,
So I can play the game in a way that doesn't hinder me whilst doing crafting.

**Acceptance Criteria (as appropriate):**
- UX improvements to current crafting screen.
- Craft, Craft-x and Craft All buttons.
- Embedded channelling bar.

**Comments:** 
Continuation from yesterday

Today I made the increase and decrease quantity buttons work. I had some difficulty with this, as the text field wasn't easily accessible. Instead I used the TMP_InputField class and looked for the .text property against that.

![[Pasted image 20230620213617.png]]

Then I made a working crafting timer in the Crafting Screen UI. This took a bit of unthreading the previous channelling panel, re-understanding and re-implementing how this worked in a more streamlined way for crafting.

Next I fixed up some issues with the RecipeSlots, which yesterday was left in a state where they weren't working. They weren't instantiating. Refactored this down and now they do:

Found a bug which must have existed since crafting started - The RecipeSlots get added and destroyed the following frame, then readded on that same frame. Will create a bug and investigate that tomorrow.


*Finish time:* 23:45
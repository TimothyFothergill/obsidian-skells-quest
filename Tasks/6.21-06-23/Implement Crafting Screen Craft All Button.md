
*Start time:* 13:03

**Story:** 
As the developer, I would like to implement a craft all button
So that players have more quality of life features

**Acceptance Criteria (as appropriate):**
- Add in new functionality for craft all.

**Comments:** 
Yesterday, multi-craft was implemented (with some bugs to address).

Craft All requires a look in the inventory and bank. Bank items are stored in a BankSlot object. This contains the item and the quantity stored. 

Paused at 13:20
Resumed at 22:15

Continued working on the Craft All button - Eventually found an elegant solution to take an existing method which returns a Boolean if all recipe items are in the inventory - I just had to make an adapted version of this method which returns a Boolean if all recipe items are in inventory and bank. Seemed to work first time with no observed issues.

*Finish time:* 23:11
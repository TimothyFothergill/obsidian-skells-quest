---
tags:
  - Crafting
  - Fix
---
*Start time:* 21:22

**Story:** 
As the developer, I need to investigate and resolve why crafting stations are not displaying anything,
So that players can craft again!

**Acceptance Criteria (as appropriate):**
- Investigate why crafting stations aren't working.
- Document the process in this ticket, may eventually form the basis of a Runbook.

**Comments:** 
When working through this, I noticed that some of the items were missing. I decided to download the Item List and used the CSV Generator to regenerate items - This seemed to work for fixing the recipes attached to items.

However the other problem was with the Abilities list. This wasn't populating the the crafting stations correctly.

A runbook has been made for this with the following content:

- [ ] Check if the game correctly populates the crafting stations
- [ ] Go to the datasheet and download the Items list, rename the file to "Items"
- [ ] Custom Tooling > CSV Generators > Items 
- [ ] Check if this resolves it, if nothing is appearing in the stations still, follow the child checkboxes.
	- [ ] Go to the datasheet and download the Abilities list, rename the file to "Abilities"
	- [ ] Custom Tooling > CSV Generators > Abilities
- [ ] Remember to delete all CSV files downloaded this way

*Finish time:* 22:03
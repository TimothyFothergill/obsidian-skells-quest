
*Start time:* 10:25

**Story:** 
As the developer, I want to move the SkillsManager out of the EventSystem GameObject,
So that I have it separated from other logic and can keep it in its own Manager object

**Acceptance Criteria (as appropriate):**
- Move SkillsManager into its own Manager GameObject.

**Comments:** 
Whilst testing this, I moved the Component into a new GameObject and disabled it. This, however, caused many issues with regards to the Skills index. Removing the old Component from EventSystem resolved this.

*Finish time:* 10:30
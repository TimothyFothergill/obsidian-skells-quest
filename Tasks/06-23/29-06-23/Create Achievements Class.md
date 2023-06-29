
*Start time:* 22:46

**Story:** 
As the developer, I would like to reward players for their progress throughout the game,
So that it may incentivise players to do tasks they may otherwise not be familiar with.

**Acceptance Criteria (as appropriate):**
- Introduce a base class for achievements that can be extended.
- Ensure the Achievements Screen can read these Achievements.

**Comments:** 
Started to piece together how this class will look. I also realised I needed a few extra classes to handle the tracking of the achievements.

I've created a ScriptableObject for Achievements, as well as Criteria objects which will check and track depending on the type of achievement. The Criteria class is a base class which is extended in the AchievementCriteria.cs file.

Things I need to do still:
- Make a few more AchievementCriterias
- Make an AchievementManager
- Tie the AchievementManager to the UI in a meaningful way
- Ensure Achievements give rewards

*Finish time:* 23:36
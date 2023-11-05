
*Start time:* 21:20
Tags: #SaveManager 

**Story:** 
As the developer, I want to have a central repository of all items in the game,
So that I can refer to them with just the ScriptableObject's `.name` property.

**Acceptance Criteria (as appropriate):**
- Create a new Dictionary which serves as a <key, value> pair for retrieving asset data.
- Ensure items can be saved and loaded from the cloud.
- Make this simple enough to be implemented for other types.

**Comments:** 
This was more straightforward than I anticipated. By using a Resources folder, I'm able to use Resources.Load() initially. This causes _some_ issues, such as having to keep it up to date in two places for now... In the long term, this can be resolved by making it so all new itembases go into the resources version of the `Data/` directory.

*Finish time:* 22:10
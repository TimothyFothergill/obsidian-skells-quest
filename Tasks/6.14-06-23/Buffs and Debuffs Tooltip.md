*Start time:* 17:45

**Story:** 
As a player, I would like a tooltip to appear whenever I hover over a buff or debuff,
So that I know what that buff/debuff is doing.

As a player, I would like a timer to appear whenever a buff or debuff is active,
So that I know how long that buff/debuff has left.

**Acceptance Criteria (as appropriate):**
- New tooltip Prefab for buffs and debuffs.
- Tooltip Prefab initiates whenever hovering over a buff or debuff.
- New timer appears whenever a buff or debuff is active.

**Comments:** 
Unlike other panels tooltips, such as the inventory system, this one may work better included with the buff/debuff image prefab itself.

Making the asset was pretty easy, but the difficult lay in dynamically setting the size. Further to that, a timer needed to be set up. Two new scripts were therefore added to the BuffImage prefab, which address the following;

Timer:
```c#
    IEnumerator Timer(float timer) {

        for(int i = 0; i < timer; i++) {

            transform.GetChild(1).GetComponent<TextMeshProUGUI>().text = timer.ToString();

            timer -= 1;

            yield return new WaitForSeconds(1);

        }

    }
```
The above is a simple for loop that sets off once - The object is destroyed when it gets to 0 by other means.

Dynamic sizing:
https://chat.openai.com/share/af17ef39-9691-4ebf-b9f3-d05a2fa7406c 
This covered the majority of what I was looking for.

Breaks:
18:30-21:45

*Finish time:* 22:15

Notes: This task was determined on 11-06-23, but needed to give myself a small pause before resuming work on it.
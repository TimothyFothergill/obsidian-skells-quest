
*Reported time:* 08:42
*Start time:* 08:42
**Tags:** #Bug 

**What I fixed:**
I had two iterators; one going up, one going down. This meant that as soon as the buff/debuff countdown got half-way, it stopped.

**Comments:**
A very simple change; I removed the `timer -= 1; ` line from the code and just calculate it by doing `(timer - i).ToString;`


*Finish time:* 08:45
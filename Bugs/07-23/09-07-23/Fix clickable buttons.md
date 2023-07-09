
*Reported time:* 22:55
*Start time:* 22:55

**What I fixed:**
The clickable buttons stopped working; something was either interrupting them, or they lost reference to what they were supposed to do on click.

**Comments:**
What?

![[Pasted image 20230709225608.png]]

When the heck did these buttons drop reference? Checking all UI buttons to make sure other things work.

A few others dropped; all were associated with the UIManager script, so changes to that script sometimes can break references. Oops!

*Finish time:* 23:00
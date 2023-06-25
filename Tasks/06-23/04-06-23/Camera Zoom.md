*Start time:* 14:15

**Story:** 
As a player, I would like to be able to zoom in and out,
So that I can see things the way I want.

**Acceptance Criteria (as appropriate):**
- A camera that zooms in and out as appropriate.

**Comments:** 
The first thing I tried was to see if I can edit the Field of View - This was straight forward, there's a property on all virtual cameras called m_Lens which contains FoV values.

Next I realised that the real goal would be to set:
- A limit for how far to zoom in/out
- The camera to move on a pivot; not changing the FoV

Virtual camera zoom has been resolved, its smooth and it's efficient.
![[Zoomin.gif]]



*Finish time:* 15:31
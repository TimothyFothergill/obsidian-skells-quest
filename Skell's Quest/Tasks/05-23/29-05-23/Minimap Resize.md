*Start time:* 10:05

**Story:** 
I want to make the minimap size smaller
So that it doesn't take up so much room on the screen.

**Acceptance Criteria (as appropriate):**
- Smaller minimap.

**Comments:** 
This was an easy task to start the morning off. The minimap is massive, however when I just drag the minimap parent to be smaller, the image goes all over the place.

The fix to this was to check the child object, which contains the actual image. The reason this happens is the parent is masking the child image.

*Finish time:* 10:09
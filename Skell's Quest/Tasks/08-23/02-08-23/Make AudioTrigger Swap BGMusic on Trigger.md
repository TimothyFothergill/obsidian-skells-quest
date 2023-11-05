
*Start time:* 08:18
**Tags:** #Audio #Dungeon #Triggers

**Story:** 
As the developer, I want to write a trigger that swaps the Background Music,
So that I can swap the music with the help of triggers.

**Acceptance Criteria (as appropriate):**
- Make an AudioTrigger that swaps music as appropriate.

**Comments:** 
This was a simple script that just listened for an isTrigger collider. Found the `AudioDatabase.FindAudioClip()` method was never returning the right thing, so uncovered that the wrong string was being passed.

*Finish time:* 08:24
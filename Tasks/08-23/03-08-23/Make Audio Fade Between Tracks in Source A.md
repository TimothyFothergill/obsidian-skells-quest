
*Start time:* 12:24
**Tags:** #Audio #Triggers 

**Story:** 
As the developer, I want to make the audio tracks fade between one another in AudioSource A,
So that players who enter the boss rooms aren't met with a sudden juxtaposition of sounds.

**Acceptance Criteria (as appropriate):**
- Ensure the music fades between one another correctly.

**Comments:** 
https://johnleonardfrench.com/how-to-fade-audio-in-unity-i-tested-every-method-this-ones-the-best/

This article gives an interesting idea, which is to use an Audio Mixer Group component, which is a new one to me.

Stopped: 12:40
Started: 22:38

I started this back up and got it across the finish line. Had plenty of IDE troubles yesterday, but got it fixed. In any event, this was a new one to me. The configuration of an Audio Mixer Group was strange:

> Open the Audio Mixer window (Window > Audio > Audio Mixer)
> Create an Audio Mixer Group
> Select that Mixer Group and in the Inspector window, expose the volume parameter (right click on volume to get the option for this)
> Back in the Audio Mixer window, at the top right is an Exposed Parameters dropdown, select the volume from the group and give it a name
> This can now be referenced in code with a `SetFloat()` or `SetInt()` (etc).

*Finish time:* 23:12
---
tags:
  - Audio
  - SceneSwapping
---
*Start time:* 21:53

**Story:** 
As the developer, I want to ensure that music tracks swap whenever the scene changes,
So that audio transitions flawlessly between scenes

**Acceptance Criteria (as appropriate):**
- Implement a way to swap the audio based on the newly loaded scene.

**Comments:** 
This was a useful task that saw me implement a delegate

```
    void OnEnable() => SceneManager.sceneLoaded += OnSceneLoaded;

    void OnSceneLoaded(Scene scene, LoadSceneMode mode) {
        bgMusic = AudioDatabase._instance.FindAudioClip(scene.name);
    }
```

The `+= OnSceneLoaded` is a special delegate function which allows me to get information about the scene.

*Finish time:* 22:48
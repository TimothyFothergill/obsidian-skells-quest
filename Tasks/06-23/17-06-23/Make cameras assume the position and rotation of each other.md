*Start time:* 13:30

**Story:** 
As the developer, I want the Virtual Camera and Freelook Camera to take over from the position of the previous one,
So that players can turn the cameras how they want to when they play.

**Acceptance Criteria (as appropriate):**
- Cameras accept each other's position and rotation on priority switch.
- Freelook camera zooms correctly.
- A keybind to return camera to default position.

**Comments:** 
The trick was to actually not use a Freelook Camera. The point of the Freelook was to be able to look around Skell. Instead, I wrote a small script that handles rotation of the lookAt target:

```c#
using UnityEngine;

public class RotateTarget : MonoBehaviour
{
	public float speed = 2.0f;
    float mouseRotationX;

    void Update()
    {
        if(Input.GetMouseButton(1)) {
            mouseRotationX = speed * Input.GetAxis("Mouse X");
            transform.Rotate(0, mouseRotationX, 0);
        }
    }
}
```

*Finish time:* 14:08
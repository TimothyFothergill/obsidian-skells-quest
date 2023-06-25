Task start time: 10:00

**Story:**
I want to prevent the minimap from spinning, so that the icons don't spin around.

**Acceptance Criterias:**
- Camera moves with the player but doesn't spin.

**Comments:**
Can move camera with pos x and z to simulate following player. x & z to equal the players x & z.

```
transform.position = new Vector3(playerTransform.position.x, transform.position.y, playerTransform.position.z);
```

Camera was detached from player and script added with the above in LateUpdate, meaning it is drawn last, making for a smooth minimap camera system.

The camera was then made smaller as well.

Task finish time 10:09
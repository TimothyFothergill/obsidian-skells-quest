*Reported time:* 01:08
*Start time:* 01:08

**Idea:**
A minigame where you slide tiles around with one tile missing.

**Comments:**

This comment will constitute a plan for tackling this:

- Background image of the usual panel (for now, this is something that will need work eventually)
- Panels which accept an image
	- Start with a 9x9 grid, do the numbers 1 - 9 to begin with

![[Pasted image 20231029150153.png]]

Code logic:

TileSlider.cs
```c#
public class TileSlide : ManagerSingleton<TileSlide>
{
    [SerializeField] List<Image> images;

    public void SetupGame() {
		// This TileSlide script is a Manager script, which can be called from anywhere.
		// SetupGame() should choose an image in the list and populate panels 2 to 9.
    }

	void Populate

}
```

valid moves[]
for(1, 2, 3, 4, 5, 6, 7, 8) {
	validMove += GetSibling(siblingindex +1)
}
for(2, 3, 4, 5, 6, 7, 8, 9) {
	validMove += GetSibling(siblingindex -1)
}
for(1, 2, 3, 4, 5, 6) {
	validMove += GetSibling(siblingindex +3)
}
for(4, 5, 6, 7, 8, 9) {
	validMove += GetSibling(siblingindex +3)
}

foreach(Data move in validMove) {
	if(move.isBlank) {
		// swap sibling index and position
	}
}

Notes: This took a few days to fully implement
It can take any image, it can be failed and beaten, it returns a bool value on either success or fail.
*Finish time:* 22:15
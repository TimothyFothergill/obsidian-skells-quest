- [ ] Create a new `Skill`
- [ ] Assign an `Animation Clip` to the `anim` variable.
- [ ] Add an empty state in the Player Animator
	- [ ] Ensure the name of the state matches the Animation Clip
- [ ] Setup a link to the `idle` state. Remove all exit time between animations.

### Why do we remove all Exit Time?
![[Pasted image 20231112152350.png]]

Exit Time is great for a smooth transition from one animation to another, however we want players to be able to move between animations quickly and effectively. This gives a sharp, crisp change in animation.
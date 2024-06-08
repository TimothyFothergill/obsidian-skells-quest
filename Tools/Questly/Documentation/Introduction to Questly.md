Questly is an easy to use Quest System that you can hook into your Unity project right away. Once you've installed it, Questly will do the heavy lifting of setting up a full featured quest system for you, so you can focus on what matters - Your game.

Questly requires the following GameObjects to work:

=== MANAGERS ===
- QuestlyManagers
	- Components:
		- QuestlyManager
		- QuestlyAudioManager

Once you have the manager in place, you can add any of these components onto your GameObjects to start using the quest system in your game:
- QuestlyQuestGiver
- QuestlyObjective
## QuestlyManager
Configure this component to:
- Set a Quest limit (default: 10)
- Toggle if Quests can be abandoned (default: true)
- Toggle if Quests are auto-accepted with no dialogue (default: false)
- Toggle if Questly can give rewards on completion (default: true)
## QuestlyAudioManager
Configure this component to:
- Toggle if Audio plays when accepting a Quest (default: true)
	- Set the Audio for accepting a Quest (default: QuestAccepted.wav)
- Toggle if Audio plays when handing in a Quest (default: true)
	- Set the Audio for handing in a Quest (default: QuestComplete.wav)
- Toggle if Audio plays when a Quest objective is fulfilled (default: false)
	- Set the Audio for when a Quest objective is fulfilled (default: QuestUpdated.wav)
- Toggle if Audio plays when a Quests is abandoned (default: true)
	- Set the Audio for when a Quest objective is fulfilled (default: QuestAbandoned.wav)
## QuestlyQuestGiver
Add this to any GameObject and configure this component to:
- Set which Quest to give to the player (required)
- Toggle rewards (default: true)
- Toggle dialogue (default: true)
	- Script File (default: messages.en)
## QuestlyObjective
Add this to any GameObject and configure this component to:
- Set which quest this GameObject is an objective of (required)
- Set if this can be interacted with prior to accepting a quest (default: false)
- Set what type of Objective this is (default: interact, Choices: escort, interact, kill, pick-up, move-to)
# Questly Tools
As part of installing QuestSystem, you will get access to the QuestSystem tools for creating Quests.
## Questly > Quests Management
A pop-up GUI which allows you to create new Quest Scriptable Objects, as well as managing existing Quests. A diagram of the Questly Quests Management GUI:

![[Pasted image 20240323232204.png]]

*Start time:* 12:56

**Story:** 
As the developer, I would like to implement a basic form of Unity Cloud Save,
So that players who play the latest version can save whatever they make, their gained levels and quest completion

**Acceptance Criteria (as appropriate):**
- Understand whether we can utilise Unity Save easily.
- See if it feeds into the easy-save asset.

**Comments:** 
I set up Skell's Quest as a project in unity gaming services. Then I followed the instructions - However I noted there's an environment of Production. This made me wonder whether I'd need a development environment.

Paused at 13:00
Resumed at 21:39

I tested this by getting a bunch of items and saving them - I wrote a simple script that saves using EasySave3's constructor. I enabled easy save for prefabs on the managers as this was the main thing that needed saving. The Managers object contains state such as inventory, equipment, stats, skills, abilities and quests.

I then made a script to save and load the game's BankManager state - this worked pretty flawlessly with ES3:

```c#
    public void SaveGame() {
        ES3.Save("myBank", PlayerBankManager._instance.StoredInBank());
    }

	public void LoadGame() {
        List<BankSlot> defaultValue = new List<BankSlot>();        
        List<BankSlot> myBank;
        myBank = ES3.Load<List<BankSlot>>("myBank", defaultValue);
        PlayerBankManager._instance.LoadBank(myBank);
        UIManager._instance.CloseAllPanels();
        PlayerManager._instance.ReturnToStartingPosition();
    }

	public void OnApplicationQuit() {
        ES3.Save("myBank", PlayerBankManager._instance.StoredInBank());
    }
```

Now I wanted to save the file to Unity Game Services Cloud Save. 

```c#
    async void Start() {
        try {
            var options = new InitializationOptions()
                .SetEnvironmentName("<environment-name-here>");
            await UnityServices.InitializeAsync();
        } catch (Exception exception) {
            Debug.LogError(exception);
        }
        try {
            await AuthenticationService.Instance.SignInAnonymouslyAsync();
        } catch (Exception e) {
            Debug.LogError(e);
        }
    }
```

This worked a charm and I was able to see my save in Cloud Save:
![[Pasted image 20230622224401.png]]

![[Pasted image 20230622224508.png]]

*Finish time:* 22:18

Notes: This is a very basic start to saving to the cloud, but it is a useful start. I would probably need to provide a method for players to log in to manage their own saves, however.
# Mod
*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

Base class of any mod. Should be present in all mods. You can have multiple Mod class derivatives in each DLL.

### Variables

Name | Description | Type
---- | ----------- | ----
[Enabled](API/MSCLoader/Mod/Variables/Enabled.md) | Get if the mod is enabled. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/Mod/Variables/ID.md) | Mod ID, unique identifier. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/Mod/Variables/Name.md) | Mod's display name. | <font color=#4170a7>string</font>
[Author](API/MSCLoader/Mod/Variables/Author.md) | Author of the mod. | <font color=#4170a7>string</font>
[Version](API/MSCLoader/Mod/Variables/Version.md) | Mod version, used in update check version comparison. | <font color=#4170a7>string</font>
[Description](API/MSCLoader/Mod/Variables/Description.md) | A short description of your mod. Displayed in the settings window for the mod. | <font color=#4170a7>string</font>
[Icon](API/MSCLoader/Mod/Variables/Icon.md) | Icon displayed in the mod list, preferably square and not larger than 256x256. | <font color=#4170a7>byte</font>[]
[UpdateLink](API/MSCLoader/Mod/Variables/UpdateLink.md) | A link from which ModLoader will check for updates. Must be GitHub or NexusMods. | <font color=#4170a7>string</font>
[modListElement](API/MSCLoader/Mod/Variables/modListElement.md) | The mod list element for the mod. | [ModListElement](API/MSCLoader/ModListElement.md)
[modSettings](API/MSCLoader/Mod/Variables/modSettings.md) | The settings container for the mod. Used when adding settings. | [ModSettings](API/MSCLoader/ModSettings/ModSettings.md)

### Public Functions

Name | Description | Order of Execution
---- | ----------- | ------------------
[ModSettings](API/MSCLoader/Mod/Functions/ModSettings.md) | Method that can be used to create or initialize settings for your mod. | 1
[ModSettingsLoaded](API/MSCLoader/Mod/Functions/ModSettingsLoaded.md) | Method called when all mods have had their [ModSettings()](API/MSCLoader/Mod/Functions/ModSettings.md) called. | 2
[MenuOnLoad](API/MSCLoader/Mod/Functions/MenuOnLoad.md) | Load Method for anything involving the menu scene. | 3
[MenuOnGUI](API/MSCLoader/Mod/Functions/MenuOnGUI.md) | OnGUI Method for the menu scene. | Every OnGUI call (Menu)
[MenuUpdate](API/MSCLoader/Mod/Functions/MenuUpdate.md) | Update Method for the menu scene. | Every frame (Menu)
[MenuFixedUpdate](API/MSCLoader/Mod/Functions/MenuFixedUpdate.md) | FixedUpdate Method for the menu scene. | Every fixed framerate frame (Menu)
[OnNewGame](API/MSCLoader/Mod/Functions/OnNewGame.md) | Method called when the player starts a new game, use cases include removing old save files. | 4
[PreLoad](API/MSCLoader/Mod/Functions/PreLoad.md) | Method called one frame after the game scene loads. | 5
[OnLoad](API/MSCLoader/Mod/Functions/OnLoad.md) | Method called just when the game has completely finished loading. | 6
[PostLoad](API/MSCLoader/Mod/Functions/PostLoad.md) | Method called after every mod has executed [OnLoad()](API/MSCLoader/Mod/Functions/OnLoad.md). | 7
[OnGUI](API/MSCLoader/Mod/Functions/OnGUI.md) | OnGUI method for the game scene. | Every OnGUI call
[Update](API/MSCLoader/Mod/Functions/Update.md) | Update method for the game scene. | Every frame
[FixedUpdate](API/MSCLoader/Mod/Functions/FixedUpdate.md) | FixedUpdate method for the game scene. | Every fixed framerate frame
[OnSave](API/MSCLoader/Mod/Functions/OnSave.md) | Method called when the player saves the game. | 8

### Example

```csharp
using MSCLoader;

namespace MyMod
{
    public class MyMod : Mod
    {
        public override string ID => "MyMod";
        public override string Name => "MY MOD";
        public override string Author => "YOU";
        public override string Version => "1.0";
        public override string Description =>  "THIS IS MY MOD!";
        public override string UpdateLink => "https://www.nexusmods.com/mysummercar/mods/9999";
        public override byte[] Icon => Properties.Resources.Icon;

        public override void ModSettings()
        {
            // Here you can add all the settings you want for your mod!
		}

        public override void OnNewGame()
        {
            // If the player starts a new game, are there things you need to reset for maximum immersion in the game?
        }

        public override void OnLoad()
        {
            // This is likely the method you want to load your stuff in the game.
        }

        public override void OnSave()
        {
            // If you have something to save, this would be the place to do it!
        }
    }
}
```

# ModLoader

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

This is the main mod loading class, it handles everything from initializing mods to making sure the various Mod methods are called at the correct times while also keeping track on how long each method takes to execute. Here you can get information on your own mod, which mods are installed, folder paths, some used colors for the UI etc.

Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html)

### Static Variables

Name | Description | Type
---- | ----------- | ----
[LoadedMods](API/MSCLoader/ModLoader/Variables/LoadedMods.md) | List of all currently found mods. All mods, regardless of enabled status, will be in this list. | <font color=#3ca486>List</font><[Mod](API/MSCLoader/Mod.md)>
[ModMethods](API/MSCLoader/ModLoader/Variables/ModMethods.md) | An array of lists containing what mod methods each mod uses. | <font color=#3ca486>List</font><[Mod](API/MSCLoader/Mod.md)>[]
[Date](API/MSCLoader/ModLoader/Variables/Date.md) | Get the current date and time. (Checks online first, with local machine time as a backup) | <font color=#3ca486>DateTime</font>
[UICanvas](API/MSCLoader/ModLoader/Variables/UICanvas.md) | The UI Canvas, under which all the ModLoader UI is placed, and where you could/should add your own UI as a child to. | [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html)
[MSCYellow](API/MSCLoader/ModLoader/Variables/MSCYellow.md) | The yellow color MSC (and mod loader) uses for it's UI elements. | [Color32](https://docs.unity3d.com/500/Documentation/ScriptReference/Color32.html)
[MSCRed](API/MSCLoader/ModLoader/Variables/MSCRed.md) | The wine red color that MSC (and mod loader) uses for it's UI elements. | [Color32](https://docs.unity3d.com/500/Documentation/ScriptReference/Color32.html)
[MSCRose](API/MSCLoader/ModLoader/Variables/MSCRose.md) | The rose color that MSC (and mod loader) uses for it's UI elements. | [Color32](https://docs.unity3d.com/500/Documentation/ScriptReference/Color32.html)
[ModDisabledRed](API/MSCLoader/ModLoader/Variables/ModDisabledRed.md) | The red color that the disabled mods has their name in. | [Color32](https://docs.unity3d.com/500/Documentation/ScriptReference/Color32.html)
[CurrentScene](API/MSCLoader/ModLoader/Variables/CurrentScene.md) | The current scene the game has loaded. | <font color=#aac397>CurrentScene</font>

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[GetModSettingsFolder](API/MSCLoader/ModLoader/Functions/GetModSettingsFolder.md) | Get a specific mod's setting folder. If it doesn't exist, calling this function will create the folder for the mod then return its path.  | <font color=#4170a7>string</font>
[GetModAssetsFolder](API/MSCLoader/ModLoader/Functions/GetModAssetsFolder.md) | Get a specific mod's asset folder. If it doesn't exist, calling this function will create the folder for the mod then return its path.  | <font color=#4170a7>string</font>
[GetMod](API/MSCLoader/ModLoader/Functions/GetMod.md) | Get a mod by its ID, returns null if not found.  | [Mod](API/MSCLoader/Mod.md)
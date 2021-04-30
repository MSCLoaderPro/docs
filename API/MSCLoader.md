# MSCLoader

*Mod Library*

Class | Description
----- | -----------
[Mod](API/MSCLoader/Mod.md) | Base class of any mod. Should be present in all mods.
[ModAssets](API/MSCLoader/ModAssets.md) | Class responsible for asset loading.
[ModConsole](API/MSCLoader/ModConsole.md) | Console handler, takes care of most of the user/modder side of the logging process.
[ModEarlyAccess](API/MSCLoader/ModEarlyAccess.md) | Simple date handler for mods, with this you can time limit your mods, and optionally prevent the mod from loading if 'todays' date is outside a specified range.
[ModLoader](API/MSCLoader/ModLoader.md) | the main mod loading class, it handles everything from initializing mods to making sure the various Mod methods are called at the correct times while also keeping track on how long each method takes to execute.
[ModPrompt](API/MSCLoader/ModPrompt.md) | A managing component of prompt.
[ModSave](API/MSCLoader/ModSave.md) | Class responsible for saving and loading save data for mods.
[ModSettings](API/MSCLoader/ModSettings.md) | Controller class for the mod's settings window.
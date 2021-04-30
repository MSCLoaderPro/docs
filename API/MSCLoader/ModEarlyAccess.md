# ModEarlyAccess

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

Simple date handler for mods, with this you can time limit your mods, and optionally prevent the mod from loading if 'todays' date is outside a specified range.  
It can take both local time and online time.

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[CheckDateAndDisable](API/MSCLoader/ModEarlyAccess/Functions/CheckDateAndDisable.md) | Check if the current date is within specified range, and if not disable the mod and show a message.  | <font color=#4170a7>void</font>
[CheckDate](API/MSCLoader/ModEarlyAccess/Functions/CheckDate.md) | Check the current date, optionally opt for online checking only. | <font color=#4170a7>bool</font>
[DisableMod](API/MSCLoader/ModEarlyAccess/Functions/DisableMod.md) | Completely disable a mod and show a message. | <font color=#4170a7>void</font>
[GetDate](API/MSCLoader/ModEarlyAccess/Functions/GetDate.md) | Get the current date (online with backup local time). | <font color=#3ca486>DateTime</font>
[GetOnlineDate](API/MSCLoader/ModEarlyAccess/Functions/GetOnlineDate.md) | Get the current date (online only, returns null if check failed). | <font color=#3ca486>DateTime</font>?

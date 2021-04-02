# ModConsole

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

Console handler, takes care of most of the user/modder side of the logging process. You can log pretty much anything you want, and it also gets logged into the output_log.txt located in the game folder.  
A user setting determines whether or not the console window should auto-open when logging an error or a warning (default setting is that it does auto-open with both).

Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html)

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[Log](API/MSCLoader/ModConsole/Functions/Log.md) | Logs a string, object or IList into the ModConsole and output_log.txt.  | <font color=#4170a7>void</font>
[LogError](API/MSCLoader/ModConsole/Functions/LogError.md) | Logs an error string to the ModConsole and output_log.txt, default red text and the console might auto-open depending on user settings. | <font color=#4170a7>void</font>
[LogWarning](API/MSCLoader/ModConsole/Functions/LogWarning.md) | Logs a warning string to the ModConsole and output_log.txt, default yellow text and the console might auto-open depending on user settings. | <font color=#4170a7>void</font>
[ToggleConsole](API/MSCLoader/ModConsole/Functions/ToggleConsole.md) | Open/Close the console window. | <font color=#4170a7>void</font>
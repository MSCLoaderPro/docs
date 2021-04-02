# [ModSettings](API/MSCLoader/ModSettings.md).AddKeybind

*public [SettingKeybind](API/MSCLoader/SettingKeybind.md) <b>AddKeybind</b>(string <b>id</b>, string <b>name</b>, [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) key, params [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[] modifiers);*  

#### Description

Creates a configurable keybind to the settings window for the mod. You assign a default main [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) and you can provide how many modifiers you want.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
name | Text displayed as the name of the setting. Upper-case recommended. | <font color=#4170a7>string</font> | N/A
key | The default main key for the setting. | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) | N/A
modifiers | The default modifier keys for the setting, keys that have to be pressed before the game recognizes the main key. | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) | Empty [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[]

#### Example

```csharp
SettingKeybind myKeybind;

public override void ModSettings()
{
    myKeybind = modSettings.AddKeybind("myKeybind", "MY KEYBIND", KeyCode.Z);
}
```
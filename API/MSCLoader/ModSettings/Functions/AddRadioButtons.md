# [ModSettings](API/MSCLoader/ModSettings.md).AddRadioButtons

*public [SettingRadioButtons](API/MSCLoader/SettingRadioButtons.md) <b>AddRadioButtons</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, params string[] <b>options</b>);*  
*public [SettingRadioButtons](API/MSCLoader/SettingRadioButtons.md) <b>AddRadioButtons</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, [UnityAction\<<font color=#4170a7>int</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) <b>action</b>, params string[] <b>options</b>);*  
*public [SettingRadioButtons](API/MSCLoader/SettingRadioButtons.md) <b>AddRadioButtons</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b>, params string[] <b>options</b>);*

#### Description

Creates radio buttons for the settings window. Can be configured with a parameter action or a regular non-parameter action. 
The parameter action calls your provided action with the current value of the setting as an argument.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
name | Text displayed as the name of the setting. Upper-case recommended. | <font color=#4170a7>string</font> | N/A
value | The default value for the setting. Shouldn't be larger than the length of the options array - 1. | <font color=#4170a7>int</font> | N/A
action | Action called whenever the value is changed. | [UnityAction\<<font color=#4170a7>int</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) / [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)  | N/A
options | Array of the possible options for the setting, their order corresponding to their value. | <font color=#4170a7>string</font>[] | N/A

#### Example

```csharp
SettingRadioButtons myRadioButtons;

public override void ModSettings()
{
    myRadioButtons = modSettings.AddRadioButtons("myRadioButtons", "MY RADIO BUTTONS", 2, (value) => { ModConsole.Log($"This is the new value: {value}"); }, "ZERO", "ONE", "TWO");
    // Whenever the value changes, for example if ONE is pressed, this will be logged in the console:
    // This is the new value: 1
}
```
# [ModSettings](API/MSCLoader/ModSettings.md).AddToggle

*public [SettingToggle](API/MSCLoader/SettingToggle.md) <b>AddToggle</b>(string <b>id</b>, string <b>name</b>, bool <b>value</b>);*  
*public [SettingToggle](API/MSCLoader/SettingToggle.md) <b>AddToggle</b>(string <b>id</b>, string <b>name</b>, bool <b>value</b>, [UnityAction\<<font color=#4170a7>bool</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) <b>action</b>);*  
*public [SettingToggle](API/MSCLoader/SettingToggle.md) <b>AddToggle</b>(string <b>id</b>, string <b>name</b>, bool <b>value</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b>);*

#### Description

Creates a toggle in the settings list. Can be configured with a parameter action or a regular non-parameter action. 
The parameter action calls your provided action with the current value of the setting as an argument.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
name | Text displayed as the name of the setting. Upper-case recommended. | <font color=#4170a7>string</font> | N/A
value | Default toggle value. | <font color=#4170a7>bool</font> | N/A
action | Action called whenever the value is changed. | [UnityAction\<<font color=#4170a7>bool</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) / [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)  | N/A

#### Example

```csharp
SettingTextBox myToggle;

public override void ModSettings()
{
    myToggle = modSettings.AddToggle("myToggle", "MY TOGGLE", false, NewValue);
}

public void NewValue(bool newValue) 
{
    ModConsole.Log($"New value is: {newValue}");
    // New value is: True
}
```
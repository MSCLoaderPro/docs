# [ModSettings](API/MSCLoader/ModSettings.md).AddTextBox

*public [SettingTextBox](API/MSCLoader/SettingTextBox.md) <b>AddTextBox</b>(string <b>id</b>, string <b>name</b>, string <b>value</b>, string <b>placeholder</b> = "ENTER TEXT...", [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation <b>inputType</b> = [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation.None);*  
*public [SettingTextBox](API/MSCLoader/SettingTextBox.md) <b>AddTextBox</b>(string <b>id</b>, string <b>name</b>, string <b>value</b>, [UnityAction\<<font color=#4170a7>string</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) <b>action</b>, string <b>placeholder</b> = "ENTER TEXT...", [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation <b>inputType</b> = [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation.None);*  
*public [SettingTextBox](API/MSCLoader/SettingTextBox.md) <b>AddTextBox</b>(string <b>id</b>, string <b>name</b>, string <b>value</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b>, string <b>placeholder</b> = "ENTER TEXT...", [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation <b>inputType</b> = [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation.None);*

#### Description

Creates a text box in the settings list. Can be configured with a parameter action or a regular non-parameter action. 
The parameter action calls your provided action with the current value of the setting as an argument. The event used for the parameter actions is the OnValueChanged.  
You can provide a character validation setting, which means you can, for example, only allow numbers in your text box or only letters.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
name | Text displayed as the name of the setting. Upper-case recommended. | <font color=#4170a7>string</font> | N/A
value | Default text value. | <font color=#4170a7>string</font> | N/A
placeholder | Placeholder text when value is "". | <font color=#4170a7>string</font> | "ENTER TEXT..."
action | Action called whenever the value is changed. | [UnityAction\<<font color=#4170a7>string</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) / [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)  | N/A
inputType | Type of input accepted by the text box [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html). | [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation | [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html).CharacterValidation.None

#### Example

```csharp
SettingTextBox myTextBox;

public override void ModSettings()
{
    myTextBox = modSettings.AddTextBox("myTextBox", "MY TEXT BOX", "NO", NewValue);
}

public void NewValue(string newValue) 
{
    ModConsole.Log($"New value is: {newValue}");
    // New value is: YES
}
```
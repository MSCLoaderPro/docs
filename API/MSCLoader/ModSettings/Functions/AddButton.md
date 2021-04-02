# [ModSettings](API/MSCLoader/ModSettings.md).AddButton

*public [SettingButton](API/MSCLoader/SettingButton.md) <b>AddButton</b>(string <b>id</b>, string <b>buttonText</b>, string <b>name</b> = "", [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b> = null, bool <b>blockSuspension</b> = false);*  
*public [SettingButton](API/MSCLoader/SettingButton.md) <b>AddButton</b>(string <b>id</b>, string <b>buttonText</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b> = null, bool <b>blockSuspension</b> = false);*

#### Description
Creates a button setting for the mod in the settings window. It can be set to execute a specific [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) when clicked. When "buttonText" is empty the button will take up the entire width of the setting window.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
buttonText | Text displayed on the button itself. | <font color=#4170a7>string</font> | N/A
name | Text displayed beside the button, hidden if empty. | <font color=#4170a7>string</font> | ""
action | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) invoked when the button is clicked. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null
blockSuspension | If true, the action can never be blocked from being invoked. For most use cases this can be left at default | <font color=#4170a7>bool</font> | false

#### Example

```csharp
SettingButton myButton;

public override void ModSettings()
{
    myButton = modSettings.AddButton("myButton", "PRESS ME!", "THIS IS MY BUTTON!", () => { ModConsole.Log("HEY! My button was pressed!"); });
    // When pressed will log a string to the console.
    // HEY! My Button was pressed!
}
```
# SettingToggle

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a toggle setting. With this you can modify your setting quite extensively.

### Variables

Name | Description | Type
---- | ----------- | ----
[nameText](API/MSCLoader/SettingToggle/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingToggle/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[toggle](API/MSCLoader/SettingToggle/Variables/toggle.md) | [Toggle](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Toggle.html) component for the actual toggle. | [Toggle](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Toggle.html)
[offImage](API/MSCLoader/SettingToggle/Variables/offImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the toggle in the OFF state. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[onImage](API/MSCLoader/SettingToggle/Variables/onImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the toggle in the ON state. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[Enabled](API/MSCLoader/SettingToggle/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingToggle/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingToggle/Variables/Name.md) | Get/Set the setting name, the text displayed beside the setting. Upper-case recommended. | <font color=#4170a7>string</font>
[Value](API/MSCLoader/SettingToggle/Variables/Value.md) | Get/Set the setting value. | <font color=#4170a7>bool</font>
[OnValueChanged](API/MSCLoader/SettingToggle/Variables/OnValueChanged.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>bool</font>> called whenever the [Value](API/MSCLoader/SettingToggle/Variables/Value.md) is changed. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>bool</font>>
[defaultValue](API/MSCLoader/SettingToggle/Variables/defaultValue.md) | The default value for the setting. The [Value](API/MSCLoader/SettingToggle/Variables/Value.md) will be set to this whenever the user resets settings to default. | <font color=#4170a7>bool</font>
[suspendActions](API/MSCLoader/SettingToggle/Variables/suspendActions.md) | When true actions added to [OnValueChanged](API/MSCLoader/SettingToggle/Variables/OnValueChanged.md) won't be called. | <font color=#4170a7>bool</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[AddAction](API/MSCLoader/SettingToggle/Functions/AddAction.md) | Add an [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html)<<font color=#4170a7>bool</font>> to the [OnValueChanged](API/MSCLoader/SettingToggle/Variables/OnValueChanged.md) [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>bool</font>>. | <font color=#4170a7>void</font>
[ResetToDefaults](API/MSCLoader/SettingToggle/Functions/ResetToDefaults.md) | Resets the [Value](API/MSCLoader/SettingToggle/Variables/Value.md) to [defaultValue](API/MSCLoader/SettingToggle/Variables/defaultValue.md) | <font color=#4170a7>void</font>

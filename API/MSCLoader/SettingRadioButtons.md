# SettingRadioButtons

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a radio button setting. With this you can modify your setting quite extensively.

### Variables

Name | Description | Type
---- | ----------- | ----
[buttons](API/MSCLoader/SettingRadioButtons/Variables/buttons.md) | List containing all the related [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md) components. | <font color=#3ca486>List</font><[RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md)>
[nameText](API/MSCLoader/SettingRadioButtons/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingRadioButtons/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[group](API/MSCLoader/SettingRadioButtons/Variables/group.md) | [ToggleGroup](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.ToggleGroup.html) for the setting, responsible for controlling the [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md) [Toggle](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Toggle.html) | [ToggleGroup](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.ToggleGroup.html) 
[Enabled](API/MSCLoader/SettingRadioButtons/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingRadioButtons/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingRadioButtons/Variables/Name.md) | Get/Set the setting name, the text displayed beside the setting. Upper-case recommended. | <font color=#4170a7>string</font>
[Value](API/MSCLoader/SettingRadioButtons/Variables/Value.md) | Get/Set the setting value. | <font color=#4170a7>int</font>
[OnValueChanged](API/MSCLoader/SettingRadioButtons/Variables/OnValueChanged.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>int</font>> called whenever the [Value](API/MSCLoader/SettingRadioButtons/Variables/Value.md) is changed. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>int</font>>
[defaultValue](API/MSCLoader/SettingRadioButtons/Variables/defaultValue.md) | The default value for the setting. The [Value](API/MSCLoader/SettingRadioButtons/Variables/Value.md) will be set to this whenever the user resets settings to default. | <font color=#4170a7>int</font>
[buttonPrefab](API/MSCLoader/SettingRadioButtons/Variables/buttonPrefab.md) | Prefab [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) for use in adding [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md) | [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html)
[toggleGroup](API/MSCLoader/SettingRadioButtons/Variables/toggleGroup.md) | Parent [RectTransform](https://docs.unity3d.com/500/Documentation/ScriptReference/RectTransform.html) containing all the settings [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md) [GameObjects](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) | [RectTransform](https://docs.unity3d.com/500/Documentation/ScriptReference/RectTransform.html)
[suspendActions](API/MSCLoader/SettingRadioButtons/Variables/suspendActions.md) | When true actions added to [OnValueChanged](API/MSCLoader/SettingRadioButtons/Variables/OnValueChanged.md) won't be called. | <font color=#4170a7>bool</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[SetButtonLabelText](API/MSCLoader/SettingRadioButtons/Functions/SetButtonLabelText.md) | Set the label text of the button of specified id. | <font color=#4170a7>void</font>
[GetButtonLabelText](API/MSCLoader/SettingRadioButtons/Functions/GetButtonLabelText.md) | Get the label text of the button of specified id. | <font color=#4170a7>string</font>
[AddButton](API/MSCLoader/SettingRadioButtons/Functions/AddButton.md) | Add a [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md) to the setting with specified name. | [RadioButton](API/MSCLoader/SettingRadioButtons/RadioButton.md)
[AddAction](API/MSCLoader/SettingRadioButtons/Functions/AddAction.md) | Add an [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html)<<font color=#4170a7>int</font>> to the [OnValueChanged](API/MSCLoader/SettingRadioButtons/Variables/OnValueChanged.md) [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>int</font>>. | <font color=#4170a7>void</font>
[ResetToDefaults](API/MSCLoader/SettingRadioButtons/Functions/ResetToDefaults.md) | Resets the [Value](API/MSCLoader/SettingRadioButtons/Variables/Value.md) to [defaultValue](API/MSCLoader/SettingRadioButtons/Variables/defaultValue.md) | <font color=#4170a7>void</font>

# SettingTextBox

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a text box setting. With this you can modify your setting quite extensively.

### Variables

Name | Description | Type
---- | ----------- | ----
[nameText](API/MSCLoader/SettingTextBox/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingTextBox/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[inputField](API/MSCLoader/SettingTextBox/Variables/inputField.md) | [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html) component for the text input. | [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html)
[inputImage](API/MSCLoader/SettingTextBox/Variables/inputImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html) background. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[inputPlaceholderText](API/MSCLoader/SettingTextBox/Variables/inputPlaceholderText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the placeholder text on the [InputField](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField.html). | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[Enabled](API/MSCLoader/SettingTextBox/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingTextBox/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingTextBox/Variables/Name.md) | Get/Set the setting name, the text displayed beside the setting. Upper-case recommended. | <font color=#4170a7>string</font>
[Value](API/MSCLoader/SettingTextBox/Variables/Value.md) | Get/Set the setting value. | <font color=#4170a7>string</font>
[Placeholder](API/MSCLoader/SettingTextBox/Variables/Placeholder.md) | Get/Set the placeholder text. | <font color=#4170a7>string</font>
[InputType](API/MSCLoader/SettingTextBox/Variables/InputType.md) | Get/Set what kind of characters should be allowed. | [CharacterValidation](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.InputField-characterValidation.html)
[OnValueChange](API/MSCLoader/SettingTextBox/Variables/OnValueChange.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>> called whenever the [Value](API/MSCLoader/SettingTextBox/Variables/Value.md) is changed. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>>
[OnEndEdit](API/MSCLoader/SettingTextBox/Variables/OnEndEdit.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>> called when the user stops editing the input. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>>
[defaultValue](API/MSCLoader/SettingTextBox/Variables/defaultValue.md) | The default value for the setting. The [Value](API/MSCLoader/SettingTextBox/Variables/Value.md) will be set to this whenever the user resets settings to default. | <font color=#4170a7>string</font>
[suspendActions](API/MSCLoader/SettingTextBox/Variables/suspendActions.md) | When true actions added to [OnValueChanged](API/MSCLoader/SettingTextBox/Variables/OnValueChange.md) or [OnEndEdit](API/MSCLoader/SettingTextBox/Variables/OnEndEdit.md) won't be called. | <font color=#4170a7>bool</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[AddOnEndEditAction](API/MSCLoader/SettingTextBox/Functions/AddOnEndEditAction.md) | Add an [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html)<<font color=#4170a7>string</font>> to the [OnEndEdit](API/MSCLoader/SettingTextBox/Variables/OnEndEdit.md) [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>>. | <font color=#4170a7>void</font>
[AddOnValueChangeAction](API/MSCLoader/SettingTextBox/Functions/AddOnValueChangeAction.md) | Add an [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html)<<font color=#4170a7>string</font>> to the [OnValueChange](API/MSCLoader/SettingTextBox/Variables/OnValueChange.md) [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>string</font>>. | <font color=#4170a7>void</font>
[ResetToDefaults](API/MSCLoader/SettingTextBox/Functions/ResetToDefaults.md) | Resets the [Value](API/MSCLoader/SettingTextBox/Variables/Value.md) to [defaultValue](API/MSCLoader/SettingTextBox/Variables/defaultValue.md) | <font color=#4170a7>void</font>

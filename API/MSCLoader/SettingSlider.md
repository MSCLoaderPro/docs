# SettingSlider

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a slider setting. With this you can modify your setting quite extensively.

### Variables

Name | Description | Type
---- | ----------- | ----
[nameText](API/MSCLoader/SettingSlider/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingSlider/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[valueText](API/MSCLoader/SettingSlider/Variables/valueText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the value text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[valueShadow](API/MSCLoader/SettingSlider/Variables/valueShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the value text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[slider](API/MSCLoader/SettingSlider/Variables/slider.md) | [Slider](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Slider.html) component for the actual sliding of the setting. | [Slider](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Slider.html)
[backgroundImage](API/MSCLoader/SettingSlider/Variables/backgroundImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the slider background. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[handleImage](API/MSCLoader/SettingSlider/Variables/handleImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the slider handle. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[Enabled](API/MSCLoader/SettingSlider/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingSlider/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingSlider/Variables/Name.md) | Get/Set the setting name, the text displayed beside the setting. Upper-case recommended. | <font color=#4170a7>string</font>
[Value](API/MSCLoader/SettingSlider/Variables/Value.md) | Get/Set the setting value. | <font color=#4170a7>float</font>
[ValueInt](API/MSCLoader/SettingSlider/Variables/ValueInt.md) | Get/Set the setting value as an integer. | <font color=#4170a7>int</font>
[MinValue](API/MSCLoader/SettingSlider/Variables/MinValue.md) | Get/Set the setting minimum value. | <font color=#4170a7>float</font>
[MaxValue](API/MSCLoader/SettingSlider/Variables/MaxValue.md) | Get/Set the setting maximum value. | <font color=#4170a7>float</font>
[WholeNumbers](API/MSCLoader/SettingSlider/Variables/WholeNumbers.md) | Get/Set if the setting should only use whole numbers (integers). | <font color=#4170a7>bool</font>
[RoundDigits](API/MSCLoader/SettingSlider/Variables/RoundDigits.md) | Get/Set amount of digits to round to. | <font color=#4170a7>int</font>
[OnValueChanged](API/MSCLoader/SettingSlider/Variables/OnValueChanged.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>float</font>> called whenever the [Value](API/MSCLoader/SettingSlider/Variables/Value.md) is changed. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>float</font>>
[ValuePrefix](API/MSCLoader/SettingSlider/Variables/ValuePrefix.md) | Get/Set the string printed before the current value on the [valueText](API/MSCLoader/SettingSlider/Variables/valueText.md). | <font color=#4170a7>string</font>
[ValueSuffix](API/MSCLoader/SettingSlider/Variables/ValueSuffix.md) | Get/Set the string printed after the current value on the [valueText](API/MSCLoader/SettingSlider/Variables/valueText.md). | <font color=#4170a7>string</font>
[TextValues](API/MSCLoader/SettingSlider/Variables/TextValues.md) | Get/Set the string printed instead of the current value. Needs to be the same size as the number of possible integers within the minimum and maximum values. | <font color=#4170a7>string</font>[]
[defaultValue](API/MSCLoader/SettingSlider/Variables/defaultValue.md) | The default value for the setting. The [Value](API/MSCLoader/SettingSlider/Variables/Value.md) will be set to this whenever the user resets settings to default. | <font color=#4170a7>float</font>
[suspendActions](API/MSCLoader/SettingSlider/Variables/suspendActions.md) | When true actions added to [OnValueChanged](API/MSCLoader/SettingSlider/Variables/OnValueChanged.md) won't be called. | <font color=#4170a7>bool</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[ChangeValueText](API/MSCLoader/SettingSlider/Functions/ChangeValueText.md) | Manually update the value text. | <font color=#4170a7>void</font>
[SetRoundValue](API/MSCLoader/SettingSlider/Functions/SetRoundValue.md) | Manually update the rounded value. | <font color=#4170a7>void</font>
[AddAction](API/MSCLoader/SettingSlider/Functions/AddAction.md) | Add an [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html)<<font color=#4170a7>float</font>> to the [OnValueChanged](API/MSCLoader/SettingSlider/Variables/OnValueChanged.md) [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent_1.html)<<font color=#4170a7>float</font>>. | <font color=#4170a7>void</font>
[ResetToDefaults](API/MSCLoader/SettingSlider/Functions/ResetToDefaults.md) | Resets the [Value](API/MSCLoader/SettingSlider/Variables/Value.md) to [defaultValue](API/MSCLoader/SettingSlider/Variables/defaultValue.md) | <font color=#4170a7>void</font>

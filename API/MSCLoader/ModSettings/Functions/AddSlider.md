# [ModSettings](API/MSCLoader/ModSettings.md).AddSlider

*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, float <b>value</b>, float <b>minValue</b>, float <b>maxValue</b>, int <b>roundDigits</b> = 2);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, float <b>value</b>, float <b>minValue</b>, float <b>maxValue</b>, int <b>roundDigits</b> = 2, [UnityAction\<<font color=#4170a7>float</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) <b>action</b> = null);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, float <b>value</b>, float <b>minValue</b>, float <b>maxValue</b>, int <b>roundDigits</b> = 2, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b> = null);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, float <b>value</b>, float <b>minValue</b>, float <b>maxValue</b>, UnityAction<float> <b>action</b> = null);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, float <b>value</b>, float <b>minValue</b>, float <b>maxValue</b>, UnityAction <b>action</b> = null);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, int <b>minValue</b>, int <b>maxValue</b>);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, int <b>minValue</b>, int <b>maxValue</b>, [UnityAction\<<font color=#4170a7>float</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) <b>action</b>);*  
*public [SettingSlider](API/MSCLoader/SettingSlider.md) <b>AddSlider</b>(string <b>id</b>, string <b>name</b>, int <b>value</b>, int <b>minValue</b>, int <b>maxValue</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b>);*

#### Description

Creates a slider for the settings window with a minimum and a maximum value. Can be configured with a parameter action or a regular non-parameter action. 
The parameter action calls your provided action with the current value of the setting as an argument.  
It can be set to either integer or float values, the float variant can be configured to round its value to specified digits.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
name | Text displayed as the name of the setting. Upper-case recommended. | <font color=#4170a7>string</font> | N/A
value | The default value for the setting. | <font color=#4170a7>int</font> / <font color=#4170a7>float</font> | N/A
minValue | The minimum value for the slider. | <font color=#4170a7>int</font> / <font color=#4170a7>float</font> | N/A
maxValue | The maximum value for the slider. | <font color=#4170a7>int</font> / <font color=#4170a7>float</font> | N/A
value | The default value for the setting. | <font color=#4170a7>int</font> / <font color=#4170a7>float</font> | N/A
roundDigits | The number of digits the value should be rounded to. | <font color=#4170a7>int</font> | 2
action | Action called whenever the value is changed. | [UnityAction\<<font color=#4170a7>float</font>\>](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction_1.html) / [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)  | N/A

#### Example

```csharp
SettingSlider mySlider;

public override void ModSettings()
{
    mySlider = modSettings.AddSlider("mySlider", "MY SLIDER", 2f, 1f, 5f, (value) => { ModConsole.Log($"This is the new value: {value}"); });
    // Whenever the value changes this will be logged in the console:
    // This is the new value: 3.0
}
```
# [ModSettings](API/MSCLoader/ModSettings.md).AddNumber

*public [SettingNumber](API/MSCLoader/SettingNumber.md) <b>AddNumber</b>(string <b>id</b>, float <b>value</b>);*  
*public [SettingNumber](API/MSCLoader/SettingNumber.md) <b>AddNumber</b>(string <b>id</b>, int <b>value</b>);*

#### Description

Creates a number setting hidden from the setting list, but it will still be saved and loaded like the other settings.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
value | Default number value. | <font color=#4170a7>float</font> / <font color=#4170a7>int</font> | N/A

#### Example

```csharp
SettingNumber myNumber;

public override void ModSettings()
{
    myNumber = modSettings.AddNumber("myNumber", 1f);

    myNumber.Value = 2f;
}
```
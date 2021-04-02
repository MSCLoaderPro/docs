# [ModSettings](API/MSCLoader/ModSettings.md).AddString

*public [SettingString](API/MSCLoader/SettingString.md) <b>AddString</b>(string <b>id</b>, string <b>value</b>);*

#### Description

Creates a string setting hidden from the setting list, but it will still be saved and loaded like the other settings.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
value | Default string value. | <font color=#4170a7>string</font> | N/A

#### Example

```csharp
SettingString myString;

public override void ModSettings()
{
    myString = modSettings.AddString("myString", "YEP");

    myString.Value = "NOPE";
}
```
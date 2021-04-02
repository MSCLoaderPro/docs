# [ModSettings](API/MSCLoader/ModSettings.md).AddBoolean

*public [SettingBoolean](API/MSCLoader/SettingBoolean.md) <b>AddBoolean</b>(string <b>id</b>, bool <b>value</b>);*

#### Description

Creates a boolean setting hidden from the setting list, but it will still be saved and loaded like the other settings.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
id | The unique identifier for the setting, used mainly for saving/loading the setting. | <font color=#4170a7>string</font> | N/A
value | Default boolean value. | <font color=#4170a7>bool</font> | N/A

#### Example

```csharp
SettingBoolean myBoolean;

public override void ModSettings()
{
    myBoolean = modSettings.AddBoolean("myBoolean", false);

    myBoolean.Value = true;
}
```
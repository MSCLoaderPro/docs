# [ModSettings](API/MSCLoader/ModSettings.md).AddSpacer

*public [SettingSpacer](API/MSCLoader/SettingSpacer.md) <b>AddSpacer</b>(float <b>height</b>);*

#### Description

Creates a spacer of specified height to the settings list.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
height | The height of the spacer (+(5 * 2) units, since that's the standard distance between settings, so a height of 0 means it's actually 10 units high, which is also the minimum so negative values won't work.). | <font color=#4170a7>float</font> | N/A

#### Example

```csharp
SettingSpacer mySpacer;

public override void ModSettings()
{
    mySpacer = modSettings.AddSpacer(10f);
}
```
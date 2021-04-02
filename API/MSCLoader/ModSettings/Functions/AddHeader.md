# [ModSettings](API/MSCLoader/ModSettings.md).AddHeader

*public [SettingHeader](API/MSCLoader/SettingHeader.md) <b>AddHeader</b>(string <b>text</b>);*  
*public [SettingHeader](API/MSCLoader/SettingHeader.md) <b>AddHeader</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>);*  
*public [SettingHeader](API/MSCLoader/SettingHeader.md) <b>AddHeader</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>textColor</b>);*  
*public [SettingHeader](API/MSCLoader/SettingHeader.md) <b>AddHeader</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>textColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>outlineColor</b>);*  

#### Description

Creates a simple text header for the settings window. You can configure its various colors if you want. We recommend to capitalize the text for the best look.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
text | The text displayed on the created header. | <font color=#4170a7>string</font> | N/A
backgroundColor | The header's background color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A
textColor | The header's text color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A
outlineColor | The header's outline color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A

#### Example

```csharp
SettingHeader myHeader;

public override void ModSettings()
{
    myHeader = modSettings.AddHeader("YEEHAW, THIS IS THE HEADER POLICE!");
}
```
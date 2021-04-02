# [ModSettings](API/MSCLoader/ModSettings.md).AddText

*public [SettingText](API/MSCLoader/SettingText.md) <b>AddText</b>(string <b>text</b>);*    
*public [SettingText](API/MSCLoader/SettingText.md) <b>AddText</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>);*    
*public [SettingText](API/MSCLoader/SettingText.md) <b>AddText</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>textColor</b>);*    
*public [SettingText](API/MSCLoader/SettingText.md) <b>AddText</b>(string <b>text</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>backgroundColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>textColor</b>, [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) <b>outlineColor</b>);*

#### Description

Creates a simple text for the settings window. You can configure its various colors if you want. We recommend to capitalize the text for the best look.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
text | The text to display. | <font color=#4170a7>string</font> | N/A
backgroundColor | The text's background color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A
textColor | The text's text color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A
outlineColor | The text's outline color. | [Color](https://docs.unity3d.com/500/Documentation/ScriptReference/Color.html) | N/A

#### Example

```csharp
SettingText myText;

public override void ModSettings()
{
    myText = modSettings.AddText("YEEHAW, THIS IS THE TEXT POLICE!\nYOU HAVE THE RIGHT TO REMAIN A MODDER,\nEVERYTHING YOU SAY OR SHOW WILL BE USED AGAINST YOU WITH RELEASE DATE QUESTIONS.\nYOU HAVE THE RIGHT TO PROPER TOOLS,\nIF YOU CAN'T MAKE THEM YOURSELF THEY WILL BE PROVIDED TO YOU IN THE FORM OF MOD LOADER PRO");
    // THIS IS THE TEXT POLICE!
    // YOU HAVE THE RIGHT TO REMAIN A MODDER,
    // EVERYTHING YOU SAY OR SHOW WILL BE USED AGAINST YOU WITH RELEASE DATE QUESTIONS.
    // YOU HAVE THE RIGHT TO PROPER TOOLS,
    // IF YOU CAN'T MAKE THEM YOURSELF THEY WILL BE PROVIDED TO YOU IN THE FORM OF MOD LOADER PRO
}
```
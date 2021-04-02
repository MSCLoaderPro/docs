# [ModConsole](API/MSCLoader/ModConsole.md).LogWarning

*public static void <b>LogWarning</b>(string <b>text</b>);*

#### Description

Logs a string as a warning into the ModConsole window, and also to the output_log.txt. This can also auto-open the console window depending on user settings (By default it does).

Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html)

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
text | String to log | <font color=#4170a7>string</font> | N/A

#### Example

```csharp
public override void OnSave() 
{
    ModConsole.LogWarning("I HAVE A BAD FEELING ABOUT THIS..");
}
```
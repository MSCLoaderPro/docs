# [ModConsole](API/MSCLoader/ModConsole.md).LogError

*public static void <b>LogError</b>(string <b>text</b>);*

#### Description

Logs a string as an error into the ModConsole window, and also to the output_log.txt. This can also auto-open the console window depending on user settings (By default it does).

Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html)

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
text | String to log | <font color=#4170a7>string</font> | N/A

#### Example

```csharp
public override void PostLoad() 
{
    ModConsole.LogError("I DON'T FEEL SO GOOD, MR. STORK");
}
```
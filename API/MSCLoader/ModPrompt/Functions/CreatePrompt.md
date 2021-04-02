# [ModPrompt](API/MSCLoader/ModPrompt.md).CreatePrompt

*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreatePrompt</b>(string <b>message</b>);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreatePrompt</b>(string <b>message</b>, string <b>title</b> = "MESSAGE");*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreatePrompt</b>(string <b>message</b>, string <b>title</b> = "MESSAGE", [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onPromptClose</b> = null);*

#### Description

Creates a prompt with the "OK" button with a **message** of your choosing with optional parameter **title** and optional **onPromptClose**, that's executed after prompt is closed.

### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
message | A message that will be displayed in the prompt. | <font color=#4170a7>string</font> | N/A
title | A title of the window. | <font color=#4170a7>string</font> | "MESSAGE"
onPromptClose | An action that will be exectued, when window is closed. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null

#### Example

```csharp
ModUI.CreatePrompt("Hello, world!")
/// Will create a prompt with "Hello, world!" message.

ModUI.CreatePrompt("Hello, Earth!", "My Mod");
// Will create a prompt with "Hello, Earth!" message and "My Mod" as a title.

ModUI.CreatePrompt("Hello, Mars!", "Mars Attacks!", () => ConquerEarth());
// Will create a prompt with "Hello, Mars!" message, "Mars Attacks!" as a title,
// and after the window gets closed, will execute "ConquerEarth" function.

void ConquerEarth()
{
    ModConsole.Log("ACK, ACK!")
}
```

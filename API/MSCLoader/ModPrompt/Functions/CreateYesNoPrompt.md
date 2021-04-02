# [ModPrompt](API/MSCLoader/ModPrompt.md).CreateYesNoPrompt

*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateYesNoPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onYes</b>);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateYesNoPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onYes</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onNo</b> = null);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateYesNoPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onYes</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onNo</b> = null, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onPromptClose</b> = null)*

#### Description

Creates a prompt with the "YES" and "NO" buttons with a **message** of your choosing, a **title**, an **onYes** action, which is executed when user clicks "YES" button.

An optional **onNo** action is available, which is executed when user presses "NO" buttton, and optional **onPromptClose** is executed, when prompt is closed.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ------- | -------
message | A message that will be displayed in the prompt. | <font color=#4170a7>string</font> | N/A
title | A title of the window. | <font color=#4170a7>string</font> | N/A
onYes | An action that will be executed, when user clicks "YES" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | N/A
onNo | An action that will be exectued, when user clicks "NO" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)| null
onPromptClose | An action that will be exectued, when the prompt is closed - regardless of player's choice. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null

#### Example

```csharp
ModUI.CreateYesNoPrompt("Do you like waffles?", "A question", () => ThatsCorrect());
// Will create a prompt with "Do you like waffles?" message, a "YES" and "NO" buttons,
// "A question" as a title, and uppon presing "YES", it will execute "ThatsCorrect()" function.

ModUI.CreateYesNoPrompt("Do you like pancakes?", "A question", () => ThatsCorrect(), () => Nope());
// Will create a prompt with "Do you like pancakes?" message, a "YES" and "NO" buttons,
// "A question" as a title, uppon presing "YES", it will execute "ThatsCorrect()" function,
// and uppon pressing "NO", it will execute "Nope()" function.

ModUI.CreateYesNoPrompt("Do you like french toasts?", "A question!", () => ThatsCorrect(), () => Nope(), () => StopIt());
// Will create a prompt with "Do you like french toasts?" message, a "YES" and "NO" buttons,
// "A question" as a title, uppon presing "YES", it will execute "ThatsCorrect()" function,
// uppon pressing "NO", it will execute "Nope()" function,
// and when the prompt gets closed (no matter what user presses), it will execute "StopIt()" function.
```

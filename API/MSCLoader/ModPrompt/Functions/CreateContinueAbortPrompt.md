# [ModPrompt](API/MSCLoader/ModPrompt.md).CreateContinueAbortPrompt

*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateContinueAbortPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onContinue</b>);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateContinueAbortPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onContinue</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onAbort</b> = null);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateContinueAbortPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onContinue</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onAbort</b> = null, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onPromptClose</b> = null);*

#### Description

Creates a prompt with the "CONTINUE" and "ABORT" buttons with a **message** of your choosing, a **title**, an **onContinue** action, which is executed when user clicks "CONTINUE" button.

An optional **onAbort** action is available, which is executed when user presses "ABORT" buttton, and optional **onPromptClose** is executed, when prompt is closed.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ------- | -------
message | A message that will be displayed in the prompt. | <font color=#4170a7>string</font> | N/A
title | A title of the window. | <font color=#4170a7>string</font> | N/A
onContinue | An action that will be executed, when user clicks "CONTINUE" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | N/A
onAbort | An action that will be exectued, when user clicks "ABORT" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null
onPromptClose | An action that will be exectued, when the prompt is closed - regardless of player's choice. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null

#### Example

```csharp
ModUI.CreateContinueAbortPrompt("Failed to pet the cat.", "Fatal Error", () => PetTheKitty());
// Will create a prompt with "Failed to pet the cat." message, a "CONTINUE" and "ABORT" buttons,
// "Fatal Error" as a title, and uppon presing "CONTINUE", it will execute "PetTheKitty()" function.

ModUI.CreateContinueAbortPrompt("Failed to pet the cat.", "Fatal Error", () => PetTheKitty(), () => LeaveKittyAlone());
// Will create a prompt with "Failed to pet the cat." message, a "CONTINUE" and "ABORT" buttons,
// "Fatal Error" as a title, uppon presing "CONTINUE", it will execute "PetTheKitty()" function,
// and uppon pressing "ABORT", it will execute "LaveKittyAlone()" function.

ModUI.CreateContinueAbortPrompt("Failed to pet the cat.", "Fatal Error", () => PetTheKitty(), () => LeaveKittyAlone(), () => FeedTheKitty());
// Will create a prompt with "Failed to pet the cat." message, a "CONTINUE" and "ABORT" buttons,
// "Fatal Error" as a title, uppon presing "CONTINUE", it will execute "PetTheKitty()" function,
// uppon pressing "ABORT", it will execute "LaveKittyAlone()" function,
// and when prompt is closed (no matter user choice), it will execute "FeedTheKitty()" function.
```

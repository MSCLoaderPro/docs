# [ModPrompt](API/MSCLoader/ModPrompt.md).CreateRetryCancelPrompt

*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateRetryCancelPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onRetry</b>);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateRetryCancelPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onRetry</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onCancel</b> = null);*  
*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateRetryCancelPrompt</b>(string <b>message</b>, string <b>title</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onRetry</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onCancel</b> = null, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>onPromptClose</b> = null);*

#### Description

Creates a prompt with the "RETRY" and "CANCEL" buttons with a **message** of your choosing, a **title**, an **onRetry** action, which is executed when user clicks "RETRY" button.

An optional **onCancel** action is available, which is executed when user presses "CANCEL" buttton, and optional **onPromptClose** is executed, when prompt is closed.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ------- | -------
message | A message that will be displayed in the prompt. | <font color=#4170a7>string</font> | N/A
title | A title of the window. | <font color=#4170a7>string</font> | N/A
onRetry | An action that will be executed, when user clicks "RETRY" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | N/A
onCancel | An action that will be exectued, when user clicks "CANCEL" button. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null
onPromptClose | An action that will be exectued, when the prompt is closed - regardless of player's choice. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) | null

#### Example

```csharp
ModUI.CreateRetryCancelPrompt("Could not compute the meaning of life.", "Fatal Error", () => FindPurposeOfLife());
// Will create a prompt with "Could not compute the meaning of life." message, a "RETRY" and "CANCEL" buttons,
// "Fatal Error" as a title, and uppon presing "RETRY", it will execute "FindPurposeOfLife()" function.

ModUI.CreateRetryCancelPrompt("Could not compute the meaning of life.", "Fatal Error", () => FindMeaningOfLife(), () => FourtyTwo());
// Will create a prompt with "Could not compute the meaning of life." message, a "RETRY" and "CANCEL" buttons,
// "Fatal Error" as a title, uppon presing "RETRY", it will execute "FindPurposeOfLife()" function,
// and uppon pressing "CANCEL", it will execute "FourtyTwo()" function.

ModUI.CreateRetryCancelPrompt("Could not compute the meaning of life.", "Fatal Error", () => FindMeaningOfLife(), () => FourtyTwo(), () => TheAnswerOfLifeUniverseAndEverything());
// Will create a prompt with "Could not compute the meaning of life." message, a "RETRY" and "CANCEL" buttons,
// "Fatal Error" as a title, uppon presing "RETRY", it will execute "FindPurposeOfLife()" function,
// uppon pressing "CANCEL", it will execute "FourtyTwo()" function,
// and when prompt is closed (regardless of user's choice), it will execute "TheAnswerOfLifeUniverseAndEverything()" function.
```

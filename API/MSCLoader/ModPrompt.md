# ModPrompt

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

A managing component of prompt. Allows you to easily create a new prompt/message box

### Variables

Name | Description | Type
---- | ----------- | -----
[DestroyOnDisable](API/MSCLoader/ModPrompt/Variables/DestroyOnDisable) | Should the ModPrompt be destroyed after being disabled. (Enabled by default) | <font color=#4170a7>bool</font>
[OnCloseAction](API/MSCLoader/ModPrompt/Variables/OnCloseAction.md) | An action that's executed when the window gets closed. | [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html)
[Text](API/MSCLoader/ModPrompt/Variables/Text.md) | The main text of the prompt | <font color=#4170a7>string</font>
[Title](API/MSCLoader/ModPrompt/Variables/Title.md) | Title of the prompt. | <font color=#4170a7>string</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[AddButton](API/MSCLoader/ModPrompt/Functions/AddButton.md) | Lets you add a new button. | <font color=#4170a7>void</font>

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[CreateContinueAbortPrompt](API/MSCLoader/ModPrompt/Functions/CreateContinueAbortPrompt.md) | Creates a [ModPrompt](API/MSCLoader/ModPrompt.md) with "Continue" and "Abort" buttons. | [ModPrompt](API/MSCLoader/ModPrompt.md)
[CreatePrompt](API/MSCLoader/ModPrompt/Functions/CreatePrompt.md) | Creates a simple [ModPrompt](API/MSCLoader/ModPrompt.md) with OK button. | [ModPrompt](API/MSCLoader/ModPrompt.md)
[CreateRetryCancelPrompt](API/MSCLoader/ModPrompt/Functions/CreateRetryCancelPrompt.md) | Creates a [ModPrompt](API/MSCLoader/ModPrompt.md) with "Retry" and "Cancel" buttons. | [ModPrompt](API/MSCLoader/ModPrompt.md)
[CreateYesNoPrompt](API/MSCLoader/ModPrompt/Functions/CreateYesNoPrompt.md) | Creates a [ModPrompt](API/MSCLoader/ModPrompt.md) with "Yes" and "No" buttons. | [ModPrompt](API/MSCLoader/ModPrompt.md)
[CreateCustomPrompt](API/MSCLoader/ModPrompt/Functions/CreateCustomPrompt.md) | Creates a [ModPrompt](API/MSCLoader/ModPrompt.md) that does not have any buttons, or text assigned to it. | [ModPrompt](API/MSCLoader/ModPrompt.md)

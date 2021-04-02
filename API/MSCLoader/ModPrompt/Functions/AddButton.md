# [ModPrompt](API/MSCLoader/ModPrompt.md).AddButton

*public [ModPromptButton](API/MSCLoader/ModPromptButton.md) <b>AddButton</b>(string <b>buttonText</b>, [UnityAction](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityAction.html) <b>action</b>)*

#### Description

Adds a button to prompt with a custom text and action that will be exectued by that button.

#### Example

```csharp
ModPrompt prompt;

/* .. */

prompt.AddButton("My button", () => NewButtonAction());

void NewButtonAction()
{
    ModConsole.Log("\"My button\" has been pressed!);

    // CONSOLE OUTPUT:
    // "My button" has been pressed!
}
```

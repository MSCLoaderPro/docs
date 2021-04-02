# [ModPrompt](API/MSCLoader/ModPrompt.md).Text

*public string Text { get; set; }*

#### Description

Text that is shown inside of the main part of a prompt.

#### Example

```csharp
ModPrompt prompt;

/* .. */

void SetPromptText(string text)
{
    prompt.Text = text;
}
```

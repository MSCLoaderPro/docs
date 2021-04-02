# [ModPrompt](API/MSCLoader/ModPrompt.md).Title

*public string Title { get; set; }*

#### Description

A text displayed on top of the prompt.

#### Example

```csharp
ModPrompt prompt;

/* .. */

void SetPromptTitle(string text)
{
    prompt.Title = text;
}
```

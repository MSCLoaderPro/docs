# [ModPrompt](API/MSCLoader/ModPrompt.md).CreateCustomPrompt

*public static [ModPrompt](API/MSCLoader/ModPrompt.md) <b>CreateCustomPrompt</b>();*

#### Description

Creates a generic prompt with default parameters and no buttons by default. A message, title and eventual buttons have to be provided.

Please refer to [ModPrompt](API/MSCLoader/ModPrompt.md) for more information.

!> If no button has been provided, an functionless "OK" button will be added.

#### Example

```csharp
ModPrompt myPrompt = ModUI.CreateCustomPrompt();
myPrompt.Text = "That parrot is dead!";
myPrompt.Title = "Customer";
myPrompt.AddButton("No, it's resting!")
myPrompt.AddButton("You're correct, sir", () => Refund());

// This will generate a prompt which would look like this:

// --------------------------------------------------
// |                    Customer                    |
// _________________________________________________|
// |               That parrot is dead!             |
// __________________________________________________
// |    No, it's resting!   |   You're correct, sir |
// __________________________________________________
```

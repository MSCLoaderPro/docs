# [Mod](API/MSCLoader/Mod.md).Author

*public string <b>Author</b> { get; set; }*

#### Description

Returns the mod Author, used for display purposes in the UI.  
Recommended to be capitalized for the best look in the UI!

#### Example

```csharp
public override string Author => "IT'S A ME!";

void GetModAuthor()
{
    Mod myMod = this;
    string modAuthor = myMod.Author;
    ModConsole.Log(modAuthor);

    // CONSOLE OUTPUT:
    // IT'S A ME!
}
```

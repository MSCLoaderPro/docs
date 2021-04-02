# [Mod](API/MSCLoader/Mod.md).Name

*public string <b>Name</b> { get; set; }*

#### Description

Returns the mod Name, a string used for display purposes in the UI.  
Recommended to be capitalized for the best look in the UI!

#### Example

```csharp
public override string Name => "MY MOD";

void GetModName()
{
    Mod myMod = this;
    string modName = myMod.Name;
    ModConsole.Log(modName);
    
    // CONSOLE OUTPUT:
    // My Mod
}
```

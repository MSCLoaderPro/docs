# [Mod](API/MSCLoader/Mod.md).ID

*public string <b>ID</b> { get; }*

#### Description

Returns the mod ID, should be unique to the mod.

#### Example

```csharp
public override string ID => "MyMod";

void GetModID()
{
    Mod myMod = this;
    string modID = myMod.ID;
    ModConsole.Log(modID);
    
    // CONSOLE OUTPUT:
    // MyMod
}
```

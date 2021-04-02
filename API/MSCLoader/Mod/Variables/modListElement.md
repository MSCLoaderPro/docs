# [Mod](API/MSCLoader/Mod.md).modListElement

*public [ModListElement](API/MSCLoader/ModListElement.md) <b>modListElement</b> { get; }*

#### Description

Returns the mod's mod list element. The UI controller for the mods mod list entry.

#### Example

```csharp
void DisableMod()
{
    Mod mod = this;
    modListElement.SetModEnabled(false);
    ModConsole.Log(mod.Enabled);
    
    // CONSOLE OUTPUT:
    // False
}
```

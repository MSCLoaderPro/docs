# [Mod](API/MSCLoader/Mod.md).Enabled

*public bool <b>Enabled</b> { get; }*

#### Description

Returns if the mod is enabled.

#### Example

```csharp
void GetModEnabled() 
{
	Mod myMod = this;
    bool enabled = myMod.Enabled;
    ModConsole.Log(enabled);
    
    // CONSOLE OUTPUT:
    // True
}
```

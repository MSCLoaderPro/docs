# [Mod](API/MSCLoader/Mod.md).Version

*public string <b>Version</b> { get; }*

#### Description

Returns the mod version. This is also used to determine the newer version when the Mod Loader searches for updates for your mod (Provided you have assigned an [UpdateLink](API/MSCLoader/Mod/Variables/UpdateLink.md) to your mod).

#### Example

```csharp
public override string Version => "1.0";

void GetModVersion()
{
    Mod myMod = this;
    string modVersion = myMod.Version;
    ModConsole.Log(modVersion);
    
    // CONSOLE OUTPUT:
    // 1.0
}
```

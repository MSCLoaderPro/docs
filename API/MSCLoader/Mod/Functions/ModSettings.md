# [Mod](API/MSCLoader/Mod.md).ModSettings

*public override void <b>ModSettings</b>();*

#### Description

Method useful for creating settings for your mod. It's the method called absolutely first for all mods.

**Order of execution**: 1.

#### Example

```csharp
public override void ModSettings()
{
    modSettings.AddHeader("MY MOD SETTINGS!");
    // This will create a header in your mod's settings list.
}
```

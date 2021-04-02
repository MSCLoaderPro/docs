# [Mod](API/MSCLoader/Mod.md).ModSettingsLoaded

*public override void <b>ModSettingsLoaded</b>();*

#### Description

Can be used, for example, to access settings of other mods. This is called after every other mod has had their [ModSettings()](API/MSCLoader/Mod/Functions/ModSettings.md) called.

**Order of execution**: 2.

#### Example

```csharp
public override void ModSettingsLoaded()
{
    // Whatever you want.
}
```

# [Mod](API/MSCLoader/Mod.md).MenuOnLoad

*public override void <b>MenuOnLoad</b>();*

#### Description

Called in the Main Menu once, after [ModSettings()](API/MSCLoader/Mod/Functions/ModSettings.md) and [ModSettingsLoaded()](API/MSCLoader/Mod/Functions/ModSettingsLoaded.md) has been called. This will only be called if the mod is enabled.

**Order of execution**: 3.

#### Example

```csharp
public override void MenuOnLoad()
{
    // Whatever you want.
}
```

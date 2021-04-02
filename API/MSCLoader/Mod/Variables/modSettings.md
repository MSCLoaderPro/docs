# [Mod](API/MSCLoader/Mod.md).modSettings

*public [ModSettings](API/MSCLoader/ModSettings.md) <b>modSettings</b> { get; }*

#### Description

Returns the mod's [ModSettings](API/MSCLoader/ModSettings.md) component. This is the main component you'd need when adding settings to your mod.

#### Example

```csharp
SettingToggle myToggle;

public override void ModSettings()
{
    myToggle = modSettings.AddToggle("toggleID", "TOGGLE NAME", false);
    // THIS WILL ADD A TOGGLE TO YOUR MOD'S SETTINGS LIST, WITH A DEFAULT VALUE OF FALSE.
}
```
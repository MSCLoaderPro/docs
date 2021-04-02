# [Mod](API/MSCLoader/Mod.md).UpdateLink

*public string <b>UpdateLink</b> { get; }*

#### Description

Returns the mod update link. Usually a link to the game's mod page on either Nexusmods or Github.  
Used by the Mod Loader when checking for updates.

#### Example

```csharp
public override string UpdateLink => "https://www.nexusmods.com/mysummercar/mods/9999";

void GetModUpdateLink()
{
    Mod myMod = this;
    string modUpdateLink = myMod.UpdateLink;
    ModConsole.Log(modUpdateLink);
    
    // CONSOLE OUTPUT:
    // https://www.nexusmods.com/mysummercar/mods/9999
}
```

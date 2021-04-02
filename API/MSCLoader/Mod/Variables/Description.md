# [Mod](API/MSCLoader/Mod.md).Description

*public string <b>Description</b> { get; set; }*

#### Description

Returns the mod description. This should be a fairly short and concise description of what your mod does.  
Displayed in the Mod's setting list, recommended to be capitalized for the best look in the UI.  
Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html).

#### Example

```csharp
public override string Description => "HI, THIS IS MY MOD. IT DOES ALL THESE THINGS.\nHAVE A NICE DAY!";

void GetModDescription()
{
    Mod myMod = this;
    string modDescription = myMod.Description;
    ModConsole.Log(modDescription);
    
    // CONSOLE OUTPUT:
    // HI, THIS IS MY MOD. IT DOES ALL THESE THINGS.
    // HAVE A NICE DAY!
}
```

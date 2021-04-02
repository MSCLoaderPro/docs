# [Mod](API/MSCLoader/Mod.md).Icon

*public byte[] <b>Icon</b> { get; set; }*

#### Description

Returns the mod icon. This is a byte array containing a png/jpg image.  
Look at [INSERT LINK TO GUIDE ON MOD ICONS HERE!]() for examples on how to add an icon to your mod.  
Displayed in the Mod List.

#### Example

```csharp
public override byte[] Icon => Properties.Resources.Icon;
```

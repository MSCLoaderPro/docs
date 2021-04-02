# [Mod](API/MSCLoader/Mod.md).PostLoad

*public override void <b>PostLoad</b>();*

#### Description

Called after one frame after [OnLoad](API/MSCLoader/Mod/Functions/OnLoad.md) has been completed for all enabled mods. This can, for example, be used to communicate and alter other mods for compatibility reasons, mod of a mod etc.

**Order of execution**: 7.

#### Example

```csharp
public override void PostLoad()
{
    // Whatever you want.
}
```

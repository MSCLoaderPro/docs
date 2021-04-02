# [Mod](API/MSCLoader/Mod.md).MenuFixedUpdate

*public override void <b>MenuFixedUpdate</b>();*

#### Description

Called in the Main Menu on every fixed framerate frame (default is every 0.02s in My Summer Car) from a regular Unity [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html).[FixedUpdate](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.FixedUpdate.html).

**Order of execution**: Every fixed framerate frame (Menu).

#### Example

```csharp
public override void MenuFixedUpdate()
{
    // Whatever you want.
}
```

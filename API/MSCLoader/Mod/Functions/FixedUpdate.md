# [Mod](API/MSCLoader/Mod.md).FixedUpdate

*public override void <b>FixedUpdate</b>();*

#### Description

Called in the game scene on every fixed framerate frame (default is every 0.02s in My Summer Car) from a regular Unity [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html).[FixedUpdate](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.FixedUpdate.html). This won't start executing until every mod has loaded fully, after [PostLoad](API/MSCLoader/Mod/Functions/PostLoad.md).

**Order of execution**: Every fixed framerate frame.

#### Example

```csharp
public override void FixedUpdate()
{
    // Whatever you want.
}
```

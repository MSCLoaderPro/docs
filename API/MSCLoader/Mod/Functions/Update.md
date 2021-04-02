# [Mod](API/MSCLoader/Mod.md).Update

*public override void <b>Update</b>();*

#### Description

Called in the game scene on every frame from a regular Unity [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html).[Update](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.Update.html). This won't start executing until every mod has loaded fully, after [PostLoad](API/MSCLoader/Mod/Functions/PostLoad.md).

**Order of execution**: Every frame.

#### Example

```csharp
public override void Update()
{
    // Whatever you want.
}
```

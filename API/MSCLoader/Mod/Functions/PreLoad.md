# [Mod](API/MSCLoader/Mod.md).PreLoad

*public override void <b>PreLoad</b>();*

#### Description

Called as soon as the game scene is loaded (On starting a new game it's called one frame after [OnNewGame](API/MSCLoader/Mod/Functions/OnNewGame.md)). Can be used to, for example, prevent item fall-through for mod objects (such as vehicles, furniture etc) where a game item is on the ground after the game has loaded fully when it was on top of the mod object previously.

**Order of execution**: 5.

#### Example

```csharp
public override void PreLoad()
{
    // Whatever you want.
}
```

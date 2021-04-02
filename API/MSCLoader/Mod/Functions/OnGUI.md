# [Mod](API/MSCLoader/Mod.md).OnGUI

*public override void <b>OnGUI</b>();*

#### Description

Called in the game scene on each call of OnGUI from a regular Unity [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html).[OnGUI](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.OnGUI.html). Use to draw [Unity Legacy GUI](https://docs.unity3d.com/500/Documentation/Manual/GUIScriptingGuide.html). This won't start executing until every mod has loaded fully, after [PostLoad](API/MSCLoader/Mod/Functions/PostLoad.md).

**Order of execution**: Every OnGUI call.

#### Example

```csharp
public override void OnGUI()
{
    if (GUI.Button(new Rect(10, 10, 150, 100), "I am a button"))
            ModConsole.Log("You clicked the button!");
}
```

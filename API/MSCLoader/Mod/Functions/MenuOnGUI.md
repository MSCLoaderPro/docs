# [Mod](API/MSCLoader/Mod.md).MenuOnGUI

*public override void <b>MenuOnGUI</b>();*

#### Description

Called in the Main Menu on each call of OnGUI from a regular Unity [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html).[OnGUI](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.OnGUI.html). Use to draw [Unity Legacy GUI](https://docs.unity3d.com/500/Documentation/Manual/GUIScriptingGuide.html) in the menu.

**Order of execution**: Every OnGUI call (Menu).

#### Example

```csharp
public override void MenuOnGUI()
{
    if (GUI.Button(new Rect(10, 10, 150, 100), "I am a button"))
            ModConsole.Log("You clicked the button!");
}
```

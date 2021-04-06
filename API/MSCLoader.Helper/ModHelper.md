# ModHelper

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

This contains various methods that might be helpful when making mods, easily finding [GameObjects](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html), [Transforms](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html), maybe selecting a random element in a given list or array, check if a layer is inside a [LayerMask](https://docs.unity3d.com/500/Documentation/ScriptReference/LayerMask.html) or perhaps just playing a sound from the game.

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[MakePickable](API/MSCLoader.Helper/ModHelper/Functions/MakePickable.md) | Extension method that puts a [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) or [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) into the **Parts** layer and optionally gives it the **PART** tag.  | <font color=#4170a7>void</font>
[GetTransform](API/MSCLoader.Helper/ModHelper/Functions/GetTransform.md) | Get a child [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) from a parent object and sub-path to your wanted object. | [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html)
[GetGameObject](API/MSCLoader.Helper/ModHelper/Functions/GetGameObject.md) | Get a child [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) from a parent object and sub-path to your wanted object. | [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html)
[PlaySound3D](API/MSCLoader.Helper/ModHelper/Functions/PlaySound3D.md) | Extension method allowing you to play a sound from the game on a [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) or a (global) [Vector3](https://docs.unity3d.com/500/Documentation/ScriptReference/Vector3.html) position using MasterAudio. | <font color=#4170a7>void</font>
[SelectRandom](API/MSCLoader.Helper/ModHelper/Functions/SelectRandom.md) | Extension method allowing you to select a random element <font color="#aac397">T</font> from a list or array. | <font color="#aac397">T</font>
[InLayerMask](API/MSCLoader.Helper/ModHelper/Functions/InLayerMask.md) | Extension method for checking if a layer (by name or number) is in a given [LayerMask](https://docs.unity3d.com/500/Documentation/ScriptReference/LayerMask.html). |<font color=#4170a7>bool</font>
[SetParent](API/MSCLoader.Helper/ModHelper/Functions/SetParent.md) | Extension method to set a parent for a [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) and immediately setting its local position, rotation and scale (and optionally its name). |<font color=#4170a7>void</font>
[OpenFolder](API/MSCLoader.Helper/ModHelper/Functions/OpenFolder.md) | Opens a specified folder in the explorer. |<font color=#4170a7>void</font>
[OpenWebsite](API/MSCLoader.Helper/ModHelper/Functions/OpenWebsite.md) | Opens a specified URL in the users default web browser. |<font color=#4170a7>void</font>
[IsWithinRange](API/MSCLoader.Helper/ModHelper/Functions/IsWithinRange.md) | Check if an int is within a given range. |<font color=#4170a7>bool</font>

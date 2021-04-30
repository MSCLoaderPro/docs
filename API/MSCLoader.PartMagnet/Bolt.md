# Bolt

*Namespace: MSCLoader.PartMagnet / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

Bolt container class, this controls a bolt for the [BoltMagnet](API/MSCLoader.PartMagnet/BoltMagnet.md) system.

### Variables

Name | Description | Type
---- | ----------- | ----
[boltMagnet](API/MSCLoader.PartMagnet/Bolt/Variables/boltMagnet.md) | Linked [BoltMagnet](API/MSCLoader.PartMagnet/BoltMagnet.md) Component. | [BoltMagnet](API/MSCLoader.PartMagnet/BoltMagnet.md)
[boltSize](API/MSCLoader.PartMagnet/Bolt/Variables/boltSize.md) | Size of the bolt from the game's available tool sizes. | <font color="#aac397">BoltSize</font>
[tightness](API/MSCLoader.PartMagnet/Bolt/Variables/tightness.md) | Current tightness. This is increased/decreased as the bolt is screwed. | <font color=#4170a7>int</font>
[minTightness](API/MSCLoader.PartMagnet/Bolt/Variables/minTightness.md) | Min tightness of the bolt. | <font color=#4170a7>int</font>
[maxTightness](API/MSCLoader.PartMagnet/Bolt/Variables/maxTightness.md) | Max tightness of the bolt. | <font color=#4170a7>int</font>
[tightnessPositionDelta](API/MSCLoader.PartMagnet/Bolt/Variables/tightnessPositionDelta.md) | Change in position each screw. | [Vector3](https://docs.unity3d.com/500/Documentation/ScriptReference/Vector3.html)
[tightnessRotationDelta](API/MSCLoader.PartMagnet/Bolt/Variables/tightnessRotationDelta.md) | Change in rotation each screw. | [Vector3](https://docs.unity3d.com/500/Documentation/ScriptReference/Vector3.html)
[allowRatchetWrench](API/MSCLoader.PartMagnet/Bolt/Variables/allowRatchetWrench.md) | Allow the ratchet wrench to be used on the bolt. | <font color=#4170a7>bool</font>
[highlightBolt](API/MSCLoader.PartMagnet/Bolt/Variables/highlightBolt.md) | Highlight the bolt when hovering with the right tool over it. | <font color=#4170a7>bool</font>
[customAudioSource](API/MSCLoader.PartMagnet/Bolt/Variables/customAudioSource.md) | (OPTIONAL) Custom audiosource that'll play the custom sounds. | [AudioSource](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioSource.html)
[customScrewInSound](API/MSCLoader.PartMagnet/Bolt/Variables/customScrewInSound.md) | (OPTIONAL) Custom screw in sound. | [AudioClip](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioClip.html)
[customScrewOutSound](API/MSCLoader.PartMagnet/Bolt/Variables/customScrewOutSound.md) | (OPTIONAL) Custom screw out sound. | [AudioClip](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioClip.html)
[deltaBreakForce](API/MSCLoader.PartMagnet/Bolt/Variables/deltaBreakForce.md) | (OPTIONAL) Change in joint break force each screw. | <font color=#4170a7>float</font>
[deltaBreakTorque](API/MSCLoader.PartMagnet/Bolt/Variables/deltaBreakTorque.md) | (OPTIONAL) Change in joint break torque each screw. | <font color=#4170a7>float</font>
[customHighlightMaterial](API/MSCLoader.PartMagnet/Bolt/Variables/customHighlightMaterial.md) | (OPTIONAL) Custom hightlight material for the hovering over. | [Material](https://docs.unity3d.com/500/Documentation/ScriptReference/Material.html)
[size](API/MSCLoader.PartMagnet/Bolt/Variables/size.md) | Raw size of the bolt, not locked to game's available tools. | <font color=#4170a7>float</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[Reset](API/MSCLoader.PartMagnet/Bolt/Functions/Reset.md) | Reset the bolt to minTightness. | <font color=#4170a7>void</font>

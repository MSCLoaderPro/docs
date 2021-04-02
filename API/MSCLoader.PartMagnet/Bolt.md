# Bolt
Namespace: MSCLoader.PartMagnet / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)
#### Description <!-- {docsify-ignore} -->
A class to control the bolting aspect of a [Bolt Magnet]()
#### Variables <!-- {docsify-ignore} -->

>[BoltMagnet]() Linked BoltMagnet Component.<br>
>[BoltSize](MSCLoader.PartMagnet/Bolt/BoltSize.md) Size of the bolt from the game's available tool sizes.<br>
>[tightness](MSCLoader.PartMagnet/Bolt/tightness.md) Current tightness. This is increased/decreased as the bolt is screwed.<br>
>[minTightness](MSCLoader.PartMagnet/Bolt/minTightness.md) Min tightness of the bolt.<br>
>[maxTightness](#Bolt) Max tightness of the bolt.<br>
>[tightnessPositionDelta](#Bolt) Change in position each screw.<br>
>[tightnessRotationDelta](#Bolt) Change in rotation each screw.<br>
>[allowRatchetWrench](#Bolt) Allow the ratchet wrench to be used on the bolt.<br>
>[highlightBolt](#Bolt) Highlight the bolt when hovering with the right tool over it.<br>
>[customAudioSource](#Bolt) (OPTIONAL) Custom audiosource that'll play the custom sounds.<br>
>[customScrewInSound](#Bolt) (OPTIONAL) Custom screw in sound.<br>
>[customScrewOutSound](#Bolt) (OPTIONAL) Custom screw out sound.<br>
>[deltaBreakForce](#Bolt) (OPTIONAL) Change in joint break force each screw.<br>
>[deltaBreakTorque](#Bolt) (OPTIONAL) Change in joint break torque each screw.<br>
>[customHighlightMaterial](#Bolt) (OPTIONAL) Custom hightlight material for the hovering over.<br>
>[size](#Bolt) Raw size of the bolt, not locked to game's available tools.<br>

#### Public Functions <!-- {docsify-ignore} -->
>[Reset](#Bolt) Reset the bolt to minTightness.





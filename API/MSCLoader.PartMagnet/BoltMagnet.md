# BoltMagnet

*Namespace: MSCLoader.PartMagnet / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

Highly configurable part attachment script which supports a practically unlimited amount of attachment points and bolts. It can be a static part that can't be broken off, and it can be a part that does break off if enough force or torque acts upon it.  
Custom sounds for attaching and detaching can be provided, otherwise it will use the game's default sounds. You can add certain actions that executes either when the part attaches or when it detaches.

### Variables

Name | Description | Type
---- | ----------- | ----
[attachmentType](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attachmentType.md) | Type of attachment, static or breakable. | <font color="#aac397">AttachmentType</font>
[attachmentPoints](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attachmentPoints.md) | Array of potential attachment points. | [Collider](https://docs.unity3d.com/500/Documentation/ScriptReference/Collider.html)[]
[bolts](API/MSCLoader.PartMagnet/BoltMagnet/Variables/bolts.md) | Array of the part's bolts. | [Bolt](API/MSCLoader.PartMagnet/Bolt.md)[]
[attachText](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attachText.md) | (OPTIONAL) Interaction text appearing when the attach prompt appears (in addition to the attach icon). | <font color=#4170a7>string</font>
[detachText](API/MSCLoader.PartMagnet/BoltMagnet/Variables/detachText.md) | (OPTIONAL) Interaction text appearing when the detach prompt appears (in addition to the detach icon). | <font color=#4170a7>string</font>
[attachmentPointsRigidbody](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attachmentPointsRigidbody.md) | (OPTIONAL) Specific rigidbodies to attach breakable parts to, else it looks for the best match. Should coincide with the same index as the relevant attachment point. | [Rigidbody](https://docs.unity3d.com/500/Documentation/ScriptReference/Rigidbody.html)[]
[customAudioSource](API/MSCLoader.PartMagnet/BoltMagnet/Variables/customAudioSource.md) | (OPTIONAL) Custom audiosource that'll play the custom sounds. | [AudioSource](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioSource.html)
[customAssembleSound](API/MSCLoader.PartMagnet/BoltMagnet/Variables/customAssembleSound.md) | (OPTIONAL) Custom attach sound. | [AudioClip](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioClip.html)
[customDisassembleSound](API/MSCLoader.PartMagnet/BoltMagnet/Variables/customDisassembleSound.md) | (OPTIONAL) Custom detach sound. | [AudioClip](https://docs.unity3d.com/500/Documentation/ScriptReference/AudioClip.html)
[baseBreakForce](API/MSCLoader.PartMagnet/BoltMagnet/Variables/baseBreakForce.md) | (OPTIONAL) Base joint break force for breakable parts. | <font color=#4170a7>float</font>
[baseBreakTorque](API/MSCLoader.PartMagnet/BoltMagnet/Variables/baseBreakTorque.md) | (OPTIONAL) Base joint break torque for breakable parts. | <font color=#4170a7>float</font>
[OnAttach](API/MSCLoader.PartMagnet/BoltMagnet/Variables/OnAttach.md) | (OPTIONAL) Event executing assigned actions whenever the part gets attached. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html)
[OnDetach](API/MSCLoader.PartMagnet/BoltMagnet/Variables/OnDetach.md) | (OPTIONAL) Event executing assigned actions whenever the part gets detached. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html)
[joint](API/MSCLoader.PartMagnet/BoltMagnet/Variables/joint.md) | Joint used when part is attached, null when detached. | [FixedJoint](https://docs.unity3d.com/500/Documentation/ScriptReference/FixedJoint.html)
[attached](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attached.md) | Whether or not the part is currently attached to an attachment point. | <font color=#4170a7>bool</font>
[attachmentPointIndex](API/MSCLoader.PartMagnet/BoltMagnet/Variables/attachmentPointIndex.md) | Current attachment point index the part is attached to. | <font color=#4170a7>int</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[Setup](API/MSCLoader.PartMagnet/BoltMagnet/Functions/Setup.md) | Attach the part on the specified and bolt tightness. | <font color=#4170a7>void</font>
[Save](API/MSCLoader.PartMagnet/BoltMagnet/Functions/Save.md) | Save the attached status, attachment index and bolt tightness into the BoltMagnetSaveData class, can be used to easily save your part with the [ModSave](API/MSCLoader/ModSave.md) system. | [BoltMagnetSaveData](API/MSCLoader.PartMagnet/BoltMagnetSaveData.md)
[Attach](API/MSCLoader.PartMagnet/BoltMagnet/Functions/Attach.md) | Attach the part on the specified collider. | <font color=#4170a7>void</font>
[Detach](API/MSCLoader.PartMagnet/BoltMagnet/Functions/Detach.md) | Detach the part. | <font color=#4170a7>void</font>
[UpdateJointBreakValues](API/MSCLoader.PartMagnet/BoltMagnet/Functions/UpdateJointBreakValues.md) | Update the parts joint break value according to bolts and base break values. | <font color=#4170a7>void</font>

# PlayMakerProxyHelper

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

This contains various methods that'll help with manipulating and modifying PlayMakerArrayListProxy and PlayMakerHashTableProxy components.  
Whether you'd want to add certain values or clear the proxies, you have that ability here.

### Extension Functions

Name | Description | Returns
---- | ----------- | -------
[GetArrayListProxy](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/GetArrayListProxy.md) | Extension method for a [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) or [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) to find a PlayMakerArrayListProxy component by its reference name. | PlayMakerArrayListProxy
[GetHashTableProxy](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/GetHashTableProxy.md) | Extension method for a [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) or [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) to find a PlayMakerHashTableProxy component by its reference name. | PlayMakerHashTableProxy
[Add](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/Add.md) | Add a value or a range of values to the ArrayList or HashTable, note that they must have the same type as the proxy's prefillType. | <font color=#4170a7>void</font>
[Clear](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/Clear.md) | Clear the ArrayList or HashTable, optionally also clear its prefill lists. | <font color=#4170a7>void</font>
[AddPrefill](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/AddPrefill.md) | Add a value or a range of values to the ArrayList or HashTable prefill list, note that they must have the same type as the proxy's prefillType. | <font color=#4170a7>void</font>
[ClearPrefill](API/MSCLoader.Helper/PlayMakerProxyHelper/Functions/ClearPrefill.md) | Clear the ArrayList or HashTable prefill list. | <font color=#4170a7>void</font>
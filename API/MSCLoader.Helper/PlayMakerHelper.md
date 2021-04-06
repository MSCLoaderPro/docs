# PlayMakerHelper

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

This contains various methods that'll help with manipulating and modifying [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) components.  
Finding states on a FSM, adding/inserting/removing actions to/in/from states, getting variables by type and name and easy access to the various GUI icons/text found in the game (interaction text, attach/detach icons, drive icon, use icon etc.).

### Variables

Name | Description | Type
---- | ----------- | -----
[FSMGUIUse](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIUse) | Use icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIAssemble](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIAssemble) | Assemble icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIDisassemble](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIDisassemble) | Disassemble icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIBuy](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIBuy) | Buy icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIDrive](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIDrive) | Drive icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIPassenger](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIPassenger) | Passenger icon FSM global variable. | [FSMBool](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUIInteraction](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUIInteraction) | Interaction text FSM global variable. | [FSMString](https://hutonggames.fogbugz.com/default.asp?W1103)
[FSMGUISubtitle](API/MSCLoader.Helper/PlayMakerHelper/Variables/FSMGUISubtitle) | Subtitle text FSM global variable. | [FSMString](https://hutonggames.fogbugz.com/default.asp?W1103)
[GUIUse](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUIUse) | Get/Set the Use icon visibility. | <font color=#4170a7>bool</font>
[GUIAssemble](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUIAssemble) | Get/Set the Assemble icon visibility. | <font color=#4170a7>bool</font>
[GUIDisassemble](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUIDisassemble) | Get/Set the Disassemble icon visibility. | <font color=#4170a7>bool</font>
[GUIBuy](API/MSCLoader/HelperPlayMakerHelper/Variables/GUIBuy) | Get/Set the Buy icon visibility. | <font color=#4170a7>bool</font>
[GUIDrive](API/MSCLoader/HelperPlayMakerHelper/Variables/GUIDrive) | Get/Set the Drive icon visibility. | <font color=#4170a7>bool</font>
[GUIPassenger](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUIPassenger) | Get/Set the Passenger icon visibility. | <font color=#4170a7>bool</font>
[GUIInteraction](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUIInteraction) | Get/Set the Interaction text visibility and content, empty string hides it. | <font color=#4170a7>string</font>
[GUISubtitle](API/MSCLoader.Helper/PlayMakerHelper/Variables/GUISubtitle) | Get/Set the Subtitle text visibility and content, empty string hides it. | <font color=#4170a7>string</font>

### Extension Functions

Name | Description | Returns
---- | ----------- | -------
[GetPlayMakerFSM](API/MSCLoader.Helper/PlayMakerHelper/Functions/GetPlayMakerFSM.md) | Extension method for a [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) or [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html) to find a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) component by name. | [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079)
[GetState](API/MSCLoader.Helper/PlayMakerHelper/Functions/GetState.md) | Extension method for a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) component to find an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) by name or index. | [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099)
[GetAction](API/MSCLoader.Helper/PlayMakerHelper/Functions/GetAction.md)\<<font color="#aac397">T</font>\> | Get an [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) of type <font color="#aac397">T</font> by index from an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) or from a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) by state name or state index. | <font color="#aac397">T</font>
[InsertAction](API/MSCLoader.Helper/PlayMakerHelper/Functions/InsertAction.md) | Insert a new [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) into specified index into an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) or a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) by state name or state index. | <font color=#4170a7>void</font>
[AddAction](API/MSCLoader.Helper/PlayMakerHelper/Functions/AddAction.md) | Add a new [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) to an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) or a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) by state name or state index. | <font color=#4170a7>void</font>
[ReplaceAction](API/MSCLoader.Helper/PlayMakerHelper/Functions/ReplaceAction.md) | Replace an [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) at specified index with a new [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) in an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) or a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) by state name or state index. | <font color=#4170a7>void</font>
[RemoveAction](API/MSCLoader.Helper/PlayMakerHelper/Functions/RemoveAction.md) | Remove an [FSMStateAction](https://hutonggames.fogbugz.com/default.asp?W1100) at specified index from an [FSMState](https://hutonggames.fogbugz.com/default.asp?W1099) or a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) by state name or state index. | <font color=#4170a7>void</font>
[GetVariable](API/MSCLoader.Helper/PlayMakerHelper/Functions/GetVariable.md)\<<font color="#aac397">T</font>\> | Get a variable of type <font color="#aac397">T</font> by name from a [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079). | <font color="#aac397">T</font>
[FindVariable](API/MSCLoader.Helper/PlayMakerHelper/Functions/FindVariable.md)\<<font color="#aac397">T</font>\> | Get a variable of type <font color="#aac397">T</font> by name from a [FsmVariables](https://hutonggames.fogbugz.com/default.asp?W1103) container. | <font color="#aac397">T</font>
[Initialize](API/MSCLoader.Helper/PlayMakerHelper/Functions/Initialize.md) | Initialize a not yet enabled [PlayMakerFSM](https://hutonggames.fogbugz.com/default.asp?W1079) for editing. | <font color=#4170a7>void</font>

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[GetGlobalVariable](API/MSCLoader.Helper/PlayMakerHelper/Functions/GetGlobalVariable.md)\<<font color="#aac397">T</font>\> | Get a global variable of type <font color="#aac397">T</font> by name. | <font color="#aac397">T</font>

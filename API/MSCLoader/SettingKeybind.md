# SettingKeybind

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a keybind setting. With this you can modify your setting quite extensively. This will also be used to check if your keybind is pressed, up or down.

### Variables

Name | Description | Type
---- | ----------- | ----
[nameText](API/MSCLoader/SettingKeybind/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingKeybind/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[Enabled](API/MSCLoader/SettingKeybind/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingKeybind/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingKeybind/Variables/Name.md) | Get/Set the setting name, the text displayed beside the keybind. Upper-case recommended. | <font color=#4170a7>string</font>
[PreBind](API/MSCLoader/SettingKeybind/Variables/PreBind.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html) executed when the player initiates a rebind. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html)
[PostBind](API/MSCLoader/SettingKeybind/Variables/PostBind.md) | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html) executed when the player finishes a rebind. | [UnityEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/Events.UnityEvent.html)
[keybind](API/MSCLoader/SettingKeybind/Variables/keybind.md) | Current [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) of the main key. | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)
[modifiers](API/MSCLoader/SettingKeybind/Variables/modifiers.md) | Current [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[] array of the modifier key(s). | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[]
[defaultKeybind](API/MSCLoader/SettingKeybind/Variables/defaultKeybind.md) | Default [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html) of the main key. | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)
[defaultModifiers](API/MSCLoader/SettingKeybind/Variables/defaultModifiers.md) | Default [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[] array of the modifier key(s). | [KeyCode](https://docs.unity3d.com/500/Documentation/ScriptReference/KeyCode.html)[]

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[ReassignKey](API/MSCLoader/SettingKeybind/Functions/ReassignKey.md) | Starts the reassignment routine. | <font color=#4170a7>void</font>
[GetKey](API/MSCLoader/SettingKeybind/Functions/GetKey.md) | Get if the keybind is pressed down (including modifiers). | <font color=#4170a7>bool</font>
[GetKeyDown](API/MSCLoader/SettingKeybind/Functions/GetKeyDown.md) | Get if the keybind started being pressed down in the same frame (including modifiers). | <font color=#4170a7>bool</font>
[GetKeyUp](API/MSCLoader/SettingKeybind/Functions/GetKeyUp.md) | Get if the keybind is released in the same frame (including modifiers). | <font color=#4170a7>bool</font>
[GetModifiers](API/MSCLoader/SettingKeybind/Functions/GetModifiers.md) | Get if the modifiers are pressed down. | <font color=#4170a7>bool</font>
[ResetToDefaults](API/MSCLoader/SettingKeybind/Functions/ResetToDefaults.md) | Reset the setting to default values. | <font color=#4170a7>void</font>
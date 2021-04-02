# SettingButton

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [ModSetting](API/MSCLoader/ModSetting.md)*

### Description

Component controlling a button setting. With this you can modify your setting quite extensively. You have access to everything related to the setting; text, shadow, button and image components.

### Variables

Name | Description | Type
---- | ----------- | ----
[nameText](API/MSCLoader/SettingButton/Variables/nameText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the name text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[nameShadow](API/MSCLoader/SettingButton/Variables/nameShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the name text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[button](API/MSCLoader/SettingButton/Variables/button.md) | [Button](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Button.html) component. | [Button](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Button.html)
[buttonImage](API/MSCLoader/SettingButton/Variables/buttonImage.md) | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html) component for the button background. | [Image](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Image.html)
[buttonText](API/MSCLoader/SettingButton/Variables/buttonText.md) | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html) component for the button text. | [Text](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Text.html)
[buttonTextShadow](API/MSCLoader/SettingButton/Variables/buttonTextShadow.md) | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html) component for the button text shadow. | [Shadow](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Shadow.html)
[Enabled](API/MSCLoader/SettingButton/Variables/Enabled.md) | Get/Set if the setting should show up in the settings list or not. Gets/Sets the active state of the setting [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) as well. | <font color=#4170a7>bool</font>
[ID](API/MSCLoader/SettingButton/Variables/ID.md) | Get/Set the setting ID, the unique identifier, stored as the settings [GameObject](https://docs.unity3d.com/500/Documentation/ScriptReference/GameObject.html) name. | <font color=#4170a7>string</font>
[Name](API/MSCLoader/SettingButton/Variables/Name.md) | Get/Set the setting name, the text displayed beside the button, if empty the text is disabled and the button takes up the entire space. Upper-case recommended. | <font color=#4170a7>string</font>
[ButtonText](API/MSCLoader/SettingButton/Variables/ButtonText.md) | Get/Set the button text on the [buttonText](API/MSCLoader/SettingButton/Variables/buttonText.md) component. Upper-case recommended. | <font color=#4170a7>string</font>
[OnClick](API/MSCLoader/SettingButton/Variables/OnClick.md) | [ButtonClickEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Button.ButtonClickedEvent.html) for the button, holds all actions that will be executed on click. | [ButtonClickEvent](https://docs.unity3d.com/500/Documentation/ScriptReference/UI.Button.ButtonClickedEvent.html)
[suspendActions](API/MSCLoader/SettingButton/Variables/suspendActions.md) | If true no actions will be executed when clicking the button. | <font color=#4170a7>bool</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[AddAction](API/MSCLoader/SettingButton/Functions/AddAction.md) | Add an action to the button. | <font color=#4170a7>void</font>

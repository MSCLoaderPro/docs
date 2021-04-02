# ModSettings

*Namespace: [MSCLoader](API/MSCLoader.md) / Inherits from: [MonoBehaviour](https://docs.unity3d.com/500/Documentation/ScriptReference/MonoBehaviour.html)*

### Description

Controller class for the mod's settings window. It's used to control names, id text, description, adding settings as well as loading and saving settings.

Every [Mod](API/MSCLoader/Mod.md) class has their own [modSettings](API/MSCLoader/Mod/Variables/modSettings.md) variable that can be used to access their own instance of this component.

### Variables

Name | Description | Type
---- | ----------- | ----
[settingsList](API/MSCLoader/ModSettings/Variables/settingsList.md) | Parent transform for all settings. | [Transform](https://docs.unity3d.com/500/Documentation/ScriptReference/Transform.html)
[settings](API/MSCLoader/ModSettings/Variables/settings.md) | List of all settings related to the mod. | <font color=#3ca486>List</font><[ModSetting](API/MSCLoader/ModSetting.md)>
[loadedSettings](API/MSCLoader/ModSettings/Variables/loadedSettings.md) | Contains all the loaded settings from the mod's configuration JSON file. | [ModConfig](API/MSCLoader/ModConfig.md)
[Name](API/MSCLoader/ModSettings/Variables/Name.md) | Header text for the mod's setting window, automatically set to the mod's [Name](API/MSCLoader/Mod/Variables/Name.md). | <font color=#4170a7>string</font>
[ID](API/MSCLoader/ModSettings/Variables/ID.md) | Sub-Header text for the mod's setting window, automatically set to the mod's [ID](API/MSCLoader/Mod/Variables/ID.md). | <font color=#4170a7>string</font>
[Description](API/MSCLoader/ModSettings/Variables/Description.md) | Description text displayed in the mod's setting window, if empty the text header is hidden to not take up space, automatically set to the mod's [Description](API/MSCLoader/Mod/Variables/Description.md). | <font color=#4170a7>string</font>

### Public Functions

Name | Description | Returns
---- | ----------- | -------
[AddButton](API/MSCLoader/ModSettings/Functions/AddButton.md) | Add a button to the settings list. | <font color=#3ca486>SettingButton</font>
[AddHeader](API/MSCLoader/ModSettings/Functions/AddHeader.md) | Add a header to the settings list. | <font color=#3ca486>SettingHeader</font>
[AddKeybind](API/MSCLoader/ModSettings/Functions/AddKeybind.md) | Add a keybind to the settings list. | <font color=#3ca486>SettingKeybind</font>
[AddRadioButtons](API/MSCLoader/ModSettings/Functions/AddRadioButtons.md) | Add radio buttons to the settings list.| <font color=#3ca486>SettingRadioButtons</font>
[AddSlider](API/MSCLoader/ModSettings/Functions/AddSlider.md) | Add a slider to the settings list. | <font color=#3ca486>SettingSlider</font>
[AddSpacer](API/MSCLoader/ModSettings/Functions/AddSpacer.md) | Add a spacer to the settings list. | <font color=#3ca486>SettingSpacer</font>
[AddText](API/MSCLoader/ModSettings/Functions/AddText.md) | Add a text to the settings list. | <font color=#3ca486>SettingText</font>
[AddTextBox](API/MSCLoader/ModSettings/Functions/AddTextBox.md) | Add a text box to the settings list. | <font color=#3ca486>SettingTextBox</font>
[AddToggle](API/MSCLoader/ModSettings/Functions/AddToggle.md) | Add a toggle to the settings list. | <font color=#3ca486>SettingToggle</font>
[AddBoolean](API/MSCLoader/ModSettings/Functions/AddBoolean.md) | Add a hidden boolean to the settings list. | <font color=#3ca486>SettingBoolean</font>
[AddNumber](API/MSCLoader/ModSettings/Functions/AddNumber.md) | Add a hidden number to the settings list. | <font color=#3ca486>SettingNumber</font>
[AddString](API/MSCLoader/ModSettings/Functions/AddString.md) | Add a hidden string to the settings list. | <font color=#3ca486>SettingString</font>

### Example

```csharp

SettingToggle myToggle;
SettingSlider mySlider;
SettingKeybind myKeybind;

public override void ModSettings()
{
    modSettings.AddHeader("MY SPECIAL SETTINGS");
    myToggle = modSettings.AddToggle("myToggle", "MY TOGGLE", true);
    mySlider = modSettings.AddSlider("mySlider", "MY SLIDER", 5, 1, 10, (value) => { ModConsole.Log(value); });
    myKeybind = modSettings.AddKeybind("myKeybind", "MY KEYBIND", KeyCode.A, KeyCode.LeftControl);
}
```

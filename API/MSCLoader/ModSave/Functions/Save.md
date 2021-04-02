# [ModSave](API/MSCLoader/ModSave.md).Save

*public static void <b>Save</b>\<T\>(string <b>fileName</b>, T <b>data</b>, string <b>encryptionKey</b> = null);*

#### Description

Saves class <font color="#aac397">T</font> into a XML-file with optional encryption. Saves into the game's default save folder: *"%UserProfile%\Appdata\LocalLow\Amistech\My Summer Car"*.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
fileName | Name of the save file, can also include subfolders.  | <font color=#4170a7>string</font> | N/A
data | Path to the bundle you want to load. | <font color="#aac397">T</font> | N/A
encryptionKey | Optional encryption key for the save file. | <font color=#4170a7>string</font> | <font color=#4170a7>null</font>
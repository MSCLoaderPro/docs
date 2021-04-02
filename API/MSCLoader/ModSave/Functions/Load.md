# [ModSave](API/MSCLoader/ModSave.md).Load

*public static T <b>Load</b>\<T\>(string <b>fileName</b>, string <b>encryptionKey</b> = null);*

#### Description

Loads an XML-file and deserializes it into class <font color="#aac397">T</font> with optional decryption using provided encryption key.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
fileName | Name of the save file, can also include subfolders.  | <font color=#4170a7>string</font> | N/A
encryptionKey | Optional encryption key for the save file. | <font color=#4170a7>string</font> | <font color=#4170a7>null</font>
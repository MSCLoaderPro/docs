# ModSave

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

Class responsible for saving and loading save data for mods. Serializes a custom class <font color="#aac397">T</font> of serializable variables into an clean XML file for easy inspection. You can also encrypt your save files if you want, for example if you save some kind of sensitive data. It saves the file to the game's save folder *"%UserProfile%\Appdata\LocalLow\Amistech\My Summer Car"*, and you can save it into a subfolder if you want.  

In the custom class, you can assign its variables default values, that will be loaded in case the save file doesn't exist yet or if one or more variables in the class isn't present in the found save file.

To save lists, convert them into an array first. If you're unsure if a certain Type or class can't be serialized, give it a try and see what happens!

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[Save](API/MSCLoader/ModSave/Functions/Save.md) | Saves a custom serializable class <font color="#aac397">T</font> into a file of specified name (and optional subfolder) with optional encryption key. | <font color=#4170a7>void</font>
[Load](API/MSCLoader/ModSave/Functions/Load.md) | Loads a file of specified name (and optional subfolder) a deserializes it into a custom class <font color="#aac397">T</font> with optional (or mandatory if the file was saved with encryption) encryption key. | <font color="#aac397">T</font>
[Delete](API/MSCLoader/ModSave/Functions/Delete.md) | Delete an XML save file of specified name (and optional subfolder). | <font color=#4170a7>void</font>

### Example

```csharp
public class SaveData
{
    public bool mySavedBool = false;
    public string mySavedString = "I Babu Frik";
    public int[] mySavedIntegerArray = { 1, 0, 1, 0, 2 };
    public Vector3 myVector = new Vector3(0, 1, 0);
}

public override void OnNewGame() 
{
    ModSave.Delete("mySaveFile");
}

public override void OnLoad()
{
    SaveData loadedSave = ModSave.Load<SaveData>("mySaveFile");

    ModConsole.Log(loadedSave.mySavedString);
    // Console output with no save file: I Babu Frik
    // Console output with save file: HEYY HEEEEEEY!!
}

public override void OnSave()
{
    List<int> myNewIntegerList = new List<int> { 1, 0, 22, 1, 13, 1455, 1421};
    ModSave.Save("mySaveFile", new SaveData
    {
        mySavedBool = true,
        mySavedString = "HEYY HEEEEEEY!!",
        mySavedIntegerArray = myNewIntegerList.ToArray(),
        myVector = new Vector3(1, 2, 3)
    });
}
```
This will create a save file like so:
```xml
<SaveData>
    <mySavedBool>true</mySavedBool>
    <mySavedString>HEYY HEEEEEEY!!</mySavedString>
    <mySavedIntegerArray>
        <int>1</int>
        <int>0</int>
        <int>22</int>
        <int>1</int>
        <int>13</int>
        <int>1455</int>
        <int>1421</int>
    </mySavedIntegerArray>
    <myVector>
        <x>1</x>
        <y>2</y>
        <z>3</z>
    </myVector>
</SaveData>
```
# Porting existing mods

While the old Mod Loader mods work fine, porting to Mod Loader Pro offers an extended functionality - such as more advanced settings, native PartMagnet system, easy way to add parts, items and more.

## Changing MSCLoader reference

First of for most, you must change the MSCLoader reference you use. If you already [updated from the MSCLoader](UpdateFromMSCLoader.md), it is already been done - you can skip this part.

If not, on the **Reference** view in **Solution Explorer**, **right-click on "MSCLoader"** and from drop-down menu, press "**Delete**". Then, simply right-click on **References**, and add Mod Loader Pro. You may want to refer to <a href="#/ForCreators/CreatingANewMod?id=adding-nescesary-references" target="_blank">this guide</a>.

While mod will compile as-is and should run without a problem (unless you, ex. are changing MSCLoader gameobjects), it is highly recommended to change following things:

## Settings > modSettings

First it is recommended to switch to the newer settings method. A new modSettings system is much more versatile, faster and less resource intensive while reading the values.

Here's an example of an old way of creating and then writing a boolean type of setting:

```csharp
static Settings myToggle = new Settings("myToggle", "My Toggle", false);

public override void ModSettings()
{
    Settings.AddCheckBox(this, myToggle);
}

/* ... */

void CheckMyToggle()
{
    bool isToggleOn = (bool)myToggle.GetValue()
    ModConsole.Print("myToggle Value: " + isToggleOn);
}
```

A new method of doing the same thing is the following:

```csharp
static SettingToggle myToggle;

public override void ModSettings()
{
    myToggle = modSettings.AddToggle("myToggle", "My Toggle", false);
}

/* ... */

void CheckMyToggle()
{
    bool isToggleOn = myToggle.Value;
    ModConsole.Print("myToggle Value: " + isToggleOn);
}
```

Not only it is much easier to set up a new setting, it is also easier to read the value (as there is no casting of variables required), and allows to change the name, which can be done using:

```csharp
myToggle.name = "A new name of the toggle";
```

You can modify, the variable without any hacky ways that were previously required.

If you want to learn more about new mod settings and what you can do with them, see [ModSettings documentation](/API/MSCLoader/ModSettings.md).

## ModUI > ModPrompt

With the ModUI being fazed out from Mod Loader Pro, there are two changes that come with that:

### Prompts and message boxes

ModPrompt is a new way of creating and managing the prompts (message boxes). It offers a wider range of customizability - from simple "OK" message, to fully customized ones.

Here's an example of old "OK" and "Yes No" prompts:

```csharp
ModUI.ShowMessage("This is a simple prompt.", "OK Prompt");

ModUI.ShowYesNoMessage("This is a question prompt", "Yes No Prompt", MyAction);
```

And here's an example of the new method:

```csharp
ModPrompt.CreatePrompt("This is a simple prompt.", "OK Prompt");

ModPrompt.CreateYesNoPrompt("This is a question prompt", "Yes No Prompt", () => MyAction());
```

While at first there is not much that changed, a new method lets you keep the prompt as a value, so you can store it when you want to reuse the same prompt, or you can add an action when the prompt is closed.

For more, see [ModPrompt documentation](/API/MSCLoader/ModPrompt.md).

### Mod Canvas

If you want to acces the Mod Loader canvas, you may notice that it is obsolete. If you want to get the Mod Loader canvas, use the following method:

```csharp
GameObject canvas = ModLoader.UICanvas;
````

## Console

Mod Loader Pro also makes some minor changes to how the mod console interaction. The main change is in the function naming. Previously, if you wanted to print a new line in console, you would use:

```csharp
ModConsole.Print("Normal messsage.");
ModConsole.Error("Error message.");
ModConsole.Warning("Warning message.");
```

Now the correct method is as follows:

```csharp
ModConsole.Log("Normal messsage.");
ModConsole.LogError("Error message.");
ModConsole.LogWarning("Warning message.");
```

If you want to learn more about console, see [console documentation](/API/MSCLoader/ModConsole.md).

## SaveLoad > ModSave

ModSave is a new way of saving and loading save files for MSC mods. Compared to the legacy SaveLoad system, [ModSave](/API/MSCLoader/ModSave.md) saves are cleaner and take up to 3x less space. ModSave is ALWAYS saved into the save file folder of My Summer Car.

If you already have implemented a new save system, you don't have to change the class that's being serialized into XML file. What you must do is to change the save file path - the only thing that you have to do is to remove the `Application.persistantDataPath` from the **fileName** variable.

So for example, this was the previous method of saving class data:

```csharp
SaveLoad.SerializesaveFile<MySaveClass>(this, mySaveClass, Application.persistentDataPath + "/MySaveName.xml");
```

The new way is as follows:

```csharp
// This will create a file called "MySaveName.xml" in the My Summer Car save folder.
ModSave.Save("MySaveName", mySaveClass);
```

And for loading, previous way of loading save file was as follows:

```csharp
MySaveClass mySaveClass = SaveLoad.DeserializeSaveLoad<MySaveClass>(this, Application.persistentDataPath + "/MySaveName.xml");
```

And this is the way it should be done with the new method:

```csharp
MySaveClass mySaveClass = ModSave.Load<MySaveClass>("MySaveName");
```
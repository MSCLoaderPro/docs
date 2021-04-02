# Creating a new mod

After you're done with [preparing environment](ForCreators/PreparingEnvironment.md), you can start creating your first mod.

## Creating the project

In order to create a Mod Loader Pro mod project, start Microsoft Visual Studio 2019, then click "Create a new project", and then search for "MSC Mod Loader Pro Mod" template.

![tut_1](/CreatingANewMod/1.png)
![tut_2](/CreatingANewMod/2.png)

Next you will be asked to name your mod and select where the project folder will be located. After you're done, click "Create".

![tut_3](/CreatingANewMod/3.png)

## Adding nescesary references

After a short while, you should load into Visual Studio IDE. First thing you must do, is to add references to MSC Mod Loader Pro and Unity Engine. In order to do that, on the right side of the Visual Studio window, find **Solution Explorer**, then right-click "**References**" and then "**Add Reference...**".

![tut_4](/CreatingANewMod/4.png)

A "**Reference Manager**" window should appear, where you want to click "**Browse...**".

![tut_5](/CreatingANewMod/5.png)

Navigate to **My Summer Car** folder, then **mysummercar_Data :arrow_right: Managed**.

From here, you must select:

- ***MSCLoader.dll***
- ***UnityEngine.dll***

Additionally, you may want, but you don't have to import following references:

- *PlayMaker.dll*
- *UnityEngine.UI.dll*

!> Make sure you imported a Mod Loader Pro assembly, you can check that by selecting the imported MSCLoader.dll ported and checking the assembly info.<br>![note](/CreatingANewMod/note.png)

## Optional quality of life stuff

You can also set up Visual Studio so it will automatically move the assembly to Mods folder. In order to do that, double-click on "**Properties**", then go to "Build Events". In "**Post-build event command line**". In here, paste the following command, where "**path to mods folder**" is replaced with your path fo mods folder (so ex. **C:\Steam\steamapps\common\My Summer Car\Mods**).

```batch
if "$(ConfigurationName)" == "Debug" (
    copy "$(TargetPath)" "path to mods folder" /y
    copy "$(TargetDir)$(TargetName).pdb" "path to mods folder\$(TargetName).pdb" /y
    cd "path to mods folder"
    call "path to mods folder\debug.bat"
) ELSE (
    copy "$(TargetPath)" "path to mods folder" /y
)
```

Next in the "**Debug**" tab, in "**Start action**" section, select "**Start external program**", and there select **mysummercar.exe** executable.

## Compiling the mod

You can finally start coding your mod. Following example of a mod will create a simple "Hello, World!" prompt when main menu loads.

```csharp
using MSCLoader;

namespace MyMod1
{
    public class MyMod1 : Mod
    {
        public override string ID => "MyMod1";
        public override string Name => "My Awesome Mod";
        public override string Author => "YOU";
        public override string Version => "1.0";
        public override string Description => "THIS IS MY AWESOME MOD!";

        public override void OnLoad()
        {
            if (ModLoader.CurrentScene == CurrentScene.MainMenu)
            {
                ModPrompt.CreatePrompt("Hello, world!", "This is my message");
            }
        }
    }
}
```

And this is the result :)

![tut_6](/CreatingANewMod/6.png)

And that's how the mod looks like in the mod settings:

![tut_7](/CreatingANewMod/7.png)
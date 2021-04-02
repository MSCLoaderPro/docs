# Cross-platform mods

While MSCLoaders mods do work on Mod Loader Pro, it's not the case the other way around. There are two ways of making mod cross-compatible with both mod loaders at the same time.

First method focuses on making a single assembly, while the second one consits of two separate assemblies for each mod loader.

## Guides

<!-- tabs:start -->

#### ** Single Assembly **

Single assembly method limits you to only using functions and features supported by the stock MSCLoader - including save managing, asset loading, etc.

#### Pros

- Easier mod distribution, as only single mod assembly has to be distributed
- 1:1 same code, meaning less work requird to maintain both versions
- Easiest method, as practically no changes to the code are nescesarry

#### Cons

- You cannot utilize advanced features of Mod Loader Pro, such as improved mod settings system
- Mod Loader Pro: In the mod settings, "checkbox group" is not functioning correctly (other checkboxes aren't automatically deselected)
- Mod Loader Pro: Mod cannot have an icon, nor description

This method doesn't require any additional setup or configuration, you only must remember that elements such as (but not limited to)...

- Mod.Description
- Mod.Icon
- Mod.UpdateLink
- ModSave
- MSCLoader.Helper
- MSCLoader.PartMagnet
- MSCLoader.MSCCar
- MSCLoader.Paint
- ModPrompt

...and others will not work under MSCLoader, and will be recognized as "not My Summer Car mod".

It is of course recommended to test your compiled under MSCLoader, as well as Mod Loader Pro, although mod that works under MSCLoader should also work under Mod Loader Pro without any much problems.

#### ** Dual Assembly**

Dual assembly method requires user to set up the Visual Studio project, but after that, it's just the matter of switching between compiling methods.

#### Pros

- Mod can take full advantage of Mod Loader Pro features and functions
- Mod can have an icon and description in Mod Loader Pro settings
- Auto update support via NexusMods or GitHub

#### Cons

- Two assemblies for MSCLoader and Mod Loader Pro need to be distributed
- Parts of the code must be maintained separately
- User must install correct version of the mod himself

This involves using [preprocessor directives](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/preprocessor-directives/). You may know of existance of directives such as `#if DEBUG`. We will be using the combination of that, and of [solution configurations](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-configuration).

### Setting up the solution

First you must create a new configuration. In order todo that, right where you select Debug/Release compiling methods, drop down the menu and click "**Configuration Manager...**"

![tut_1](/CrossPlatformMods/Media/1.png)

This will open **Configuration Manager** window. Under **Active solution configuration**, click a drop down list and select **<New...>**.

![tut_2](/CrossPlatformMods/Media/2.png)

For now, we will make a configuration for **debugging**. Name your configuration (for instance, "*Pro Debug*"), and under **Copy settings from**, choose **Debug**. Make sure that **Create new project configurations** is selected. You can press **OK**.

![tut_3](/CrossPlatformMods/Media/3.png)

Configuration Manager should look something like this:

![tut_4](/CrossPlatformMods/Media/4.png)

Next up, in the **Solution Explorer**, double-click on **Properties**.

![tut_5](/CrossPlatformMods/Media/5.png)

Go into **Build** tab. In **General** section, find **conditional compilation symbols**: type "***PRO***".

![tut_6](/CrossPlatformMods/Media/6.png)

?> If you want to make a **release** version, follow the same steps above, but under **copy settings from**, choose **Release**.

### Usage

If everything has been configured correctly, you can finally use the directives. A below example will show a Mod Loader Pro and MSCLoader version of the settings.

```csharp
#if PRO
    // This is a Mod Loader Pro settings.
    SettingToggle myToggle;
    public static override ModSettings()
    {
        myToggle = modSettings.AddToggle("myToggle", "My Toggle", false);
    }
#else
    // This is a MSCLoader settings.
    Settings myToggle = new Settings("myToggle", "My Toggle", false);
    public static override ModSettings()
    {
        Settings.AddCheckBox(this, myToggle);
    }
#endif
```

If **Pro Debug** configuration is selected, only the code between `#if PRO` and `#else` will be compiled for that assembly, the grayed-out part will be skipped, and the code in IDE will look like this:

![tut_7](/CrossPlatformMods/Media/7.png)

And if **Debug** or **Release** is selected, only code between `#else` and `#endif` will be compiled, the grayed-out part will be skipped, and the code will look like this:

![tut_8](/CrossPlatformMods/Media/8.png)

If, for example, you want to compile a bit only for Mod Loader Pro, but without an alternative in MSCLoader, you can do following thing:

```csharp
#if PRO
    ModConsole.Log("This text is only displayed in Mod Loader Pro build.");
#endif
```

Compiling from both configurations will produce a separate assemblies. There is no real way to distinguish those assemblies, but what we can recommend is naming the build for Mod Loader Pro by adding "**.pro**" between file name and its extensions. For example: `MyMod.pro.dll`.

<!-- tabs:end -->
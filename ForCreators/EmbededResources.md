# *Embeded Resources* #

# locating/making a resources file

Adding a resource to your project is one of the easiest processes in modding.

if you want to add a resource follow these simple steps:

1. click on `Project` in the header of Visual Studio and then click on `'YourModName' Properties`.

![tut_1](/EmbededResources/Media/1.png)

2. a tab should have opened and should look like this.

![tut_2](/EmbededResources/Media/2.png)

3. click on `Resources`, you should see this now.

![tut_3](/EmbededResources/Media/3.png)

4. if you don't see that but see this, click on  `This project does not contain a default resources file. Click here to create one.`

![tut_4](/EmbededResources/Media/4.png)

# Adding a resource

`NOTICE: this doesn't fully apply to adding Mod Icons!`
[Adding mod icon](ForCreators/EmbededResources.md?id=adding-mod-icon)

1. click on the arrow left to `Add Resource` you should see this.

![tut_5](/EmbededResources/Media/5.png)

2. click on `Add Existing File...` a file explorer window should have opened, now find your resource on your computer and select it. then click on `Open when you found it.`

# Adding mod icon

Adding an icon to the mod is a very simple and fast process. It involves simply adding an image file into Resources of the assembly. unfortunately, due to System.Image library limitations built into Unity3D, an image extension has to be removed.

You need an image in **PNG** format in the **1:1** ratio. The recommended resolution is **56x56** pixels. Name it something simple (for example, **icon.png**).

If you have one, it should look in File Explorer like this:

![tut_6](/AddingModIcon/Media/1.png)

In the same explorer location your icon is located, click on the address bar and type `cmd` and press `Enter`.

![tut_7](/AddingModIcon/Media/2.png)

In the new console window, type the following command and press `Enter` to confirm:

```batch
rename "icon.png" "icon"
```

![tut_8](/AddingModIcon/Media/3.png)

You can close the window. You will notice that the icon now looks like this:

![tut_9](/AddingModIcon/Media/4.png)

This is perfectly normal.

Now, open your mod project in Visual Studio and in **Solution Explorer**, double-click on **Properties**. Here, go to **Resources** tab. You should have an empty table right in front of you. If the resources file is missing, create one.

In here, at the top of Resources view, click a small arrow next to **Add Resources**, and select **Add Existing File...**. From there, select your **icon** file.

![tut_10](/AddingModIcon/Media/5.png)

![tut_11](/AddingModIcon/Media/6.png)

Your file should be visible in Resources browser:

![tut_12](/AddingModIcon/Media/7.png)

Now go into your main Mod class and add a below line of code:

```csharp
public override byte[] Icon => Properties.Resources.icon;
```

![tut_13](/AddingModIcon/Media/8.png)

And this is how the icon looks like in the mod settings:

![tut_14](/AddingModIcon/Media/9.png)

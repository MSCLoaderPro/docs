# Adding mod icon

Adding an icon to the mod is a very simple and fast process. It involves simply adding an image file into Resources of the assembly. unfortunately, due to System.Image library limitations built into Unity3D, an image extension has to be removed.

You need an image in **PNG** format in the **1:1** ratio. The recommended resolution is **56x56** pixels. Name it something simple (for example, **icon.png**).

If you have one, it should look in File Explorer like this:

![tut_1](/AddingModIcon/Media/1.png)

In the same explorer location your icon is located, click on the address bar and type `cmd` and press `Enter`.

![tut_2](/AddingModIcon/Media/2.png)

In the new console window, type the following command and press `Enter` to confirm:

```batch
rename "icon.png" "icon"
```

![tut_3](/AddingModIcon/Media/3.png)

You can close the window. You will notice that the icon now looks like this:

![tut_4](/AddingModIcon/Media/4.png)

This is perfectly normal.

Now, open your mod project in Visual Studio and in **Solution Explorer**, double-click on **Properties**. Here, go to **Resources** tab. You should have an empty table right in front of you. If the resources file is missing, create one.

In here, at the top of Resources view, click a small arrow next to **Add Resources**, and select **Add Existing File...**. From there, select your **icon** file.

![tut_5](/AddingModIcon/Media/5.png)

![tut_6](/AddingModIcon/Media/6.png)

Your file should be visible in Resources browser:

![tut_7](/AddingModIcon/Media/7.png)

Now go into your main Mod class and add a below line of code:

```csharp
public override byte[] Icon => Properties.Resources.icon;
```

![tut_8](/AddingModIcon/Media/8.png)

And this is how the icon looks like in the mod settings:

![tut_9](/AddingModIcon/Media/9.png)

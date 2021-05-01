# Mod Auto-Updates

Mod Loader Pro can automatically check and download available updates. It is up to modder to add one - either via **NexusMods**, or **GitHub**. Modder's only task is to add a link to the update page of his mod.

## NexusMods or GitHub

Unfortunately, due to **NexusMods** policy, only premium NexusMods members can have automatic update downloading of installed mods. That means, if one doesn't have premium on NexusMods, he/she will only be notified about the available update, and will be asked if he/she wants to open a NexusMods page of your mod.

**GitHub** on the other hand is much liberal and allows anyone to access their API. The only downside for the modder is that he must make a new repository for his mod - **YOUR MOD DOES NOT HAVE TO BE OPEN-SOURCE!**

## Preparing the download source

<!-- tabs:start -->

#### **NexusMods**

If you plan on using NexusMods, you first must create a new mod page. Go to [My Summer Car page for NexusMods](https://www.nexusmods.com/mysummercar/) and after you log-in, click "**Upload**" and then "**Upload mod**".

![tut_1](/ModAutoUpdates/Media/1.png)

You don't have to publish the mod yet, nor add the files. On the last page hit "**View mod page**". You should land on a mod page site. Copy it's URL, it should look something like `https://www.nexusmods.com/mysummercar/mods/xxx`.

#### **GitHub**

If you want to use [GitHub](https://github.com/), log-in into your GitHub account. Now, depending on your choice, you may follow two separate guides:

#### Open-Source projects

If your projects is open-source, you probably already have a project available on your GitHub. Go into your project's repository and copy it's URL, which should look something like this: `https://github.com/YourName/ProjectName`.

#### Closed-Source projects

If you don't want to publish the source code of your mod, on your GitHub main page, in the top right corner, click the "**+**", and then choose "**New repository**" from the list.

![tut_2](/ModAutoUpdates/Media/2.png)

Name your repository and press **Create repository**.

![tut_3](/ModAutoUpdates/Media/3.png)

!> Remember to make the repository **Public**, when you're about to release the mod.

You should be automatically redirected to that repository page. Copy it's URL. It should look like this: `https://github.com/YourName/ProjectName`.

<!-- tabs:end -->

## Adding update link to your mod

If you finally have your link, go into your mod project, and add the following line:

```csharp
public static override string UpdateLink => "your link"
```

Examples:

```csharp
public static override string UpdateLink => "https://www.nexusmods.com/mysummercar/mods/xxx"; // NexusMods.
public static override string UpdateLink => "https://github.com/YourName/repo_name"; // GitHub.
```

!> Mod Loader Pro may throw a warning that your mod's UpdateLink is incorrect, if you haven't published the mod yet, or no releases are available. This is normal and should be expected, until your mod page is set to public.

## Versioning

Mod Loader Pro reads your <a href="/API/MSCLoader/Mod/Variables/Version" target="_blank">Version</a> string and, in case of NexusMods, it reads **latest_version** tag, and in case of GitHub: **tag_name** - in both cases it assumes these follow [semantic versioning format](https://semver.org):

```Major.Minor.Patch```

Mod verison **HAS TO HAVE** *Major* and *Minor* numbers, while *Patch* is optional.

Here are some examples:

```csharp
public static override string Version => "1.0"; // First release of a mod.
public static override string Version => "1.0.0"; // Recognized as the same version as the one above.
public static override string Version => "1.0.1"; // A patch for the version 1.0.
public static override string Version => "0.5";
public static override string Version => "2021.3.19";
```

## Releasing updates

Please pack a mod into **.ZIP** archive, as if you would want to drag-and-drop it into Mods folder. So for example:

* MyMod.zip
    * Assets
        * MyMod
            * MyAssets.assetbundle
    * MyMod.dll

!> If you plan to publish two versions of a mod - one for MSCLoader and one for Mod Loader Pro, please add before the .ZIP extionsion a "**.Pro**" in the file name. This will tell Mod Loader Pro to only download that file, and ignore another one. For example: `MyMod.Pro.zip`.

<!-- tabs:start -->

#### **NexusMods**

On the mod management page, go into **Manage files**.

Fill out the file info. Here's an example of how it could look like:

![tut_4](/ModAutoUpdates/Media/4.png)

!> Make sure the "**File version**" is **EXACT THE SAME** as your **Version string**! Do not add any any dashes, underscores or anything else!

!> Remember to check "**This is the latest version of the mod (your main version will be updated automatically)**" and "**This is a new version of an existing file (optional)**".

Then you can add your file and save everything - that's all! Your mod update is out!

#### **GitHub**

Go to your mod repository. On the right, find **Releases** widget and press it's header.

![tut_5](/ModAutoUpdates/Media/5.png)

Then on the right find the **"Draft a new release"** button.

![tut_6](/ModAutoUpdates/Media/6.png)

In the **"tag version"**, write your file version: it **MUST** be the same as the version in **Version string**. So for a mod update version `1.1`, you could fill out the info like this:

![tut_7](/ModAutoUpdates/Media/7.png)

Don't forget to attach your **.ZIP** archive and hit "**Publish release**"!

?> Note: Files tagged as "**This is a pre-release**" won't be checked by Mod Loader Pro.

<!-- tabs:end -->

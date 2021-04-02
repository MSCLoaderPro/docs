# [ModAssets](API/MSCLoader/ModAssets.md).LoadBundle

*public static [AssetBundle](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html) <b>LoadBundle</b>(byte[] <b>bundleBytes</b>);*  
*public static [AssetBundle](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html) <b>LoadBundle</b>(string <b>filePath</b>);*  
*public static [AssetBundle](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html) <b>LoadBundle</b>([Mod](API/MSCLoader/Mod.md) <b>mod</b>, string <b>bundleName</b>);*  

#### Description

Loads a bundle into memory, use to load your assets and then unload it.

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
bundleBytes | Array of bytes for the assetbundle.  | <font color=#4170a7>byte</font>[] | N/A
filePath | Path to the bundle you want to load. | <font color=#4170a7>string</font> | N/A
mod | [Mod](API/MSCLoader/Mod.md) which Asset folder you want to load a bundle from. | [Mod](API/MSCLoader/Mod.md) | N/A
bundleName | Name of the bundle you want to load. | <font color=#4170a7>string</font> | N/A

#### Example

```csharp
public override void OnLoad()
{
    AssetBundle bundle = ModAssets.LoadBundle(Properties.Resources.myBundle)
    // Loads a bundle in the assembly's resources.
    GameObject myObject = bundle.LoadAsset<GameObject>("myObject.prefab");
    bundle.Unload(false);
}
```
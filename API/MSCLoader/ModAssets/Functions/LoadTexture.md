# [ModAssets](API/MSCLoader/ModAssets.md).LoadTexture

*public static [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html) <b>LoadTexture</b>(string <b>path</b>, bool <b>normalMap</b> = false);*  
*public static [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html) <b>LoadTexture</b>([Mod](API/MSCLoader/Mod.md) mod, string <b>textureName</b>, bool <b>normalMap</b> = false);*  

#### Description

Loads a texture into memory. 

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
filePath | Path to the texture you want to load. | <font color=#4170a7>string</font> | N/A
mod | [Mod](API/MSCLoader/Mod.md) which asset folder you want to load a texture from. | [Mod](API/MSCLoader/Mod.md) | N/A
textureName | Name of the texture you want to load (with extension). | <font color=#4170a7>string</font> | N/A
normalMap | Set if the texture is a normal map or not.  | <font color=#4170a7>bool</font> | false

#### Example

```csharp
public override void OnLoad()
{
    Texture2D myTexture = ModAssets.LoadTexture(this, "myTexture", false);
}
```
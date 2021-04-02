# ModAssets

*Namespace: [MSCLoader](API/MSCLoader.md)*

### Description

Class responsible for asset loading. There's methods for loading [AssetBundles](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html), [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html) (png, jpg, tga, dds), convert textures to normal maps and also [Mesh](https://docs.unity3d.com/500/Documentation/ScriptReference/Mesh.html) loading (obj).

### Static Functions

Name | Description | Returns
---- | ----------- | -------
[LoadBundle](API/MSCLoader/ModAssets/Functions/LoadBundle.md) | Loads an [AssetBundle](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html) into memory from either a byte array, file path or by name from a [Mod](API/MSCLoader/Mod.md) asset folder. | [AssetBundle](https://docs.unity3d.com/500/Documentation/ScriptReference/AssetBundle.html)
[LoadTexture](API/MSCLoader/ModAssets/Functions/LoadTexture.md) | Loads a [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html) into memory from a file path. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[LoadTexturePNG](API/MSCLoader/ModAssets/Functions/LoadTexturePNG.md) | Loads a PNG into memory from a file path. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[LoadTextureJPG](API/MSCLoader/ModAssets/Functions/LoadTextureJPG.md) | Loads a JPG into memory from a file path. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[LoadTextureDDS](API/MSCLoader/ModAssets/Functions/LoadTextureTGA.md) | Loads a DDS (DXT1 or DXT5) into memory from a file path. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[LoadTextureTGA](API/MSCLoader/ModAssets/Functions/LoadTextureTGA.md) | Loads a TGA into memory from a file path. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[ConvertToNormalMap](API/MSCLoader/ModAssets/Functions/ConvertToNormalMap.md) | Converts a [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html) into a Unity normal map. | [Texture2D](https://docs.unity3d.com/500/Documentation/ScriptReference/Texture2D.html)
[LoadMeshOBJ](API/MSCLoader/ModAssets/Functions/LoadMeshOBJ.md) | Loads a obj file into memory from a specified path. | [Mesh](https://docs.unity3d.com/500/Documentation/ScriptReference/Mesh.html)

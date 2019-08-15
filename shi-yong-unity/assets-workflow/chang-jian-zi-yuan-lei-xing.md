# Common types of Assets

## Image files

Unity supports most common image file types, such as BMP, TIF, TGA, JPG, and PSD. If you save your layered Photoshop \(.psd\) files into your Assets folder, Unity imports them as flattened images. You can find out more about[importing images with alpha channels from photoshop](https://docs.unity3d.com/2019.2/Documentation/Manual/HOWTO-alphamaps.html), or[importing your images as sprites](https://docs.unity3d.com/2019.2/Documentation/Manual/SpriteEditor.html)

## FBX and Model files

Since Unity supports the FBX file format, you can import data from any 3D modeling software that supports FBX. Unity also natively supports importing SketchUp files. For information on how to get the best results when exporting your FBX files from your 3D modeling software, see[Optimizing FBX files](https://docs.unity3d.com/2019.2/Documentation/Manual/HOWTO-importObject.html).

**Note:**You can also save your 3D files from most common 3D modeling software in their native format \(for example, .max, .blend, .mb, .ma\). When Unity finds them in your Assets folder, it imports them by calling back to your 3D modeling software’s FBX export**plug-in**  
. However, it is recommended to export them as FBX

## Meshes and animations

Whichever 3D modeling software you are using, Unity imports the Meshes and animations from each file. For a list of 3D modeling software that Unity supports, see[Model file formats](https://docs.unity3d.com/2019.2/Documentation/Manual/3D-formats.html).

Your**Mesh**  
file does not need to have an animation to be imported. If you do use animations, you can import all animations from a single file, or import separate files, each with a single animation. For more information about importing animations, see[Model import workflows](https://docs.unity3d.com/2019.2/Documentation/Manual/ImportingModelFiles.html).

## Audio files

If you save uncompressed audio files into your Assets folder, Unity imports them according to the**compression**  
  
  
settings specified. Read more about[importing audio files](https://docs.unity3d.com/2019.2/Documentation/Manual/AudioFiles.html).

## Other Asset types

In all cases, your original source file is never modified by Unity, even though within Unity you can often choose between various ways to compress, modify, or otherwise process the Asset. The import process reads your source file, and creates a game-ready representation of your Asset internally, matching your chosen import settings. If you modify the import settings for an Asset, or make a change to the source file in the Asset folder, that causes Unity to re-import the Asset again to reflect your changes.

**Note**: Importing native 3D formats requires that the 3D modeling software be installed on the same computer as Unity. This is because Unity uses the 3D modeling software’s FBX Exporter plug-in to read the file. Alternatively, you can directly export as FBX from your application and save into the Projects folder.



## Standard Assets

Unity ships with multiple**Standard Assets**  
. These are collections of Assets that most Unity customers use. These include: 2D,**Cameras**  
, Characters, CrossPlatformInput, Effects, Environment, ParticleSystems, Prototyping, Utility, and Vehicles.

To transfer**Standard Assets**in and out of Projects, Unity uses**Asset packages**  
, available on the Unity**Asset Store**  
. Asset packages allow you to share and re-use Unity Projects and collections of Assets.

**NOTE:**If you chose not to install Standard Assets when you installed Unity, you can[download them](https://docs.unity3d.com/2019.2/Documentation/Manual/AssetPackages.html#Standard)from the[Asset Store](https://assetstore.unity.com/packages/essentials/asset-packs/standard-assets-32351).

## Assets in the Unity Package Manager

You can install a wide range of Assets, including plug-ins, tools, and libraries directly into Unity through the**Unity Package Manager \(UPM\)**. These are a new type of package, and are available through the[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html). For more information about packages in general, see the[Packages](https://docs.unity3d.com/2019.2/Documentation/Manual/Packages.html)  
documentation.

---

* 2018–04–11 Page amended with limited
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




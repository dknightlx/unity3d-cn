# Accessing package Assets

This section explains how to access or refer to Assets that are defined inside a package:

* [Referring to package paths](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-assets.html#Paths)
* [Loading a Texture inside a package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-assets.html#Textures)
* [Resolving absolute paths](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-assets.html#GetFullPath)



## Referring to package paths

To refer to Assets that are defined inside a package, use this path scheme:

```
"Packages/
<
package-name
>
/..."

```

The path of the Asset inside a package begins with`Packages/`and the package[name](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#name)\(not the \[display name\]\(upm-manifestPkg.html\#display name\)\).

By contrast, you access Project Assets using this scheme:

```
"Assets/..."

```

For example, the path for the file image.png in the package subfolder`/Example/Images`of the**com.unity.images-library**package is:

```
"Packages/com.unity.images-library/Example/Images/image.png"

```



## Loading a Texture inside a package

To load a Texture stored inside a package, use the[LoadAssetAtPath](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/AssetDatabase.LoadAssetAtPath.html)method and specify the path following the`Packages/<package-name>/`path scheme as demonstrated in this example:

```
Texture2D texture = (Texture2D)AssetDatabase.LoadAssetAtPath("Packages/com.unity.images-library/Example/Images/image.png", typeof(Texture2D));

```



## Resolving absolute paths

To get the absolute path of a packaged Asset, use the[Path.GetFullPath\(\)](https://docs.microsoft.com/en-us/dotnet/api/system.io.path.getfullpath?view=netframework-4.7.2)method. For example:

```
string absolute =   Path.GetFullPath("Packages/com.unity.images-library/Example/Images/image.png");

```

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




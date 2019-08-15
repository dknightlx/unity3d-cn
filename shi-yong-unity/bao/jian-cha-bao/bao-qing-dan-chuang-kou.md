# Package Manifest window

When you click on the**package manifest**  
file in the**Project view**  
, the**Package Manifest**window opens:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/class-PackageManifestImporter.png "Inspecting a package manifest in the Editor")

Inspecting a package manifest in the Editor

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterA.png "A")Click the**Open**button to load this package manifest in your default code editor, such as Visual Studio. Click the**View in Package Manager**button to open the**Packages**window and load this package in the[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html).

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterB.png "B")The[Information](https://docs.unity3d.com/2019.2/Documentation/Manual/class-PackageManifestImporter.html#Info)section contains details about this specific package version.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterC.png "C")Use the**Brief Description**text box to specify the text that you want to appear in the[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html)of the**Packages**window. For more information, see the documentation for the[description](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#description)attribute.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterD.png "D")Use the[Dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/class-PackageManifestImporter.html#Depend)section to manage the list of packages that this package depends on.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterE.png "E")Click the**Revert**button to discard any changes you’ve made to the manifest. Click the**Apply**button to save any changes you’ve made to the manifest.



## Information

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/class-PackageManifestImporter-Info.png "Information section")

Information section

| **Property** | **Description** |
| :--- | :--- |
| **Name** | The official Unity name for this package. For more information, see the documentation for the[name](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#name)attribute. |
| **Display name** | The user-facing name on display in the Project view and in the Package Manager. For more information, see the documentation for the[displayName](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#displayName)attribute. |
| **Version** | The package version number. For more information, see the documentation for the[version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#version)attribute. |
| **Minimal Unity version** | Enable this option to specify the lowest Unity version this package is compatible with. When you enable this option, the**Major**,**Minor**, and**Release**properties appear.  Disable this option to indicate that this package is compatible with all Unity versions and remove the**Major**,**Minor**, and**Release**properties.  For more information, see the documentation for the[unity](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#unity)attribute. |
| **Major** | Specify the MAJOR portion of the minimal Unity version. For more information, see the documentation for the[unity](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#unity)attribute. |
| **Minor** | Specify the MINOR portion of the minimal Unity version. For more information, see the documentation for the[unity](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#unity)attribute. |
| **Release** | Specify the UPDATE and RELEASE portion of the minimal Unity version. For more information, see the documentation for the[unityRelease](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#unityRelease)attribute. |



## Dependencies

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/class-PackageManifestImporter-Depend.png "Dependencies section")

Dependencies section

Lists the other packages that are dependencies for this package. Each entry consists of the official package name \(for example,**“com.unity.progrids”**\) and its version number.

To add a new dependency:

1. Click the add button \(
   **+**
   \). A new row appears in the list.
2. Fill out the
   **Package name**
   and
   **Version**
   . For more information, see the documentation for the
   [dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#dependencies)
   attribute.

To remove a dependency:

1. Select the entry you want to remove.
2. Click the remove button \(
   **-**
   \). The row disappears from the list.

---

* 2019–04–11 Page published with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Custom Packages added in Unity[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20191)




# Asset packages

Unity Assets and items on the Unity**Asset Store**  
are supplied in**Asset packages**.**Asset packages**are collections of files and data from Unity Projects, or elements of Projects, which are compressed and stored in one file, similar to zip files. Like zip files, an Asset package maintains its original directory structure when it is unpacked, as well as metadata about Assets \(such as import settings and links to other Assets\).

In Unity, the**Assets**menu option**Export Package**compresses and stores the collection, while**Import Package**unpacks the collection into your currently open Unity Project.

This page contains information on:

* [Importing Asset packages](https://docs.unity3d.com/2019.2/Documentation/Manual/AssetPackages.html#ImportingPackages)
* [Exporting and updating Asset packages](https://docs.unity3d.com/2019.2/Documentation/Manual/AssetPackages.html#ExportingPackages)



## Importing Asset packages

You can import**Custom Asset Packages**, which are collections of Assets that users and developers in the Unity community have made available on the Asset Store.

**Note**:**Standard Asset**  
Packages are deprecated and should no longer be used.

To import an Asset package:

1. Open the Project you want to import Assets into.
2. Choose
   **Assets**

 

   &gt;
   **Import Package**
   &gt;
   **Custom Package**
   .
3. In the file explorer, select the package you want and the Import Unity Package dialog box appears, with all the items in the package pre-checked, ready to install. \(See Import Unity Package dialog box image below.\)
4. Select
   **Import**
   and Unity puts the contents of the package into the Assets folder, which you can access from your
   **Project view**

 

   .

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/CustomPackageInstallDialog.png "New install Import Unity Package dialog box")

New install Import Unity Package dialog box



## Exporting Asset packages

Use**Export Package**to create your own**Custom Package**.

1. Open the Project you want to export Assets from.

2. Choose**Assets &gt; Export Package**from the menu to bring up the**Exporting Package**dialog box. \(See_Exporting Package dialog box_image below.\)

3. In the dialog box, select the Assets you want to include in the package by clicking on the boxes so they are checked.

4. Leave the**include dependencies**box checked to auto-select any Assets used by the ones you have selected.

5. Click on**Export**to bring up the file explorer, and choose where you want to store your package file.

6. Name and save the package anywhere you like.

**HINT:**When exporting a package Unity can export all dependencies as well. So, for example, if you select a**Scene**  
and export a package with all dependencies, then Unity exports all Models, Textures and other Assets that appear in the**Scene**as well. This can be a quick way of exporting several Assets without manually locating them all.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/ExportPackageDialog.png "Exporting Package dialog box")

Exporting Package dialog box

### Updating Asset packages

Sometimes you may want to change the contents of a package and create a newer, updated version of your Asset package. To do this:

1. Select the Asset files you want in your package \(select both the unchanged ones and the new ones\).

2. Export the files as described above in_**Export Package**_, above.

**Note:**You can re-name an updated package and Unity recognizes it as an update, so you can use incremental naming: for example,`MyAssetPackageVer1`,`MyAssetPackageVer2`.

**Hint:**Avoid removing files from Asset packages and then replacing them with the same name: Unity recognizes them as different and possibly conflicting files and then displays a warning symbol when they are imported. If you have removed a file and then decide to replace it, it is better to give it a different but related name to the original.



---

* 2019–06–27  Page amended with limited
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




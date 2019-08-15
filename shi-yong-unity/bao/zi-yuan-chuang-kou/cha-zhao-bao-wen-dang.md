# Finding package documentation

The Unity Manual provides documentation for a specific version of Unity. Each package has its own version, so each package provides documentation for a specific version of that package. For this reason, the package documentation isn’t part of the main Unity Manual documentation; instead, documentation for each package lives on its own_micro-site_on Unity’s documentation server.

To access the documentation for a specific package, you have two options:

* [Get documentation for the latest version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-docs.html#Manual)
  \(from the Unity Manual\).
* [Get documentation for a specific package version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-docs.html#Editor)
  \(from the
  **Packages**
  window\).

When the package page opens, you can see four links at the top of the page.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-DocSite.png "Unitys Package documentation menu bar")

Unity’s Package documentation menu bar

To switch back and forth between the**Manual**documentation, the**Scripting API**documentation, the**Changelog**, and the**License**information for this package, click the corresponding link at the top of the page.



## Getting documentation for the latest version

Each version of the Unity Manual documentation provides the[Packages documentation](https://docs.unity3d.com/2019.2/Documentation/Manual/PackagesList.html)page, which lists the packages you can use with that version of Unity:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-List.png "Unity packages list")

Unity packages list

You can click the link in the list to open the latest version of that package documentation, where latest means the highest version generated. If you can’t find the package you want in this list, there might be several reasons:

* It isn’t released for this version of Unity.
* It is a
  **preview**
  package. The packages list includes only a limited number of
  **preview packages**
 

  .
* It is a private package. Some packages are not available to everyone because someone outside of Unity is developing them or because they are under a special license.

You might be able to access the documentation[through the Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-docs.html#Editor)for preview packages and packages released in another version of Unity. In the case of private packages, try to contact the developer directly to request access.



## Getting documentation for a specific package version

You can find out more about a package by viewing its documentation, changelog, or license information.

To access any of these pages, you can click the**View documentation**,**View changelog**, or**View licenses**links from inside the**Packages**window.

To access the documentation for a specific package version:

1. Open the[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-actions.html)in Unity.

2. If you are looking for a**preview**package, select**Show preview packages**from the**Advanced**drop-down menu.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs.png "Show preview packages")
   Show preview packages

3. Select the package you want information for from the list on the left.

4. Expand the arrow to the left of the package in the list.

   A new row appears, displaying the**See all versions**link.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs1.png "See all versions")
   See all versions

5. Click the**See all versions**link.

   A scrollable list appears with all available versions.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs2.png "All available versions")
   All available versions

6. Click on another version to select it.

   The package details appear in the pane on the right.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs3.png "Select a version to see its details")
   Select a version to see its details
   Notice the**verified**tag no longer appears in this example because version 1.2.4 of the TextMesh Pro package is not verified for Unity version 2019.1.

7. Click the**View documentation**link to open the documentation for the selected version of the package.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs4.png "View documentation")
   View documentation
   **NOTE**: If you are offline when you click the**View documentation**link and the package is on your computer \(that is, embedded or installed from a local folder\), the Package Manager opens the first MD file it finds under the`<package-root-folder>/Documentation~`folder in your default MD viewer. If the Package Manager installed the package from a server \(that is, from a package registry server or a Git remote repository\), the following message appears instead:

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs5.png "This package does not contain offline documentation")
   This package does not contain offline documentation

You can follow this procedure for any version of any package. Note that the documentation is not necessarily different for each package version release, since some version updates \(patches\) involve only bug fixes or trivial changes.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

  



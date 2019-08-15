# List view

The**Packages**window displays the list of packages according to the criteria that you select by filtering, including, or searching:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-View.png "List of all packages available, including preview packages")

List of all packages available, including preview packages

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterA.png "A")You can click these expander icons to show and hide the list of versions available for this package.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterB.png "B")The package version displays the version of the package that’s installed. If the package is not yet installed, the version that appears is the recommended version.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterC.png "C")These icons show you the status of the package:

| **Icon:** | **Description** |
| :--- | :--- |
| ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-checkmark.png "check mark") | A check mark indicates that the package is already[installed](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-install.html)or[enabled](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-disable.html). |
| ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-downloadicon.png "download icon") | The download icon indicates that the installed packages have an[available update](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-update.html). |
| ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-errorflag.png "error indicator") | An error icon indicates that something went wrong during installation or loading. For more advice on resolving errors, see[Error messages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-errors.html). |

By default, the**Packages**window displays the list of**All packages**with no[Preview](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Preview)packages, but you can[filter](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-filter.html)the list to display only packages installed in your Project \(including[local](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-localpath.html)packages\) or display only[built-in](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#BuiltIn)Unity packages. You can also[include Preview packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-list.html#ShowPreview)in the list and[search](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-search.html)for a specific package by package[name](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#name),[tag](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html#Tags)  
name, or package[version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Versions).



## Including Preview packages

[Preview](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Preview)packages do not appear by default in the list of packages on the**Packages**window. This is because**preview packages**  
might be unstable, so you should not use them in production.

To include preview packages in the list, select**Show preview packages**from the[Advanced](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html#Advanced)drop-down menu.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-docs.png "Show preview packages")

Show preview packages



## Finding a specific version

To view the list of versions available for a package:

1. In the list of packages, click the expander icon to the left of the package name.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-AvailableUpdates.png "List with no preview versions")
   List with no preview versions
   If there are updates available, they are displayed along with the**See all versions**link.

2. Click**See all versions**to see the list of all available versions for that package.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-AvailableVersions.png "List with preview versions")
   List with preview versions

3. You can select any of these versions for the current package and see the details specific to that version in the[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html).

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




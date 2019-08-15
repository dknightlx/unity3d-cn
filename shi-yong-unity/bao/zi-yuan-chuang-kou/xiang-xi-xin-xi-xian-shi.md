# Details view

The pane on the right side of the Packages window displays details about the selected package.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-DetailsPane.png "Package details")

Package details

These details include the following information:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterA.png "A")The display name.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterB.png "B")The[package version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-list.html#VersionList)\(and[tag](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html#Tags), if available\)

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterC.png "C")The links to[open the package documentation](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-docs.html)page, the package change log \(if available\), and the license information.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterD.png "D")The official package name from the[registry](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Registry). Unity packages always start with “**com.unity.**”.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterE.png "E")The author.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterF.png "F")A brief description.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterG.png "G")Dependency information. This section lists whether this package depends on another package and which version. Installed packages indicate the status of the dependencies after the version number. Packages without dependencies display the message “No dependencies”.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterH.png "H")Packages that include sample Assets display the samples along with an import button. To import the sample code, click the**Import in project**button next to the sample.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterI.png "I")Button to[install](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-install.html)or[update](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-update.html)a package \(or the**Up to date**message if the selected version is already installed.\)

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LetterJ.png "J")Buttons to[remove](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-remove.html)or[disable](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-disable.html)the package.



## Status bar

The Package Manager displays messages in the status bar at the bottom left of the Packages window.

There are typically three status messages that you might see. The**Loading packages**message appears briefly the first time you open Packman**UI**  
in a new Project. However, if the Package Manager[detects a problem](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-errors.html), such as a missing network connection, the Package Manager displays a warning in the status bar:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-StatusBar_Network.png "Network error message")

Network error message

A message also appears to inform you when the Packages window last refreshed its information:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-StatusBar_Update.png "Update message")

Update message



## Tags

Some packages display tags next to the version number. These tags convey information about the source or state of the package:

* [Source](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Sources)
  tag types indicate where the package originates from \(for example, whether it comes from a local directory or is downloaded from the package registry\).
* [State](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#States)
  tag types indicate at the package’s stage of the development cycle. For example, whether it is in development, preview, or verified for a specific version of Unity.

Some source tags imply state tags and vice versa \(for example, if a package is embedded in your Project, then Unity automatically assumes it is in development, so only the**in development**tag appears in the[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html)\).

The**Packages**window displays the following values:

| **Tag** | **Type** | **Meaning** |
| :--- | :--- | :--- |
| [Verified](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Verified) | state | Unity’s Quality Assurance team has verified this package to work with a specific version of the Editor. |
| [Preview](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Preview) | state | This package is at an early stage of the release cycle. It might not have complete documentation, or it might not be fully validated by either the development team or Unity’s Quality Assurance team. |
| [In Development](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Develop) | state | This package is in a very early stage of development and is[embedded](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Embedded)in your Project. |
| [Local](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Local) | source | This package is located on your local disk but is external to your Unity Project folder. |

**NOTE**: If no tag appears beside the package version in the[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html), it is[production quality](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Production), which means it is fully validated, documented, supported, and incrementally updated.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




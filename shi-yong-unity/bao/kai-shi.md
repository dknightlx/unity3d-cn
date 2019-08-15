# Getting started

The Package Manager uses three interfaces to communicate with users, manifests, and registries:

* You can use the
  [Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html)
  , which is the Package Manager user interface, to quickly browse and search for features. It also allows you to easily select the packages you want to install and update, and resolve conflicts in package dependencies.
* The Package Manager provides a
  [dedicated Inspector](https://docs.unity3d.com/2019.2/Documentation/Manual/class-PackageManifestImporter.html)
  in Unity, which allows you to walk through the contents of any package and view its manifest. This
  [Project view integration](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-inspect.html)
  means you can also edit
  **package manifests**

 

  directly in Unity for
  [embedded](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Embedded)
  or
  [local](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Local)
  packages.
* The
  [Package Manager scripting API](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-api.html)
  enables users to interact with the Package Manager programmatically.

## Where to find out more information about packages

The next step depends on what level of experience you have and what problem you are trying to solve.

If you are only interested in finding documentation for a specific package, see[Finding package documentation](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-docs.html).

For information about using packages with the Unity Package Manager, the following table provides links to various topics of this documentation:

| **What do you want to do?** | **See this documentation:** |
| :--- | :--- |
| **Get an introduction to Packages** | [Finding packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-find.html)explains how to use the**Packages**window to find specific versions of each package.  The[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html)section explains how to interact with the Unity Package Manager inside Unity.  The[Packages documentation](https://docs.unity3d.com/2019.2/Documentation/Manual/PackagesList.html)page lists the packages that are currently available for this version of Unity, with links to the documentation for the most recent version published. |
| **Install a package** | [Installing from the registry](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-install.html)describes how to use the**Packages**window to install a new package from the registry.  [Installing a local package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-local.html)describes how to use the**Packages**window to install a package from a local folder.  [Dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-dependencies.html)describes how to edit the Project manifest to install packages from all locations, including two locations that the**Packages**window doesn’t support:[Embedded](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-embed.html)and[Git URLs](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-git.html).  [Switching to another package version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-update.html)describes how to use the**Packages**window to switch versions of a package already installed.  [Removing an installed package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-remove.html)describes how to use the**Packages**window to remove a package from your Project.  [Disabling a built-in package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-disable.html)describes how to use the**Packages**window to enable and disable built-in packages. |
| **Troubleshoot a package** | If any of your Project’s packages, including the[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html)itself, fails to load correctly, refer to the[Troubleshooting](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-errors.html)and[Package conflicts](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-conflicts.html)sections. |
| **Learn more about working with manifests** | The[Project manifest](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html) reference page describes each attribute, including what values are valid and what role they play.  The[Inspecting packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-inspect.html)reference page describes how to view a package manifest in the Inspector. If the package is mutable \(editable\), you can also use the Inspector to modify the manifest itself. |
| **Learn advanced ways to work with packages** | To get started creating scripts that interact with the Package Manager, see[Scripting API for packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-api.html). It provides a high-level overview of working with the Package Manager APIs and code samples for[browsing the list of packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-api.html#Find)and[adding a package to a Project](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-api.html#Install).  If you want to find out about how to use your own package registry server in addition to the standard Unity registry, see[Scoped package registries](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html). |
| **Build and share your own tools and Assets in a package** | The[Custom packages](https://docs.unity3d.com/2019.2/Documentation/Manual/CustomPackages.html)section is a complete guide on building your own packages. It explains custom package requirements, such as naming and file structure. It also covers how to fill out the package manifest, share your package, and more. |

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




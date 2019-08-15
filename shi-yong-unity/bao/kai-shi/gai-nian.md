# Concepts

This section explains many of the concepts surrounding the Unity Package Manager functionality:

* [Versions](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Versions)
* [Manifests](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Manifests)
 
* [Registry](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Registry)
* [Package Management](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Management)
* [Package states](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#States)
* [Package sources](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Sources)



## Versions

Multiple versions of each package are available, marking changes to that package along its life cycle. Every time a developer updates the package, they[give it a new version number](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#pkg-ver). A change in package version tells you whether it contains a breaking change \(major\), a new backward-compatible functionality \(minor\), or bug fixes only \(patch\), following[Semantic Versioning](http://semver.org/).

To view the list of versions available for a specific package, see[Finding a specific version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-list.html#VersionList).



## Manifests

There are two types of manifest files:

* [Project manifests](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html)

 

  \(
  `manifest.json`
  \) These store information that the Package Manager needs to locate and load the right packages, including a list of packages and versions declared as dependencies.
* [Package manifests](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html)

 

  \(
  `package.json`
  \). These store information about a specific package, and a list of packages and versions that the package requires.

Both files use[JSON](https://json.org/)\(JavaScript Object Notation\) syntax.



## Registry

Unity maintains a central registry of official packages that are available for distribution. A[package registry](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html#registry)stores package contents and information \(metadata\) on each package version. By default, all Projects use the official Unity package registry, but you can[add additional registries](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html)to store and distribute private packages or stage packages in development.



## Package Management

The Unity Package Manager is a tool that manages the entire package system. Its primary tasks include the following:

* It communicates with the Unity registry and any additional registries you specify.
* It reads your
  [Project manifest](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html)
  and fetches package contents and metadata.
* It installs, upgrades, and uninstalls packages, whether they are dependencies of the Project or one of the installed packages.
* It enables and disables Unity’s
  **built-in packages**
 

  .
* It displays information about every version of every package.
* It
  [resolves conflicts](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-conflicts.html)
  when the Project and its packages require more than one package version.

The Unity Package Manager installs samples, tools, and Assets on a per-Project basis, rather than installing them across all Projects for a specific machine or device. It uses a read-only[global cache](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-cache.html)to store downloaded package metadata and contents. Once installed, Unity treats[package Assets](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-assets.html)just like any other Asset in the Project, except that these Assets are**immutable**  
\(read-only\). You can only change Assets from[Local](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Local)and[Embedded](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Embedded)package sources.



## Package states

States indicate where the package is in the development cycle:

| **State** | **Description** |
| :--- | :--- |
| **In Development** | The package developer is still creating the package. Usually this corresponds to having the package embedded in the developer’s Project. |
| **Preview** | The package is ready to use and can appear in the package registry, but it is not ready for use in production. This stage is like a beta cycle. |
| **Production-ready** | The package is safe to use in production and the developer has published it to the package registry. |
| **Verified** | The package has undergone testing and has been verified to work safely with a specific version of Unity, and all other packages verified for that version. |

The**Packages**window displays a tag that corresponds to some of these states. For more information, see[Tags](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html#Tags)  
.



## Package sources

Sources describe where the package came from:

| **Source** | **Description** |
| :--- | :--- |
| **Registry** | The Unity Package Manager downloads most packages from a package registry into a[global cache](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-cache.html)on your computer as you request them. These packages are immutable \(read only\), so you can use them in your Project, but you cannot modify them or change their package manifests. |
| **Built-in** | These packages allow you to enable or disable Unity features \(for example, Terrain Physics, Animation, etc.\). They are immutable \(read only\). |
| **Embedded** | Any package stored inside your Project folder is_embedded_. This source corresponds with the_in development_state because you typically put all the scripts, libraries, samples, and other Assets your new package needs in a folder under your Project folder when you begin development on a package. |
| **Local** | You can[install a package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-local.html)from any folder on your computer \(for example, if you have cloned a development repository locally\). |
| **Git** | The Package Manager installs**Git**packages directly from a Git repository instead of from the registry server. |

To edit the package manifest for a package, see[Inspecting packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-inspect.html).

The**Packages**window displays a tag that corresponds to some of these sources. For more information, see[Tags](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html#Tags).

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




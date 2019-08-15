# Packages

A package is a container that stores various types of features or Assets, such as:

* Editor tools and libraries, such as a text editor, an animation viewer or test frameworks.
* Runtime tools and libraries like the Physics API or a Graphics pipeline.
* Asset collections, such as Textures or animations.
* Project templates to share common project types with others.

Packages are newer, more tightly integrated versions of[Asset packages](https://docs.unity3d.com/2019.2/Documentation/Manual/AssetPackages.html)  
, able to deliver a wide range of enhancements to Unity through the Package Manager. In the Editor, you can access the[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html)through this menu:**Window**&gt;**Package Manager**.

## How Unity works with packages

When Unity opens a Project, the[Unity Package Manager](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-parts.html)reads the[Project manifest](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html)  
\(**1**\) to figure out what packages to load in the Project. Then it sends a request \(**2**\) to the[registry server](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-concepts.html#Registry)\(**3**\) for each package that appears as a dependency in the manifest. The registry server sends the requested information and data back to the Package Manager \(**4**\), which then installs those packages \(**5**\) in the Project. Each Project has its own manifest which lists the packages to load as “dependencies” of the Project.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-overview.png "How the Unity Package Manager installs packages")

How the Unity Package Manager installs packages

If you want to include a package in your Project, you must update the[Project manifest](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html)to include it in the list of dependencies. If you want to, you can modify the Project manifest directly, but it is safer and easier to let the Package Manager do that. For more information on using the user interface, see the documentation for the[Packages window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html).

---

* 2019–04–11 Page published with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Unity Package Manager added in Unity[2018.1](https://docs.unity3d.com/2018.1/Documentation/Manual/30_search.html?q=newin20181)




# Package conflicts

When you add a package to a**Project manifest**  
, Unity considers that package a dependency of the Project. However, a package can also have dependencies on other packages, which might create indirect dependencies in a Project that uses this package.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-conflicts-dependencies.png "Direct and indirect package dependencies")

Direct and indirect package dependencies

In this example, if you install Package A and Package B in your Project, then your Project has direct dependencies on both Package A and Package B. However, if Package B also has a dependency on Package C, then your Project also has an indirect dependency on Package C.

A conflict exists when a Project has dependencies on a package with different versions. A conflict can only exist between two indirect dependencies, when neither is added explicitly in the dependencies of the Project’s manifest file.

To[resolve the package conflict](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-conflicts-auto.html), Unity considers the version number of the conflicted package and the number of levels of dependencies between the root and the packages. If you prefer to use a different version of the package, you can also[override Unity’s solution](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-conflicts-override.html).

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

  



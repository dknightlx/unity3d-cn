# Overriding Unity’s conflict resolution

To override the automatically selected version with a different version, explicitly define the package version you want to use in the Project. You can either install the package version through the Package Manager window or edit the Project’s manifest directly.

For example, this Project has the following**dependencies**value in its`manifest.json`file:

```
{
  "dependencies": {
    "A" : "1.0.0",
    "C" : "2.0.0"
  }
}


```

Package A has a dependency on**1.0.0**of Package B, and Package C has a dependency on**2.0.0**of Package B:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-conflicts-override.png "Overriding package versions in the manifest")

Overriding package versions in the manifest

In this case, the Package Manager flags Package B as being in conflict. Unity displays a conflict warning in the console and loads version**2.0.0**of Package B.

To suppress the warning, explicitly add version**2.0.0**of Package B to the Project:

```
{
  "dependencies": {
    "A" : "1.0.0",
    "B" : "2.0.0",
    "C" : "2.0.0"
  }
}

```

Alternatively, you can specify a third version in the`manifest.json`file:

```
{
  "dependencies": {
    "A" : "1.0.0",
    "B" : "3.0.0",
    "C" : "2.0.0"
  }
}

```

In this case, there is no conflict and Unity loads only version**3.0.0**of Package B.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




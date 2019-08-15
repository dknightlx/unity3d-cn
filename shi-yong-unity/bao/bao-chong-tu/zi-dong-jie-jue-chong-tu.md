# Automatic conflict resolution

When the Package Manager computes package dependencies, and finds requests for multiple versions of the same package, it automatically selects the package with the fewest dependency levels from the root. In the case of a tie, the Package Manager chooses the_highest_version among the versions that are tied. It then displays a description of the conflict in the Unity console.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-conflicts-auto.png "Package Manager chooses v2.0.0 of Package X because it is closer")

Package Manager chooses v2.0.0 of Package X because it is ‘closer’

In this example, the higher version \(**2.0.1**\) of Package X appears as a dependency three levels away from the Project \(via Package B and Package C\). The Package Manager loads version**2.0.0**of Package X because its dependency is two levels away from the Project \(via only Package A\).

**NOTE**: Even if the Package Manager can resolve which package to load, Unity still displays a conflict report in the console if Unity requests different_major versions_of the same package, such as**1.0.0**and**2.0.0**.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

  



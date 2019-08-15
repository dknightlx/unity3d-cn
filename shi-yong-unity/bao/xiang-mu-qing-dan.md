# Project manifest

When Unity loads a Project, the Unity Package Manager reads the**Project manifest**so that it can compute a list of which packages to load. When a user installs or uninstalls a package through the[Package Manager window](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui.html), the Package Manager stores those changes in the Project manifest file. The Project manifest file manages the list of packages through the[dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html#dependencies)object.

In addition, the Project manifest serves as a configuration file for the Package Manager. It stores the location of one or more package registries. For**Git packages**  
, it also provides a lock object defining a commit hash and revision number to guarantee that the Package Manager always installs exactly the same dependencies.

You can find the Project manifest file, called`manifest.json`, in the`Packages`folder under the root folder of your Unity Project. Like the[package manifest file](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html), the Project manifest file uses JSON \(JavaScript Object Notation\) syntax.

## Attributes

All attributes are optional. However, if your Project manifest file does not contain any values, the**Packages**window doesn’t load, and the Package Manager doesn’t load any packages.

**TIP**: At any time, you can fix any problems with your registry by choosing**Reset packages to defaults**[from the main Unity Help menu](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-errors.html#Reset). However, be aware that this action resets all changes you made to the packages in your Project so it is best to use this strategy as a last resort.

| **Key** | **JSON Type** | **Description** |
| :--- | :--- | :--- |
| **dependencies** | Object | List of packages available in your Project. This entry in the manifest uses a map structure to list[package names](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#name)associated with the[version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#version)required for the Project.  See the[Dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-dependencies.html)section for a more detailed overview of all supported schemes.  **NOTE**: This list does not include indirect dependencies \(packages required by other packages\). |
| **registry** | String | URL of the main Unity Package Manager registry. This overrides the default registry URL \(`https://packages.unity.com`\).  **NOTE**: If you override the default registry with your own registry, you lose access to the official Unity packages. Instead, if you want to augment the Unity package library with your own private collection of packages, set the**scopedRegistries**attribute to use a scoped registry instead. |
| **scopedRegistries** | Array of Objects | Specify custom registries in addition to the default registry. This allows you to host your own packages.  See the[Scoped registries](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html)section for more details. |
| **lock** | Object | Describes Git package resolution information with a commit hash and selected revision. Package Manager updates this attribute automatically. This guarantees the Package Manager installs exactly the same dependencies.  This attribute is reserved for Git packages, but other features might use it in the future to guarantee deterministic package version resolution. |
| **testables** | Array of Strings | Lists the package names that you want to include in the[Unity Test Runner](https://docs.unity3d.com/2019.2/Documentation/Manual/testing-editortestsrunner.html). For more information, see[Adding tests to a package](https://docs.unity3d.com/2019.2/Documentation/Manual/cus-tests.html). |

## Project manifest example

```
{
  "registry": "https://my.registry.com",
  "scopedRegistries": [{
    "name": "My internal registry",
    "url": "https://my.internal.registry.com",
    "scopes": [
      "com.company"
    ]
  }],
  "dependencies": {
    "com.unity.package-1": "1.0.0",
    "com.unity.package-2": "2.0.0",
    "com.unity.package-3": "3.0.0",
    "com.unity.my-local-package": "file:/path/to/com.unity.my-local-package",
    "com.unity.my-git-package": "https://my.repository/my-package.git#v1.2.3"
  },
  "lock": {
    "com.unity.my-git-package": {
       "hash": "9e72f9d5a6a3dadc38d813d8399e1b0e86781a49",
       "revision": "v1.2.3"
    }
  },
  "testables": [ "com.unity.package-1", "com.unity.package-2" ]
}

```

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




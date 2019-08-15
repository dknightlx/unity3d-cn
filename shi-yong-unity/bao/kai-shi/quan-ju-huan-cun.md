# Global Cache

When the Unity Package Manager downloads package contents and metadata, it stores them in a global cache. This makes re-using and sharing packages more efficient, and allows you to install and update stored packages even when offline. The global cache is read-only to users and installed with Unity starting with version 2017.4.

## Location

By default, Unity stores the global cache in a root directory that depends on the operating system \(and the user account type on Windows\):

| **Operating system** | **Default root directory** |
| :--- | :--- |
| Windows \(non-system user account\) | `%LOCALAPPDATA%\Unity\cache` |
| Windows \(system user account\) | `%ALLUSERSPROFILE%\Unity\cache` |
| macOS | `$HOME/Library/Unity/cache` |
| Linux | `$HOME/.config/unity3d/cache` |

## Structure

The Package Manager uses two different shared caches, each serving a different purpose. They are stored in subdirectories under the folder location above:

| **Subfolder** | **Description** |
| :--- | :--- |
| `npm` | Stores data obtained from registries using the[npm](https://www.npmjs.com/package/protocol)protocol. This includes package metadata and package[tarballs](https://en.wikipedia.org/wiki/Tar_%28computing%29). |
| `packages` | This cache contains the uncompressed contents of package tarballs fetched from a registry. |

Inside each of these subfolders, each registry has its own path so that packages hosted on different registries are not mixed up.

## Requirements

The user account running the Unity Editor process must have full write permissions on the root directory and its contents. Without these permissions, the Package Manager cannot download and save the package metadata and contents in the cache.

## Customizing the shared cache location

You can use two environment variables to override either global cache folder:

* **UPM\_NPM\_CACHE\_PATH**overrides the**npm**folder path. For example \(macOS\):

  `UPM_NPM_CACHE_PATH=/dev/ssd/shared/Unity/cache/npm`

* **UPM\_CACHE\_PATH**overrides the**packages**folder path. For example \(macOS\):

  `UPM_CACHE_PATH=/dev/ssd/shared/Unity/cache/packages`

You must restart the Unity Editor and the Hub after changing either of these environment variables for them to take effect.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

  



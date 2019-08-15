# Installing a local package

The Package Manager can load a package from anywhere on your computer even if you saved it outside your Unity Project folder \(for example, if you have a package called**com.unity.my-local-package**and you save it on the`Desktop`but your Unity Project is under the`Documents`folder\).

You can also use a folder inside your Project folder, provided that it is not one of the[reserved Project sub-folders](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-local.html#PkgLocation).

To load a package from your local disk:

1. Click the plus \(**+**\) icon in the status bar.

2. The**Add package from disk**button appears.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/PackageManagerUI-ExternalPackageButton.png "Add package from disk button")
   Add package from disk button

3. Click the**Add package from disk**button to bring up a file browser.

4. Navigate to the folder root of your**local package**.

5. Double-click the`package.json`file in the file browser.

The file browser closes, and the package now appears in the[package list](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-list.html)with the**local**tag.



## Local packages inside your Project

You can place a local package anywhere inside your Project except under these folders:

| **Project folder:** | **Reason:** |
| :--- | :--- |
| `Assets` | If you place a package inside this folder, the Asset Database imports any Assets under this folder twice: once as Assets and once as Package contents. |
| `Library` | Do not modify the contents of this folder. |
| `ProjectSettings` | This folder is for[settings](https://docs.unity3d.com/2019.2/Documentation/Manual/comp-ManagerGroup.html)Assets only. |
| `Packages` | If you place a package under this folder, the Package Manager automatically interprets it as an**Embedded package** , regardless of the reference in the**Project manifest** . |

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




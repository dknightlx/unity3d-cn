# Removing an installed package

You can only remove packages which are not required by another package.

**NOTE**: This only removes the_reference_to the package in the manifest. The package itself, including its contents, remains intact, even for**local packages**  
.

When you remove a package from a Project, any Editor or run-time functionality that it implemented is no longer available in that Project.

To remove an installed package:

1. Open the**Packages**window.

2. If the[package scope](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-filter.html)is set to**Built-in packages**  
   , select either**In Project**or**All packages**from the[package scope](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-filter.html)drop-down menu.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-ui-inprojects.png "Switch the scope to In Project")
   Switch the scope to In Project

3. Select the package you want to remove from the[list of packages](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-list.html). The[details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html)now displays that package’s information.

4. Click the**Remove**button.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/upm-ui-remove.png "Remove button in the bottom right corner of the details view")
   Remove button in the bottom right corner of the details view
   When the progress bar finishes, the package disappears from the list.

5. If you want to restore a removed package, follow the instructions for[installing a package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-install.html).

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




# Scene Visibility

Unity’s**Scene**  
visibility controls allow you to quickly hide and show**GameObjects**  
in the[Scene view](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingTheSceneView.html)  
without changing their in-game visibility. This is useful for working with large or complex Scenes where it can be difficult to view and select specific GameObjects.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisExVisible.png "Selected GameObjects are highlighted in orange")

Selected GameObjects are highlighted in orange

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisExHidden.png "Changing the Scene visibility settings hides the selected GameObjects in the scene view")

Changing the Scene visibility settings hides the selected GameObjects in the scene view

Using visibility options is safer than[deactivating GameObjects](https://docs.unity3d.com/2019.2/Documentation/Manual/DeactivatingGameObjects.html)because visibility options only affect the Scene view. This means you can’t accidentally remove GameObjects from the rendered scene, or trigger unnecessary bake jobs for lighting, occlusion, and other systems.

Unity saves Scene visibility settings to a file called_SceneVisibilityState.asset_in the Project’s_Library_folder. The scene reads from this file and updates it automatically whenever you change the visibility settings. This makes it possible for your settings to persist from one session to the next. Because source control setups for Unity typically ignore the_Library_folder, changing visibility settings should not create source control conflicts.

## Setting Scene visibility for GameObjects and their children

You control Scene visibility for individual GameObjects from the[Hierarchy window](https://docs.unity3d.com/2019.2/Documentation/Manual/Hierarchy.html).

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisIconsHierarchy.png "Every GameObject has a Scene visibility icon/toggle")

Every GameObject has a Scene visibility icon/toggle

To toggle Scene visibility:

* Click a GameObject’s visibility icon in the Hierarchy window, or press**H**, to hide/show the GameObject and its children.  
  
  Toggling visibility for an object and its children affects all child objects, from the “target” object all the way down to the bottom of the hierarchy.  
  

* **Alt**+ Click a GameObject’s visibility icon in the Hierarchy window to hide/show the GameObject only.  
  
  Toggling visibility for a single object does not affect its children. They retain whatever visibility status they had previously.  
  

* Click the scene’s visibility icon to hide/show everything in the scene.

Because you can toggle visibility for a whole branch or a single GameObject, you can end up with GameObjects that are visible, but have hidden children or parents. To help you track what’s going on, the visibility icon changes to indicate each GameObject’s status.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisIconsOvw.png)

|  |  |  |
| :--- | :--- | :--- |
| A | ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisVisibleHiddenChildren.png) | The GameObject is visible, but some of its children are hidden. |
| B | ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisHiddenVisibleChildren.png) | The GameObject is hidden, but some of its children are visible. |
| C | ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisVisible.png) | The GameObject and its children are visible. This icon only appears when you hover over the GameObject. |
| D | ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisHidden.png) | The GameObject and its children are hidden. |

Scene visibility changes you make in the Hierarchy window are persistent. Unity re-applies them whenever you toggle Scene visibility off and on again in the Scene view, close and re-open the Scene, and so on.

## Turning Scene visibility on and off

The Scene visibility switch in the[Scene view](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingTheSceneView.html)control bar displays the number of hidden GameObjects in the scene. Click it to toggle Scene visibility on and off.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisSceneViewToggle.png "The Scene visibility counter shows 14 hidden GameObjects in this scene")

The Scene visibility counter shows 14 hidden GameObjects in this scene

* Turning Scene visibility off essentially mutes the Scene visibility settings you set in the Hierarchy window, but doesn’t delete or change them. All hidden GameObjects are temporarily visible.  
  

* Turning Scene visibility back on re-applies the visibility settings set in the Hierarchy window.

## Isolating selected GameObjects

The Isolation view temporarily overrides the Scene visibility settings so that only the selected GameObjects are visible, and everything else is hidden.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneVisIsolation.png "Isolation view overrides Scene visibility settings so only the selection and its children \(A\) are visible.&amp;lt;br/&amp;gt;Clicking the Exit button \(B\) reverts to the previous Scene visibility settings.")

Isolation view overrides Scene visibility settings so only the selection and its children \(A\) are visible.

  


Clicking the Exit button \(B\) reverts to the previous Scene visibility settings.

To enter the Isolation view, press**Shift + H**.

This isolates all selected GameObjects and their children. Isolating hidden GameObjects makes them visible until you exit the Isolation view.

While in the Isolation view, you can continue to change Scene visibility settings, but any changes you make are lost on exit.

To exit the Isolation view, press**Shift + H**again, or click the**Exit**button in the Scene view.

Exiting the Isolation view reverts back to your original Scene visibility settings.

---

* 2019–05–07 Page published with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Scene Visibility options added in[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20191)




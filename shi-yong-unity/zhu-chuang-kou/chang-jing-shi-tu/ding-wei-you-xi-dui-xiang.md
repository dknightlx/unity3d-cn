# Positioning GameObjects

To select a**GameObject**  
, click on it in the[Scene view](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingTheSceneView.html)  
or click its name in the[Hierarchy window](https://docs.unity3d.com/2019.2/Documentation/Manual/Hierarchy.html). To select or de-select multiple GameObjects, hold the**Shift**key while clicking, or drag a rectangle around multiple GameObjects to select them.

Unity highlights selected GameObjects and their children in the Scene view. By default, the selection outline color is orange, and the child outline color is blue. You can also choose to highlight selected GameObjects’ wireframes in a different color. You can change all of these outline highlight colors from the Unity Preferences \(**Unity &gt; Preferences**on macOS or**Edit &gt; Preferences**on Windows\).

See documentation on the[Gizmos Menu](https://docs.unity3d.com/2019.2/Documentation/Manual/GizmosMenu.html)for more information about the outline and wireframe selection visualizations.

Selected GameObjects also display a**Gizmo**  
in the**Scene**  
view if you have one of the four Transform tools selected:

## Move, Rotate, Scale, and RectTransform

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/Editor-MoveRotateScaleTransform.png)

The first tool in the**toolbar**  
, the**Hand Tool**, is for panning around the Scene. The**Move**,**Rotate**,**Scale**,**Rect Transform**and**Transform**tools allow you to edit individual GameObjects. To alter the[Transform](https://docs.unity3d.com/2019.2/Documentation/Manual/class-Transform.html)component of the GameObject, use the mouse to manipulate any Gizmo axis, or type values directly into the number fields of the**Transform**component in the**Inspector**  
.

Alternatively, you can select each of the four**Transform**modes with a hotkey:**W**for Move,**E**for Rotate,**R**for Scale,**T**for RectTransform, and**Y**for Transform.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/MoveRotateScaleTransform.jpg "The Move, Scale, Rotate, Rect Transform and Transform Gizmos")

The Move, Scale, Rotate, Rect Transform and Transform Gizmos

### Move

At the center of the**Move**Gizmo, there are three small squares you can use to drag the GameObject within a single plane \(meaning you can move two axes at once while the third keeps still\).

If you hold shift while clicking and dragging in the center of the Move Gizmo, the center of the Gizmo changes to a flat square. The flat square indicates that you can move the GameObject around on a plane relative to the direction the Scene view**Camera**  
is facing.

### Rotate

With the**Rotate**tool selected, change the GameObject’s rotation by clicking and dragging the axes of the wireframe sphere Gizmo that appears around it. As with the Move Gizmo, the last axis you changed will be colored yellow. Think of the red, green and blue circles as performing rotation around the red, green and blue axes that appear in the Move mode \(red is the x-axis, green in the y-axis, and blue is the z-axis\). Finally, use the outermost circle to rotate the GameObject around the Scene view z-axis. Think of this as rotating in screen space.

### Scale

The**Scale**tool lets you rescale the GameObject evenly on all axes at once by clicking and dragging on the cube at the center of the Gizmo. You can also scale the axes individually, but you should take care if you do this when there are child GameObjects, because the effect can look quite strange.

### RectTransform

The[RectTransform](https://docs.unity3d.com/2019.2/Documentation/Manual/class-RectTransform.html)is commonly used for positioning 2D elements such as**Sprites**  
or[UI elements](https://docs.unity3d.com/2019.2/Documentation/Manual/UIBasicLayout.html), but it can also be useful for manipulating 3D GameObjects. It combines moving, scaling and rotation into a single Gizmo:

* Click and drag within the rectangular Gizmo to move the GameObject.
* Click and drag any corner or edge of the rectangular Gizmo to scale the GameObject.
* Drag an edge to scale the GameObject along one axis.
* Drag a corner to scale the GameObject on two axes.
* To rotate the GameObject, position your cursor just beyond a corner of the rectangle. The cursor changes to display a rotation icon. Click and drag from this area to rotate the GameObject.

Note that in 2D mode, you can’t change the z-axis in the Scene using the Gizmos. However, it is useful for certain scripting techniques to use the z-axis for other purposes, so you can still set the z-axis using the Transform component in the Inspector.

For more information on transforming GameObjects, see documentation on the[Transform Component](https://docs.unity3d.com/2019.2/Documentation/Manual/class-Transform.html)  
.

### Transform

The**Transform**tool combines the**Move**,**Rotate**and**Scale**tools. Its Gizmo provides handles for movement and rotation. When the**Tool Handle Rotation**is set to**Local**\(see below\), the Transform tool also provides handles for scaling the selected GameObject.

### Custom tools

If your Project uses custom Editor tools, some of them might also allow you to position GameObjects.

You can access custom tools by right-clicking the**Available Custom Editor Tools**button in the Scene view toolbar.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/Editor-CustomTools.jpg)

For information, see the documentation on[Using Custom Editor Tools](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingCustomEditorTools.html).



## Gizmo handle position toggles

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/GizmoDisplayToggles.png)

The**Gizmo handle position toggles**are used to define the location of any Transform tool Gizmo, and the handles use to manipulate the Gizmo itself.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/HandlePositionButtons.png "Gizmo display toggles")

Gizmo display toggles

### For position

Click the**Pivot**/**Center**button on the left to toggle between**Pivot**and**Center**.

* **Pivot**
  positions the Gizmo at the actual pivot point of a
  **Mesh**

 

  .
* **Center**
  positions the Gizmo at the center of the GameObject’s rendered bounds.

### For rotation

Click the**Local**/**Global**button on the right to toggle between**Local**and**Global**.

* **Local**
  keeps the Gizmo’s rotation relative to the GameObject’s.
* **Global**
  clamps the Gizmo to world space orientation.



### Unit snapping

While dragging any Gizmo Axis using the**Move**tool or the**Transform**tool, hold the**Control**  
key \(**Command**on Mac\) to snap to increments defined in the**Snap Settings**\(menu:**Edit**&gt;**Snap Settings…**\)

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneViewUnitSnappingSettings.png)

### Surface snapping

While dragging in the center using the**Move**tool, hold**Shift**and**Control**\(**Command**on Mac\) to quickly snap the GameObject to the intersection of any**Collider**  
.

### Look-at rotation

While using the**Rotate**tool, hold**Shift**and**Control**\(**Command**on Mac\) to rotate the GameObject towards a point on the surface of any**Collider**.

### Vertex snapping

Use**vertex snapping**to quickly assemble your Scenes: take any vertex from a given Mesh and place that vertex in the same position as any vertex from any other Mesh you choose. For example, use vertex snapping to align road sections precisely in a racing game, or to position power-up items at the vertices of a Mesh.

Follow the steps below to use vertex snapping:

1. Select the Mesh you want to manipulate and make sure the**Move**tool or the**Transform**tool is active.

2. Press and hold the**V**key to activate the vertex snapping mode.

3. Move your cursor over the vertex on your Mesh that you want to use as the pivot point.

4. Hold down the left mouse button once your cursor is over the vertex you want and drag your Mesh next to any other vertex on another Mesh.

5. Release the mouse button and the**V**key when you are happy with the results \(**Shift+V**acts as a toggle of this functionality\).

**Note:**You can snap vertex to vertex, vertex to surface, and pivot to vertex.

### Screen Space Transform

While using the**Transform**tool, hold down the**Shift**key to enable Screen Space mode. This mode allows you to move, rotate and scale GameObjects as they appear on the screen, rather than in the Scene.

---

* 2019–03–05 Page amended with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Transform tool added in[2017.3](https://docs.unity3d.com/2017.3/Documentation/Manual/30_search.html?q=newin20173)

* Selection Outline for child GameObjects added in[2018.3](https://docs.unity3d.com/2018.3/Documentation/Manual/30_search.html?q=newin20183)

* Button and menu to access custom Editor tools added in[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20183)




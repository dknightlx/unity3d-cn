# The Inspector window

Projects in the Unity Editor are made up of multiple[GameObjects](https://docs.unity3d.com/2019.2/Documentation/Manual/GameObjects.html)  
that contain**scripts**  
, sounds, Meshes, and other graphical elements such as Lights. The**Inspector**window \(sometimes referred to as “the Inspector”\) displays detailed information about the currently selected GameObject, including all attached[components](https://docs.unity3d.com/2019.2/Documentation/Manual/Components.html)  
and their properties, and allows you to modify the functionality of GameObjects in your**Scene**  
.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorWindowCallout.jpg "The Inspector in its default position in Unity")

The Inspector in its default position in Unity

## Inspecting GameObjects

Use the Inspector to view and edit the properties and settings of almost everything in the Unity Editor, including physical game items such as GameObjects, Assets, and Materials, as well as in-Editor settings and preferences.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/GenericInspector.png "The Inspector window displaying settings for a typical GameObject and its components")

The Inspector window displaying settings for a typical GameObject and its components

When you select a GameObject in either the[Hierarchy](https://docs.unity3d.com/2019.2/Documentation/Manual/Hierarchy.html)or[Scene view](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingTheSceneView.html)  
, the Inspector shows the properties of all components and Materials of that GameObject. Use the Inspector to edit the settings of these components and Materials.

The image above shows the Inspector with the Main**Camera**  
GameObject selected. In addition to the GameObject’s Position, Rotation, and Scale values, all the properties of the Main**Camera**are available to edit.

## Inspecting script variables

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorExampleObjWithScripts.png "The Inspector window displaying settings for a GameObject with several custom scripts attached. The scripts’ public properties are available to edit")

The Inspector window displaying settings for a GameObject with several custom scripts attached. The scripts’ public properties are available to edit

When GameObjects have custom script components attached, the Inspector displays the public variables of that script. You can edit these variables as settings in the same way you can edit the settings of the Editor’s built-in components. This means that you can set parameters and default values in your scripts easily without modifying the code.

## Inspecting Assets

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorExampleMaterial.png "The Inspector window displaying the settings for a Material Asset")

The Inspector window displaying the settings for a Material Asset

When an[Asset](https://docs.unity3d.com/2019.2/Documentation/Manual/AssetWorkflow.html)  
is selected in your[Project window](https://docs.unity3d.com/2019.2/Documentation/Manual/ProjectView.html), the Inspector shows you the settings related to how that Asset is imported and used at run time \(when your game is running either in the Editor or your published build\).

Each type of Asset has a different selection of settings. The images below demonstrate some examples of the Inspector displaying the import settings for other Asset types:

The[Model tab](https://docs.unity3d.com/2019.2/Documentation/Manual/FBXImporter-Model.html)of the[Model Import Settings](https://docs.unity3d.com/2019.2/Documentation/Manual/class-FBXImporter.html)window:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/MeshExample40.png "The Inspector window displaying the import settings for an .fbx file containing 3D Models")

The Inspector window displaying the import settings for an .fbx file containing 3D Models

The[Audio Clip Import Settings](https://docs.unity3d.com/2019.2/Documentation/Manual/class-AudioClip.html)window:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorExampleAudio.png "The Inspector window displaying the import settings for an Audio file")

The Inspector window displaying the import settings for an Audio file

The[Texture Import Setting](https://docs.unity3d.com/2019.2/Documentation/Manual/class-TextureImporter.html)window:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorExampleTexture.png "The Inspector window displaying the Import Settings for a Texture")

The Inspector window displaying the Import Settings for a Texture

## Prefabs

If you have a Prefab selected, some additional options are available in the Inspector window.

For more information, see documentation on[Prefabs](https://docs.unity3d.com/2019.2/Documentation/Manual/Prefabs.html)  
.

## Project settings

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/InspectorExampleSettings.png "The Inspector window displaying the Tags &amp; Layers Project Settings panel")

The Inspector window displaying the

**Tags **

**&**

** Layers**

Project Settings panel

When you select any of the Project Settings categories \(menu:**Editor**&gt;**Project Settings**  
\), these settings are displayed in the Inspector window. For more information, see documentation on[Project Settings](https://docs.unity3d.com/2019.2/Documentation/Manual/comp-ManagerGroup.html).

## Icons and labels

You can assign custom icons to GameObjects and scripts. These display in the Scene view along with built-in icons for GameObjects such as Lights and Cameras.

For more about icons and labels, see Unity documentation on[assigning icons](https://docs.unity3d.com/2019.2/Documentation/Manual/AssigningIcons.html).

## Re-ordering components

To reorder components in the Inspector window, drag-and-drop their headers from one position to another. When you drag a component header, a blue insertion marker appears. This shows you where the component should go when you drop the header:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/DragAndDropComponent.png "Dragging and dropping components on a GameObject in the Inspector window")

Dragging and dropping components on a GameObject in the Inspector window

You can only reorder components on a GameObject. You can’t move components between different GameObjects.

You can also drag and drop script Assets directly into the position you want them to appear.

When you select multiple GameObjects, the Inspector displays all of the components that the selected GameObjects have in common. To reorder all of these common components at once, multi-select the GameObjects, then drag-and-drop the components into a new position in the Inspector.

The order you give to components in the Inspector window is the order you need to use when querying components in your user scripts. If you query the components programmatically, you’ll get the order you see in the Inspector.

---

* 2018–04–23 Page amended with limited[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Component drag and drop added in Unity 5.6




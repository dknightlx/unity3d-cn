# Scene view control bar

The**Scene view**  
control bar lets you choose various options for viewing the**Scene**  
and also control whether lighting and audio are enabled. These controls only affect the**Scene view**during development and have no effect on the built game.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneViewControlBar.png)

## Draw mode menu

The first drop-down menu selects which**Draw Mode**will be used to depict the Scene. The available options are:

### Shading mode

* **Shaded**
  : show surfaces with their textures visible.
* **Wireframe**
  : draw meshes with a wireframe representation.
* **Shaded Wireframe**
  : show meshes textured and with wireframes overlaid.

### Miscellaneous

* **Shadow Cascades**
  : show directional light
  [shadow cascades](https://docs.unity3d.com/2019.2/Documentation/Manual/DirLightShadows.html)
  .
* **Render Paths**
  : show the
  [rendering path](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderingPaths.html)

 

  for each object using a color code: Blue indicates
  [deferred shading](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderTech-DeferredShading.html)

 

  , Green indicates
  [deferred lighting](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderTech-DeferredLighting.html)
  , yellow indicates
  [forward rendering](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderTech-ForwardRendering.html)

 

  and red indicates
  [vertex lit](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderTech-VertexLit.html)
  .
* **Alpha Channel**
  : render colors with alpha.
* **Overdraw**
  : render objects as transparent “silhouettes”. The transparent colors accumulate, making it easy to spot places where one object is drawn over another.
* **Mipmaps**
  : show ideal texture sizes using a color code: red indicates that the texture is larger than necessary \(at the current distance and resolution\); blue indicates that the texture could be larger. Naturally, ideal texture sizes depend on the resolution at which the game will run and how close the
  **camera**

 

  can get to particular surfaces.
* **Texture Streaming**
  : tint
  **GameObjects**

 

  green, red, or blue, depending on their status in the
  [Texture Streaming](https://docs.unity3d.com/2019.2/Documentation/Manual/TextureStreaming.html)
  system. For more information, see documentation on
  [Texture Streaming debugging](https://docs.unity3d.com/2019.2/Documentation/Manual/TextureStreaming-API.html#Debugging)
  .

### Deferred

These modes let you view each of the elements of the G-buffer \(**Albedo**,**Specular**,**Smoothness**and**Normal**  
\) in isolation. See documentation on[Deferred Shading](https://docs.unity3d.com/2019.2/Documentation/Manual/RenderTech-DeferredShading.html)for more information.

### Global Illumination

The following modes are available to help visualise aspects of the[Global Illumination](https://docs.unity3d.com/2019.2/Documentation/Manual/GlobalIllumination.html)system:**UV Charts**,**Systems**,**Albedo**,**Emissive**,**Irradiance**,**Directionality**,**Baked**,**Clustering**and**Lit Clustering**. See documentation on[GI Visualisations](https://docs.unity3d.com/2019.2/Documentation/Manual/GIVis.html)for information about each of these modes.

### Material Validator

There are two**Material Validator**modes:**Albedo**and**Metal Specular**. These allow you to check whether your physically-based materials use values within the recommended ranges. See[Physically Based Material Validator](https://docs.unity3d.com/2019.2/Documentation/Manual/MaterialValidator.html)for more information.

## 2D, lighting and Audio switches

To the right of the**Render Mode**menu are three buttons that switch certain Scene view options on or off:

* **2D**
  : switches between 2D and 3D view for the Scene. In 2D mode the camera is oriented looking towards positive z, with the x axis pointing right and the y axis pointing up.
* **Lighting**
  : turns Scene view lighting \(lights, object shading, etc\) on or off.
* **Audio**
  : turns Scene view
  **audio effects**

 

  on or off.

## Effects button and menu

The menu \(activated by the small mountain icon to the right of the**Audio**button\) has options to enable or disable**rendering**  
effects in the Scene view.

* **Skybox**

 

  : a skybox texture rendered in the Scene’s background
* **Fog**

 

  : gradual fading of the view to a flat color with distance from the camera.
* **Flares**

 

  :
  **lens flares**

 

  on lights.
* **Animated Materials**
  : Defines whether or not animated materials show the animation

The**Effects**button itself acts as a switch that enables or disables all the effects at once.

## Scene visibility switch

The Scene visibility switch toggles Scene visibility for GameObjects on and off. When it’s on, Unity applies the Scene visibility settings. When it’s off, Unity ignores them. This switch also displays the number of hidden GameObjects in the Scene.

For more information, see the documentation on[Scene Visibility](https://docs.unity3d.com/2019.2/Documentation/Manual/SceneVisibility.html).

## Component Editor Tools panel switch

The Component Editor Tools panel switch toggles a**toolbar**  
for custom commands that affect the current selection. The**toolbar**appears in a window inside the main Scene view window.

For more information see the documentation on[Using Custom Editor Tools](https://docs.unity3d.com/2019.2/Documentation/Manual/UsingCustomEditorTools.html).

## Camera settings menu

The Camera settings menu contains options for configuring the Scene view camera. For more information, see the documentation on[Camera settings](https://docs.unity3d.com/2019.2/Documentation/Manual/SceneViewCamera.html).

## Gizmos menu

The**Gizmos**menu contains lots of options for how objects, icons, and**gizmos**  
are displayed. This menu is available in both the Scene view and the[Game view](https://docs.unity3d.com/2019.2/Documentation/Manual/GameView.html). See documentation on the[Gizmos Menu](https://docs.unity3d.com/2019.2/Documentation/Manual/GizmosMenu.html)manual page for more information.

## Search box

The rightmost item on the control bar is a search box that lets you filter items in the Scene view by their names and/or types \(you can select which with the small menu at the left of the search box\). The set of items that match the search filter are also shown in the Hierarchy view which, by default, is located to the left of the Scene view.

* 2019–03–05 Page amended with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Scene Visibility Switch added in[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20191)

* Scene view Camera settings added in 2019.1

* Component Editor Tools panel switch added in 2019.1




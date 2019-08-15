# Scene view Camera

The**Camera**  
settings menu contains options for configuring the**Scene view**  
**Camera**. These adjustments do not affect the settings on**GameObjects**  
with**Camera**components.

To access the Camera settings menu, click the Camera icon in the**toolbar**  
of the**Scene**  
view.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneViewCameraIcon.png "The Camera icon in the Scene view")

The Camera icon in the Scene view

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/SceneViewCameraSettings.png "The Camera settings menu")

The Camera settings menu

| **Property** |  |   |  | **Description** |
| :--- | :--- | :--- | :--- | :--- |
|  |  |  | **Field of View** | The height of the Camera’s view angle. |
|  |  |  | **Dynamic Clipping** | Check this box to make Unity calculate the Camera’s near and**far clipping planes** relative to the**viewport** size of the Scene. |
|  |  |  | **Clipping Planes**  | The distances from the Camera where Unity starts and stops**rendering** GameObjects in the Scene. |
|  |  |  | **Near** | The closest point to the Camera that Unity renders GameObjects. |
|  |  |  | **Far** | The furthest point from the Camera that Unity renders GameObjects. |
|  |  |  | **Occlusion Culling**  | Check this box to enable occlusion culling in the Scene view. This prevents Unity from rendering GameObjects that the Camera cannot see because they are hidden behind other GameObjects. |
|  |  |  | **Camera Easing** | Check this box to make the Camera ease in and out of motion in the Scene view over the time set by**Duration**. This makes the Camera ease into motion when it starts moving \(instead of starting at full speed\), and ease out when it stops. |
|  |  |  | **Duration** | The length of time in seconds that it takes for the Camera to accelerate to its initial full speed, which is set by the**Camera Speed**. |
|  |  |  | **Camera Speed** | The current speed of the Camera in the Scene view. |
|  |  |  | **Min** | The minimum speed of the Camera in the Scene view. Valid values are between 0.01 and 98. |
|  |  |  | **Max** | The maximum speed of the Camera in the Scene view. Valid values are between 0.02 and 99. |

**Tip**: To reset the properties to their default values, click the cog icon in the top right corner of the Camera settings menu and select**Reset**.

In[Flythrough mode](https://docs.unity3d.com/2019.2/Documentation/Manual/SceneViewNavigation.html#flythrough)  
, you can change the speed of the Camera while moving. To do this, use the mouse scroll wheel or drag two fingers on a trackpad.

You can also configure the Camera in script with the[SceneView.CameraSetting](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/SceneView.CameraSettings.html)API.

---

* 2019–02–08  Page published with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Scene view Camera Settings added in[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20191)




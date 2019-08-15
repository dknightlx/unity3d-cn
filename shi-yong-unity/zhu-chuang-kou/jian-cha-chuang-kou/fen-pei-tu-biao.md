# Assigning icons

Unity allows you to assign custom icons for**GameObjects**  
and**scripts**  
. These icons display in the**Scene view**  
, along with built-in icons for items such as Lights and**Cameras**  
. Use the[Gizmos menu](https://docs.unity3d.com/2019.2/Documentation/Manual/GizmosMenu.html)to control how icons are drawn in the**Scene**  
view.

### GameObject Select Icon button

To change the icon for a GameObject, select the GameObject in the Heirarchy window or Scene view, then click the**Select Icon**button \(the blue cube, highlighted with a red square in the image below\) in the**Inspector**  
window to the left of the GameObject’s name.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconSelectorForGameObject.png "The GameObject Select Icon button \(here highlighted with a red square\) in the Inspector window")

The GameObject

**Select Icon**

button \(here highlighted with a red square\) in the Inspector window

When you assign an icon to a GameObject, the icon displays in the Scene view over that GameObject \(and any duplicates made afterwards\). You can also assign the icon to a**Prefab**  
to apply the icon to all instances of that**Prefab**in the Scene.

### Script Select Icon button

To assign a custom icon to a script, select the script in the Project window, then click the**Select Icon**button \(the C\# file icon, highlighted with a red square in the image below\) in the Inspector window to the left of the script’s name.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconSelectorForScript.png "The Script Select Icon button \(here highlighted with a red square\) in the Inspector window")

The Script

**Select Icon**

button \(here highlighted with a red square\) in the Inspector window

When you assign an icon to a script, the icon displays in the Scene view over any GameObject which has that script attached.

## The Select Icon menu

Whether you are assigning an icon to a GameObject or a Script, the pop-up**Select Icon**menu is the same:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconSelectorPopup.png)

The**Select Icon**menu has built-in icons. Click on an icon to select it, or click**Other…**to select an image from your project Assets to use as the icon.

The built-in icons fall into two categories:**label icons**and**image-only icons**.

**Label icons**

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/LabelIcons.png)

Assign a label icon to a GameObject or script to display the name of the GameObject in the Scene view.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconLabel.jpg "A GameObject with a label icon assigned")

A GameObject with a label icon assigned

**Image-only icons**

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/ImageOnlyIcons.png)

Image-only icons do not show the GameObject’s name. These are useful for assigning to GameObjects that may not have a visual representation \(for example, navigation waypoints\). With an icon assigned, you can see and click on in it the Scene view to select and move an otherwise invisible GameObject.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconsAssignedToInvisibleGameObjects.jpg "A yellow diamond icon assigned to multiple invisible GameObjects")

A yellow diamond icon assigned to multiple invisible GameObjects

Any Asset image in your project can also be used as an icon. For example, a skull and crossbones icon could be used to indicate danger areas in your level.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/IconCustomAssignedToScript.jpg "A skull and crossbones image has been assigned to a script. The icon is displayed over any GameObjects which have that script attached.")

A skull and crossbones image has been assigned to a script. The icon is displayed over any GameObjects which have that script attached.

**Note:**When an Asset’s icon is changed, the Asset itself is marked as modified and therefore picked up by**version control**  
systems.


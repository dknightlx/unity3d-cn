# Installing the Unity Hub

The Unity Hub is a management tool that you can use to manage all of your Unity Projects and installations. Use the Hub to manage multiple installations of the Unity Editor along with their associated components, create new Projects, and open existing Projects.

* To install the Unity Hub for macOS or Windows, visit
  [Download Unity](https://unity3d.com/get-unity/download)
  on the Unity website.
* To install the Unity Hub on Linux, visit
  [Download Unity Hub for Linux](https://forum.unity.com/threads/unity-hub-v-1-0-0-is-now-available.555547/)
  on the Unity Forums.

To install and use the Unity Editor, you must have a Unity Developer Network \(UDN\) account. If you already have an account, sign in, choose your licenses type, and proceed to the[Installing the Unity Editor](https://docs.unity3d.com/2019.2/Documentation/Manual/GettingStartedInstallingHub.html#install)section.

If you do not have an account, follow the prompts to create one. You can choose to create a Unity ID or use one of the social sign-ins. For more information on accounts and subscriptions, see[Unity Organizations](https://docs.unity3d.com/2019.2/Documentation/Manual/OrgsUnityOrganizations.html).

## Installing the Unity Editor

To install the Editor:

1. Click the**Installs**tab. The default install locations are:

   Windows:

   ```
   C:\Program Files\Unity\Hub\Editor
   ```

   Mac:

   ```
   /Applications/Unity/Hub/Editor
   ```

   1. Optionally, to change the default installation location, click the Gear icon.![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/gs_gear_icon.png "Gear icon")

   2. In the**Editor Folder Location**dialog box, enter the new installation location and click**Done**.

2. Click the**Add**button and select a specific version of the Editor.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/gs_hub_installs_screen.png "Hub install screen")  
   Hub install screen

3. Click the**Next**button and select the modules you want to install with the Editor. If you don’t install a component now, you can add it later if you need to. When you’ve selected all the modules you need, click**Done**.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/gs_choose_components.png "Modules install")  
   Modules install

If you are installing multiple Editor versions, the first installation starts as soon as the download is complete. Other selected versions download simultaneously and queue to start when the current installation finishes.

The Hub displays the installation location of each Editor under the corresponding version label.

To add modules to an Editor, locate its files, or uninstall it, click the three dots next to that Editor version.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/gs_hub_installs_screen2.png "Modifying an existing Editor install")

Modifying an existing Editor install

## Adding existing instances of the Editor to the Hub

You can add instances of the Editor to the Hub that you installed outside of the Hub.

1. Click the**Installs**tab.

2. Click the**Locate**button to find existing installations of the Editor.

3. In the file dialog, navigate to the location of the Editor installation and select the Unity executable. On MacOS this is_Unity.app_. On Windows this is_Unity.exe_.

   On macOS, the typical location of the\_Unity.app\_is:

   ```
   /Applications/Unity/Hub/Editor/
   &
   lt;version
   &
   gt;/Unity.app
   ```

   On Windows, the typical location of the\_Unity.exe\_is:

   ```
   C:\Program Files\Unity\Editor\Unity.exe
   ```

   Or

   ```
   C:\Program Files\Unity
   &
   lt;version
   &
   gt;\Editor\Unity.exe
   ```

4. Click the**Select Editor**button.

To remove the Editor from the Hub, click the three dots next to the Editor version. Removing an Editor that you added in this manner does not uninstall it or modify it in any way.

## Support for Editor versions prior to 2017.1

Sign-in status is not shared for pre–2017.1 versions of the Editor opened through the Hub. Performing tasks such as**Manage License**,**Open Project**,**Create Project**, and**Sign in**opens the Unity Launcher instead of the Hub.

If you attempt to use the Unity Hub to open an Editor version 5 or earlier and you do not have an appropriate license file, the Editor will hang on the splash screen.

To avoid this issue, run the Editor directly, external to the Unity Hub, and the Editor will load correctly even if the license file is not detected.

## Using the Unity Installer to install the Unity Editor

The Unity installer is a small executable program \(approximately 1 MB in size\) that lets you select which components of the Unity Editor you want to download and install.

To install previous versions of the Unity Editor using the Installer, visit the[Unity download archive](https://unity3d.com/get-unity/download/archive). The archive page provides Unity Installer download links for all released versions of the Editor.

For additional information on installing the Editor using the Installer, see the 2018.3 version of the[Unity Manual](http://docs.unity3d.com/).

---

* 2018–12–19  Page amended with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* 2018–06–12 Page published with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* Hub design updated in Unity[2019.1](https://docs.unity3d.com/2019.1/Documentation/Manual/30_search.html?q=newin20191)




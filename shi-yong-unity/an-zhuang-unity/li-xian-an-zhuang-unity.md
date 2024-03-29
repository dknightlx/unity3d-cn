# Installing Unity offline without the Hub

The Unity Download Assistant supports offline deployment. This allows you to download all the necessary files for installing Unity, and to generate a script for repeating the same installation on other computers without internet access.

## Preparation

Run the Download Assistant, and install Unity as normal on one computer. This computer must have enough free disk space to download all the files. Click the dropdown and select**Custom**, then choose the location you wish to download the files to.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/DeployingUnityOffline-DownloadAssistant.png)

## Check you have everything you need

Open your PC’s file manager, navigate to the custom location folder you specified earlier, and look for the`.sh`or`.bat`file inside that folder. Check the contents of this file. It should look similar to the following example:

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/DeployingUnityOffline-installsh.png)

## Deploying Unity to other computers

### Windows

1. Copy the entire folder to the target Windows PC, and run the supplied
   `.bat`
   file.
2. To avoid the Windows UAC prompt, run
   `install.bat`
   from the Administrator shell. In the
   **Start**
   menu, search for
   `cmd.exe`
   , right-click, and select
   **Run as administrator**
   .
3. Navigate to the folder with the
   **scripts**

 

   . This will usually be in your Downloads folder \(
   `cd C:\Users\[YourName]\Download\UnityPackages`
   \).

### Mac

1. Copy the entire folder to the target Mac OS X machine, and run the supplied
   `.sh`
   file. Run
   `sudo install.sh`
   .
2. Navigate to the folder with the scripts. This will usually be in your Downloads folder \(
   `cd ~/Downloads/UnityPackages`
   \).
3. You can repeat these instructions as many times as you need to for each computer you wish to install Unity on.




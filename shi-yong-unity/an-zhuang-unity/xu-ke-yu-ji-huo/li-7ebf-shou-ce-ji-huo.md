# Offline / Manual Activation

Online activation usually fails when Unity cannot contact the license server. This might be because you don’t have access to the internet, your firewall or proxy settings are blocking the connection, or the Unity license servers are down. For more information on why this can happen, see[Troubleshooting](https://docs.unity3d.com/2019.2/Documentation/Manual/ManualActivationGuide.html#Troubleshooting), below.

When online activation fails, the Unity Editor automatically attempts to perform a manual activation. This page provides step-by-step instructions to manually activate Unity on your machine.**You still need access to a machine with internet access**, but it does not have to be the machine on which you are trying to activate Unity.

This documentation assumes you have already downloaded and installed Unity. To download Unity, you need an internet connection. Go to[Download Unity](https://unity3d.com/get-unity/download)to get the latest version. If you’re not sure which type of license you need, go to the[Unity Store](https://store.unity.com/)and view comparisons for Unity Personal, Plus and Pro.

## Step 1: Get a license request file

1. Open Unity. When Unity cannot contact the license server, it displays a message in the License Management window that says “No network connection”.![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/communicationProblem.png)

2. Click**Manual Activation**.

3. Click**Save License Request**.![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/wouldYouLikeToSave.png)

4. Save the file in a directory of your choice. Make sure you remember where you save the file. When you click**Save**, Unity displays a notification that reads “License request file saved successfully”.

This license request file is tied to the machine you used to generate it. This license file does not work on any other machine, and will not recognise the machine if you reformat it or make certain hardware changes.

## Step 2: Request a license

Now that you have your license request file, the next steps require internet access. If your machine does not have internet access, you can activate your license on a machine that does have access by copying the file to the other machine, activating the license using the following steps, and then copying the file back to your machine to use Unity.

1. Go to the[Unity license Manual Activation webpage](https://license.unity3d.com/). Click the**Browse**button, choose the license request file that you created in step 1, then click**Next**

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/manualactivationwindow.png)

2. Select the type of license you want to activate.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/activateyourlicense.png)

3. Enter the serial number, then click**Next**.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/manualActivation.png "Note: In this window the serial number has been hidden.")
   Note: In this window the serial number has been hidden.

4. Click**Download license file**.

   ![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/youAreAlmostDone.png)

This downloads your license to the machine you’re using to browse the website. If you’re activating Unity on a different machine to the one that has internet acces, remember to transfer the license to the machine you want to activate Unity on.

Some browsers append “.xml” to the license file name. If this is the case, you need to delete this from the file name before you load the license file into Unity.

## Step 3: Activate your licence

Now that you have your licence file, you can activate your Unity account.

Open Unity again and return to the License Management page.

![](https://docs.unity3d.com/2019.2/Documentation/uploads/Main/loadLicense.png)

Click**Load License**, and choose the license request file that you downloaded in step 2. If the license loads successfully, Unity displays a “Thank you!” message. Click**Start Using Unity**to continue.



## Troubleshooting

If you encounter any error codes or other problems during the activation process, they might be caused by the following issues:

* Your machine might not have internet access. In this case, you might need to manually activate your licence. You can find instructions on how to do this in the
  [Manual Activation](https://docs.unity3d.com/2019.2/Documentation/Manual/ManualActivationGuide.html)
  documentation.
* Your firewall/proxy or internet security settings might be blocking Unity from sending and receiving data about your license file.
* You might not have the correct read/write privileges on your machine to save the license file. To solve this you might need to give these permissions to the user account your are using to attempt the licence activation. This is a particularly common problem in workplaces and schools; contact your IT administrator to find out whether there are restrictions in place that might prevent the activation process from working correctly.
* Major operating system changes or updates might affect your machine’s ID, which causes your licence to stop recognizing your machine. See the Unity Knowledge Base article
  [I Have Just Updated/Installed A New Operating System. Why Is My License Failing To Activate?](https://support.unity3d.com/hc/en-us/articles/205698949-I-have-just-updated-installed-a-new-Operating-System-Why-is-my-license-failing-to-activate-)
* Unity’s license servers might be down. See the
  [Unity Cloud System Status Page](https://status.cloud.unity3d.com/)
  for status updates on the all Unity servers.

For information on all potential errors and how to resolve them, see the[Unity Support Knowledge Base](https://support.unity3d.com/hc/en-us/sections/202242003-Activations-and-Management). If you can’t find a solution, contact[Unity Customer Services](https://support.unity3d.com/hc/en-us/requests/new?ticket_form_id=65905)for more assistance.

---

* 2018–07–25 Page amended with[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* 2017–09–06 Page amended with limited[editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)

* License activation updated in Unity 2017.2

  



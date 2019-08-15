# Scripting API for packages

The Package Manager scripting API enables users to interact with the Package Manager programmatically. For example, you might want to install a specific package or version depending on the platform of the target machine.

At the heart of the system is the[PackageManager.Client](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Client.html)class which allows you to find packages, browse the list of packages, and install and uninstall packages through scripting.

Another important class is[PackageManager.PackageInfo](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.PackageInfo.html), which contains the state of a package, including metadata obtained from the**package manifest**  
and the registry. For example, you can get a[list of versions](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.VersionsInfo.html)available for the package, or the[list of any errors](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.PackageInfo-errors.html)produced while locating or installing the package.



## Adding a package to the Project

This example demonstrates how to use the[Client](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Client.html)class to install or add a package to the Project.

You can specify either the package name or the name with a specific version when calling the[Client.Add](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Client.Add.html)method. For example, using`Client.Add("com.unity.textmeshpro@1.3.0");`installs version 1.3.0 of the TextMesh Pro package, but using only`Client.Add("com.unity.textmeshpro")`installs \(or updates to\) the latest version of the package.

The**Client.Add**method returns an[AddRequest](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Requests.AddRequest.html)instance, which you can use to get the status, any errors, or a[Request](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Requests.Request_1.Result.html)response containing the[PackageInfo](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.PackageInfo.html)information for the newly added package.

```
using System;
using UnityEditor;
using UnityEditor.PackageManager.Requests;
using UnityEditor.PackageManager;
using UnityEngine;

namespace Unity.Editor.Example {
   static class AddPackageExample
   {
       static AddRequest Request;
      
       [MenuItem("Window/Add Package Example")]
       static void Add()
       {
           // Add a package to the Project
           Request = Client.Add("com.unity.textmeshpro");
           EditorApplication.update += Progress;
       }

       static void Progress()
       {
           if (Request.IsCompleted)
           {
               if (Request.Status == StatusCode.Success)
                   Debug.Log("Installed: " + Request.Result.packageId);
               else if (Request.Status 
>
= StatusCode.Failure)
                   Debug.Log(Request.Error.message);

               EditorApplication.update -= Progress;
           }
       }
   }
}

```



## Browsing the list of packages in a Project

This example demonstrates how to use the[Client](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Client.html)class to iterate over the packages in the Project.

The[Client.List](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Client.List.html)method returns a[ListRequest](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Requests.ListRequest.html)instance, which you can use to get the status, any errors, or a[Request](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.Requests.Request_1.Result.html)response containing the[PackageCollection](https://docs.unity3d.com/2019.2/Documentation/ScriptReference/PackageManager.PackageCollection.html)which you can iterate.

```
using System;
using UnityEditor;
using UnityEditor.PackageManager.Requests;
using UnityEditor.PackageManager;
using UnityEngine;

namespace Unity.Editor.Example {
   static class ListPackageExample
   {
       static ListRequest Request;
    
       [MenuItem("Window/List Package Example")]
       static void List()
       {
           Request = Client.List();    // List packages installed for the Project
           EditorApplication.update += Progress;
       }

       static void Progress()
       {
           if (Request.IsCompleted)
           {
               if (Request.Status == StatusCode.Success)
                   foreach (var package in Request.Result)
                       Debug.Log("Package name: " + package.name);
               else if (Request.Status 
>
= StatusCode.Failure)
                   Debug.Log(Request.Error.message);

               EditorApplication.update -= Progress;
           }
       }
   }
}

```

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




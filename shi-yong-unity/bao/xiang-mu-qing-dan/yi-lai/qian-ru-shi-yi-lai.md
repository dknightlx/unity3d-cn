# Embedded dependencies

Any package that appears under your Project’s`Packages`folder is**embedded**in that Project. Typically, when you create a new package, you embed it in your Project while you are developing it. When it is ready to be shared with other users and tested in other Projects, you can publish it to a[scoped package registry](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html).

Embedded packages do not need to appear in the**Project manifest**  
as a dependency. If they do, the package on disk takes precedence over the version of the package listed as a dependency. For example, if the**Project manifest**specifies a dependency on version 1.3.1 of Package X but the Project also has an**embedded package**  
with that name, the Package Manager uses the**embedded package**, regardless of its apparent version, instead of downloading the more recent version from the registry.

It is your responsibility to track the content of your embedded packages, and any changes you make to it. If your Unity Project is under source control, you should also add packages embedded in that Project to the same source control.

  



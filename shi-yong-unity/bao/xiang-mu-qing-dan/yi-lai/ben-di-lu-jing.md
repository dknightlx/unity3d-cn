# Local paths

You can specify a dependency as any local directory that contains a package. This feature is helpful for local offline development and testing. To set a local path through the**UI**  
, see[Installing a local package](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-local.html).

The path reference always begins with the`file:`prefix, and always uses forward slashes \(`/`\) for path separators.

You can use either absolute paths, or paths that are relative to the Project manifest root. In other words, a path preceded with two dots \(`..`\) refers to the root of the Project path \(for example,`<project path>/my-package`\).

For Windows absolute paths, the drive letter and its colon \(usually`C:`\) follows the`file:`prefix but is otherwise identical to Linux or MacOS paths.

## Example of an absolute path in Linux or macOS

```
{
  "dependencies": {
    "my_local_package": "file:/Users/johndoe/Packages/my_local_package"
  }
}

```

## Example of an absolute path in Windows

```
{
  "dependencies": {
    "my_local_package": "file:C:/Users/johndoe/Packages/my_local_package"
  }
}

```

## Example of a relative path

```
{
  "dependencies": {
    "my_local_package": "file:../test/my-test-package"
  }
}

```

  



# Dependencies

The**dependencies**attribute in the**Project manifest**  
is a JSON object that maps a package name to a version. The version number indicates which version of the package to download from the package registry. For example:

```
{
  "dependencies": {
    "com.my-package": "2.3.1",
    "com.my-other-package": "1.0.1-preview.1",
       etc.
  }
}

```

In addition to using[version numbers](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#pkg-ver), the Package Manager also supports adding Project dependencies with the following:

* [Embedded dependencies](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-embed.html)
* [Local paths](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-localpath.html)
* [Git URLs](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-git.html)

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




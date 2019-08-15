# Scoped package registries

A scoped registry allows you to use a registry in addition to the Unity default registry where you can host your own packages. Using scoped registries ensures that the Package Manager always maps a package to one and only one registry, guaranteeing a consistent result regardless of network conditions.

For example, if you set up your own server where you are hosting some of the Unity packages, you could end up getting the package from the wrong registry if one registry is temporarily unavailable, even if the Package Manager always searches the registries in the same order. However, if you set up a scoped registry for your own server, the package always maps to one and only one registry, guaranteeing a consistent result regardless of network conditions.

## Supported registry types

Unity Package Manager supports registries based on the**npm**protocol. You can use any off the shelf**npm**registry server and it should work, but[Verdaccio](https://www.npmjs.com/package/verdaccio)is quick to set up and doesn’t require a lot of configuration.

Once you set up these servers, you can include them as**scoped registries**, which is the[same concept that**npm**uses](https://docs.npmjs.com/creating-and-publishing-scoped-public-packages).

### Limitations

Some npm registry servers do not support searching all packages with the`/all`Web API route. The Package Manager Search API relies on configured scoped registries to support this old npm API protocol. It has an HTTP endpoint that returns the metadata of all published packages \(for example,`https://registry.my-company.com/-/all`\).

If you have a tool that uses the Package Manager API to list available packages, you might experience unexpected results if your registry does not support the old protocol. For example, in this case, the**Packages**window does not display packages from those scoped registries in the**All packages**tab. However, this limitation does not apply to package resolution, so you can still manually add packages from scoped registries to the**Project manifest**  
.

## Setting up a scoped registry

To set up your scoped registries in your Project manifest, use the[scopedRegistries](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html#scopedRegistries)attribute, which takes an array of scoped registry configuration objects. Each object contains a[name](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html#name), a[url](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html#url)location, and a list of[scopes](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-scoped.html#scopes)for each package name pattern you want to map to that scoped registry. When the Package Manager decides which registry to fetch a package from, it compares the package**name**to the**scopes**values and finds the registry whose**scopes**most closely match.

For example, in the Project manifest below, there are two scoped registries,**Main**and**Tools**:

```
{
  "scopedRegistries": [
    {
      "name": "Main",
      "url": "https://my.company.com/registry",
      "scopes": [
        "com.my-company", "com.my-company.tools.foo"
      ]
    },
    {
      "name": "Tools",
      "url": "https://my.company.com/tools-registry",
      "scopes": [
        "com.my-company.tools"
      ]
    }
  ],
  "dependencies": {
    "com.unity.cinemachine": "1.0.0",
    "com.unity.2d.common": "1.0.0",
    "com.unity.2d.animation": "1.0.0",
    "com.my-company.bar": "1.0.0"
  }
}


```

When a user requests the**com.my-company.bar**package, the Package Manager finds that the**com.my-company.\***namespace is the closest match to its name, and therefore fetches the package from the**Main**registry.

When a user requests the**com.my-company.tools.foo**package, the**Main**registry has a scope with a namespace that’s an exact match.

When a user requests the**com.my-company.tools.animation**package, the Package Manager finds that the**com.my-company.tools.\***namespace is the closest match to its name and therefore fetches the package from the**Tools**registry. Even though it also matches the**Main**scope, the**com.my-company.\***namespace is not as close a match.

When a user requests the**com.other-company.bar**package, the Package Manager doesn’t find a match in any of the scoped registries, and therefore fetches the package from the default registry.

### Configuration

Configure scoped registries with the[scopedRegistries](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPrj.html#scopedRegistries)attribute in the Project manifest. The**scopedRegistries**attribute contains an array of entries \(objects\) that represent all of the registries.

Each registry object contains a unique**name**, a location \(**url**\), and an array of namespaces, or**scopes**. The Package Manager uses the scopes to match package names to registries.

| **Attribute** | **JSON Type** | **Description** |
| :--- | :--- | :--- |
| **name** | String | The scope name as it appears in the user interface. The**Packages**window displays this name in the[package details view](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-ui-details.html). For example,`"name": "Tools"`. |
| **url** | String | The URL to the[npm-compatible registry](https://docs.google.com/document/d/1-PW4l1iXWXm9k8Pm4Rbw_8_wCLRoAmnPUPn3li_c7zk/edit#heading=h.vbo63iu5tkve). For example,`"url": "https://my.company.com/tools-registry"` |
| **scopes** | Array of Strings | Array of scopes that you can map to a package name, either as an exact match on the package name, or as a namespace.  For example,`"scopes": [ "com.my-company", "com.my-company.tools.foo" ]`  **NOTE**: This type of configuration assumes that packages follow the[Reverse domain name notation](https://en.wikipedia.org/wiki/Reverse_domain_name_notation). This ensures that**com.unity**is equivalent to**com.unity.\***. |

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




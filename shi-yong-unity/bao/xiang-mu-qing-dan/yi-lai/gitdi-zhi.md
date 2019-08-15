# Git URLs

When the Package Manager fetches a package from a Git repository, it adds the package locally to your Project. This allows you to easily test unpublished changes, but you cannot use it to contribute to that Git repository. To set up an existing local Git repository as a dependency in your Project, use[a local path](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-localpath.html)instead.

To use**Git packages**  
in a Project, make sure the[Git client](https://git-scm.com/)is installed on your machine and that you have added the Git executable path to the PATH system environment variable.

If the repository tracks files with[Git LFS](https://git-lfs.github.com/), make sure the Git LFS client is also installed on your machine. If it is not installed, the Package Manager can’t retrieve the files stored on the LFS server and instead checks out the LFS pointer files without any error or warning messages.

**NOTE**: You cannot use the**Packages**window to install a package directly from a Git repository. You must edit the**Project manifest**  
to add a Git URLs as a dependency.

To specify a Git URL as a dependency, add the name of the package to install with a Git URL instead of the version number or local file path. For example, this demonstrates how to specify a remote Git using the recommended HTTPS protocol:

```
{
  "dependencies": {
    "com.mycompany.mypackage": "https://mycompany.github.com/gitproject/com.mycompany.mypackage.git"
}

```

The Package Manager supports the**https**,**http**,[**ssh**](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-git.html#Git-SSH),**git**, and[**file**](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-git.html#Git-FILE)protocols using this form:

```
<
protocol
>
://[
<
user
>
[:
<
password
>
]@]
<
host
>
[:
<
port
>
]/
<
path
>
.git[#
<
revision
>
]

```

You can also skip the`.git`path suffix if the URL starts with git in these forms:

```
  git://[
<
user
>
[:
<
password
>
]@]
<
host
>
[:
<
port
>
]/
<
path
>
[#
<
revision
>
]

```

or:

```
  git+
<
protocol
>
://[
<
user
>
[:
<
password
>
]@]
<
host
>
[:
<
port
>
]/
<
path
>
[#
<
revision
>
]

```

You might need to[configure credentials in Git configuration files](https://git-scm.com/docs/gitcredentials)in order to provide your username and password securely. This is preferable to hard-coding them in the Git URL, which is a major security issue if the Project is shared with others.

Git uses the keys at the default location when you use SSH to authenticate. However, if you are using[PuTTY](https://www.putty.org/)as the SSH client on Windows, you might need to configure the**GIT\_SSH**environment variable to make it point to`plink.exe`.

You need to set up SSH keys outside of Unity. The Editor notifies you of authentication failure if you don’t have proper access.

For more information on setting up authentication for a specific host, see the help pages for[GitLab](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html)and[GitHub](https://github.com/settings/tokens).

## Targeting a specific revision

You can specify any revision to install. A revision is an expression that eventually resolves to a commit hash in Git. The most common types of revisions are commit hashes, tags, and branches.

To target a specific revision, append the following to the Git URL in the**dependencies**attribute:**\#**followed by the revision \(either the[version](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-manifestPkg.html#pkg-ver)or a specific Git hash\). Specifying the hash ensures that you get exactly the version you want. For example:

```
{
  "dependencies": {
    "com.mycompany.mypackage": "https://mycompany.github.com/gitproject/com.mycompany.mypackage.git#523c4f291cea796141e7211f4951702984d2e9ca"
  }
}

```

If the revision omitted, the Package Manager uses the remote repository’s`HEAD`revision.

For more information about setting a proper revision, see the[Git user manual section on Git revisions](https://www.git-scm.com/docs/gitrevisions).



## Using the SSH protocol

If you want to use the**ssh**protocol, make sure you use the full protocol syntax. The Package Manager does not support SCP-based shorthand syntax, and many Git hosting services supply the repository’s URL with the SCP syntax. So if you are copying the URL directly, make sure you use the`ssh://`protocol and replace the colon \(`:`\) before the repository path with a slash \(`/`\). For example, if you get`git@mycompany.github.com:gitproject/com.mycompany.mypackage.git`from a GitHub repository, make sure you change it to the full syntax, as shown in this example:

```
{
  "dependencies": {
    "com.mycompany.mypackage": "ssh://git@mycompany.github.com/gitproject/com.mycompany.mypackage.git"
}

```

**NOTE**: If you set up your SSH key with a passphrase, the Package Manager can’t retrieve the package, because you need to enter the passphrase in a shell or command line. In this case, consider using the**https**protocol instead, or use the[ssh-add](http://man7.org/linux/man-pages/man1/ssh-add.1.html)utility shipped with Git. For more information, see[Authentication issues with Git URLs](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-errors.html#ssh-add).



## Using the FILE protocol

The Package Manager does not support file paths with the**file**prefix, but it does support full URLs with the**file**protocol. For example:

```
{
  "dependencies": {
    "com.mycompany.mypackageA": "file://localhost/absolute/path/to/com.mycompany.mypackageA.git",
    "com.mycompany.mypackageB": "file:///absolute/path/to/other/com.mycompany.mypackageB.git"
  }
}
```




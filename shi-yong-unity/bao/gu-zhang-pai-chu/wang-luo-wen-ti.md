# Network issues

* [Configuring your firewall](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#Firewall)
* [Configuring your proxy server](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#Proxy)



## Configuring your firewall

Make sure the Unity Package Manager can access the following domain names using HTTPS:

* packages.unity.com
* download.packages.unity.com
* dl.bintray.com
* api.bintray.com
* akamai.bintray.com
* upm-cdn.unity.com \(or upm-cdn-china.unitychina.cn for locations in China\)

Add the above domain names to your firewall’s whitelist.



## Configuring your proxy server

When using a proxy server, configure the`HTTP_PROXY`and`HTTPS_PROXY`environment variables for the Unity Package Manager to use when performing requests against the Unity package registry.

You can set these variables globally \(either system or user variables\) according to your operating system. Alternatively, you can[set them only for the Unity Hub](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#Hub)when it launches.

For environments where you are behind a firewall, you can configure SSL certificate authorities for[self-signed certificates](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#SSL).



### Self-signed certificates

In some corporations and institutions, users are behind a firewall and can only access the internet through a proxy. Some proxies unpack the HTTPS content and repack it with its own self-signed certificate. Unity Package Manager’s underlying HTTPS layer rejects these self-signed certificates because it does not recognize them, and treats the connection as a possible man-in-the-middle attack. This means that you can’t use many features in Unity, including the Package Manager, unless you configure additional SSL certificate authorities to whitelist these certificates.

To configure additional SSL certificate authorities:

1. Create a text file with one or more custom certificate authorities. The file should consist of one or more trusted certificates in the[Privacy-Enhanced Mail](https://en.wikipedia.org/wiki/Privacy-Enhanced_Mail)\(PEM\) format. For example:

   ```
   -----BEGIN CERTIFICATE-----
   MIIC+zCCAeOgAwIBAgIJAO0U6hVJnbvjMA0GCSqGSIb3DQEBBQUAMBQxEjAQBgNV
   BAMMCWxvY2FsaG9zdDAeFw0xOTAzMTIwMTIxMzRaFw0yOTAzMDkwMTIxMzRaMBQx
   EjAQBgNVBAMMCWxvY2FsaG9zdDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoC
   ggEBAKNh0EM7j57pXorGs5OHzlk9TYeUqITtXXdWfY1fbqRdj+a8qLNs4m/nDsDW
   KgibHYG3FUqIidjPL61DLQuWUPY9Zo+uQaccIe0E5wb+To9mwMlLuhMD6iCPFRpe
   jcDhNj4vG1RVARMO1jupeZqdb+xHBZqtmMJmtiDOBxt662Z4hvoH8mdqNEuSkozz
   HqXmcdigrTO37DspGRBx08GJlHFHUs7C+hYOsOdNjME3dH/8uihjKYiqQb1E12dN
   PNL7jYm3AZv+qUmDFM3BJE0hSmAP00GuTJxbe31Kh4e7N5/XSiLsnqwircOj/Hfi
   eWjtsoXbCNDIiWUQtXBeLD/BdvkCAwEAAaNQME4wHQYDVR0OBBYEFDFw8VDkgMne
   mDjgo+b1iaPfUkdVMB8GA1UdIwQYMBaAFDFw8VDkgMnemDjgo+b1iaPfUkdVMAwG
   A1UdEwQFMAMBAf8wDQYJKoZIhvcNAQEFBQADggEBAFEjUWGz1r3xSsbwUJsRhbMc
   M7Jjf9/r833H7eq31mbl/JbXPnpo8IctMuWyw42ccMtgq7i+coQeKwvWnHtI5rhe
   vshEkIqNPAoCnpW5NLprYDDTG1PDEhv6FYpW8Alq65i03tptzaoHlH3sH+97E/h0
   qSYI7yNHWMC5u0r1DB0BR+lZsj6RnwWPySMSuXx5sSiKIS/HkkMVwwmxKa4ZwuwS
   LFwHSUdqk0lJK4b0mCwyTHNvYO1IDziE5EKwfuaKVgOa62iCHVahgIVa+een4EfS
   hCCr3M3cq11Mi+mnRi1scxxrOno4OEEChWg2szZLlxBrkVJllrrq620XJ6RLB/8=
   -----END CERTIFICATE-----
   -----BEGIN CERTIFICATE-----
   MIIDtzCCAp+gAwIBAgIQDOfg5RfYRv6P5WD8G/AwOTANBgkqhkiG9w0BAQUFADBl
   MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
   d3cuZGlnaWNlcnQuY29tMSQwIgYDVQQDExtEaWdpQ2VydCBBc3N1cmVkIElEIFJv
   b3QgQ0EwHhcNMDYxMTEwMDAwMDAwWhcNMzExMTEwMDAwMDAwWjBlMQswCQYDVQQG
   EwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3d3cuZGlnaWNl
   cnQuY29tMSQwIgYDVQQDExtEaWdpQ2VydCBBc3N1cmVkIElEIFJvb3QgQ0EwggEi
   MA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCtDhXO5EOAXLGH87dg+XESpa7c
   JpSIqvTO9SA5KFhgDPiA2qkVlTJhPLWxKISKityfCgyDF3qPkKyK53lTXDGEKvYP
   mDI2dsze3Tyoou9q+yHyUmHfnyDXH+Kx2f4YZNISW1/5WBg1vEfNoTb5a3/UsDg+
   wRvDjDPZ2C8Y/igPs6eD1sNuRMBhNZYW/lmci3Zt1/GiSw0r/wty2p5g0I6QNcZ4
   VYcgoc/lbQrISXwxmDNsIumH0DJaoroTghHtORedmTpyoeb6pNnVFzF1roV9Iq4/
   AUaG9ih5yLHa5FcXxH4cDrC0kqZWs72yl+2qp/C3xag/lRbQ/6GW6whfGHdPAgMB
   AAGjYzBhMA4GA1UdDwEB/wQEAwIBhjAPBgNVHRMBAf8EBTADAQH/MB0GA1UdDgQW
   BBRF66Kv9JLLgjEtUYunpyGd823IDzAfBgNVHSMEGDAWgBRF66Kv9JLLgjEtUYun
   pyGd823IDzANBgkqhkiG9w0BAQUFAAOCAQEAog683+Lt8ONyc3pklL/3cmbYMuRC
   dWKuh+vy1dneVrOfzM4UKLkNl2BcEkxY5NM9g0lFWJc1aRqoR+pWxnmrEthngYTf
   fwk8lOa4JiwgvT2zKIn3X/8i4peEH+ll74fg38FnSbNd67IJKusm7Xi+fT8r87cm
   NW1fiQG2SVufAQWbqz0lwcy2f8Lxb4bG+mRo64EtlOtCt/qMHt1i8b5QZ7dsvfPx
   H2sMNgcWfzd8qVttevESRmCD1ycEvkvOl77DZypoEd+A5wwzZr8TDRRu838fYxAe
   +o0bJW1sj6W3YQGx0qMmoRBxna3iw/nDmVG3KwcIzi7mULKn+gpFL6Lw8g==
   -----END CERTIFICATE-----

   ```

2. Put this file in the same location as`upm-config.json`if possible, although Unity supports any location on the file system.

3. Create an empty JSON file named`upm-config.json`in the system-level Unity configuration folder:

   * Windows:
     `%ALLUSERSPROFILE%Unity/config`
   * macOS:
     `/Library/Application Support/Unity/config`
   * Linux:
     `/usr/share/unity3d/config`

4. In the`upm-config.json`file, add the**caFile**attribute set to the absolute file path for your PEM file. For example:

   ```
   {
     "caFile": "C:\\ProgramData\\Unity\\config\\cert.pem"
   }

   ```



### Setting environment variables for the Unity Hub

This section provides instructions for creating a command file you can run from a[Windows command prompt](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#Windows)or a[macOS or Linux terminal](https://docs.unity3d.com/2019.2/Documentation/Manual/upm-network.html#MacOS). Alternatively, you can copy and paste the commands directly into the prompt or terminal window.

**NOTE:**Before you run the command file, shut down the Hub completely. If the Hub is already running, the script switches focus to the Hub without relaunching, so it does not apply the changed proxy settings.



#### Windows

These instructions create a command file on Windows.

The file launches the Hub with the environment variables set. You can either double-click the file, or invoke it from the command prompt. Unity passes these environment variables on to any Unity Editor process launched from the Hub.

1. Open a text editor such as Notepad.

2. Enter the following text, replacing**proxy-url**with the correct proxy server URL and adjusting the Hub install path if needed:

   ```
   @echo off
   set HTTP_PROXY=proxy-url
   set HTTPS_PROXY=proxy-url
   start "" "C:\Program Files\Unity Hub\Unity Hub.exe"
    

   ```

   **NOTE:**If there are spaces in the path, you must use double quotes around the path to the program.

3. Save the file to a location where you can easily find it \(such as the`Desktop`\), and make sure the file has the`.cmd`\(for example,`launchUnityHub.cmd`\).



#### macOS

These instructions create the`launchUnityHub.command`file on macOS.

The file launches the Hub with the environment variables set. You can either double-click the file, or invoke it from a Bash terminal. Unity passes these environment variables on to any Unity Editor process launched from the Hub.

**NOTE:**Double-clicking the command file opens a Terminal window or tab and leaves it open, even after the script finishes. You can change this behavior in the preferences for the**Terminal.app**.

1. Open a Terminal window.

2. Enter the following script, replacing**proxy-url**with the correct proxy server URL and adjusting the Hub install path if needed:

   ```
   echo '#!/bin/bash
   export HTTP_PROXY=proxy-url
   export HTTPS_PROXY=proxy-url
   nohup "/Applications/Unity Hub.app/Contents/MacOS/Unity Hub" 
   &
   >
   /dev
   ull 
   &
   ' 
   >
    launchUnityHub.command
   chmod +x launchUnityHub.command

   ```

   **NOTE:**If there are spaces in the path, you must use double quotes around the path to the program.

3. Move the`launchUnityHub.command`file to a convenient location \(for example, the`Desktop`\), if you prefer.

---

* 2019–04–11 Page published with
  [editorial review](https://docs.unity3d.com/2019.2/Documentation/Manual/DocumentationEditorialReview.html)




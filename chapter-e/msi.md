## How to Generate an MSI

1. Install [WiX 3.9](https://wix.codeplex.com/releases/view/136891) from the official website.
2. Add WiX's bin folder to your PATH. ([Here's how](https://msdn.microsoft.com/en-us/library/gg513936.aspx))
3. Download and Install the latest public release of Stencyl. 
4. [Download this ZIP](http://static.stencyl.com/edukit/Stencyl-MSI-Generator-3.zip). It contains a WiX project for generating an MSI. Unzip it.
5. Then, copy the contents of your Stencyl install to that that folder under a folder called **dist**.
6. From the command line, cd to the WiX project's folder and run **generate_installer.bat**

If all goes well, an MSI will pop up after some time (5-10 minutes).

If it fails, please [contact us via e-mail](http://www.stencyl.com/about/contact/).


## Specifying a Default Username / Password

Do the following.

1. Open up **installer/src/Core.wxs** in a text editor.
2. Locate the following lines.

  ```
  <RegistryValue Type='string' Name='global.default.user' Value='[DEFAULTUSERNAME]'/>
  <RegistryValue Type='string' Name='global.default.password' Value='[DEFAULTPASSWORD]'/>
  ```

3. Replace **[DEFAULTUSERNAME]** with your Stencyl account name. (the username, not the e-mail)
4. Replace **[DEFAULTPASSWORD]** with your password, with sha1() applied to it.
5. Save the file.
6. Rebuild the MSI (step 6 above).

> If you don't trust web-based SHA1 generators, you can download [this utility from Microsoft](https://support.microsoft.com/en-us/kb/841290) and generate it yourself.

> `FCIV -sha1 path\to\file\holding\password`

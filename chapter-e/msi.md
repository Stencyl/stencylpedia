## Creating an MSI Installer for Stencyl

We are providing these instructions to [schools](http://www.stencyl.com/education/pricing/) that wish to deploy Stencyl over a network using an MSI installer.


## How To: Generating an MSI

At this time, you must build the MSI installer yourself described below. We do not provide a pre-built MSI at this time.

1. Install [WiX 3.9](https://wix.codeplex.com/releases/view/136891) from the official website.
2. Add WiX's bin folder to your PATH. ([Here's how](https://msdn.microsoft.com/en-us/library/gg513936.aspx))
3. Download and Install the latest [public release](http://www.stencyl.com/download/) of Stencyl. 
4. [Download this ZIP package](http://static.stencyl.com/edukit/Stencyl-MSI-Generator-3.zip). It contains a WiX project for generating an MSI. Unzip it.
5. Copy the contents of your Stencyl install to the subfolder (inside the unpacked ZIP package) called **dist**.
6. From the command line, cd to the WiX project's folder and run **generate_installer.bat**

If all goes well, an MSI will pop up after some time - usually within 5 - 10 minutes.

If building the MSI fails, please [contact us via e-mail](http://www.stencyl.com/about/contact/).


## How To: Setting Properties

One key purpose of an MSI is to automate installation across many computers. In order to fully automate the installation process, you will want your ActiveDirectory administrator to set the following properties using [msiexec](http://stackoverflow.com/questions/458857/how-to-make-better-use-of-msi-files) or [Orca](http://support.microsoft.com/kb/255905).

#### The Properties

Here are the properties you can configure prior to installation. 

Property Name | Description | Required?
--- | --- | ---
**DEFAULTUSERNAME** | Your school's Stencyl username | Yes
**DEFAULTPASSWORD** | The *SHA1 hash* of the account's password (visit [this page](http://www.stencyl.com/users/hashForm) to get it) | Yes
**INSTALLDIR** | Installation directory | Optional but recommended
WORKDIRECTORYROOT | The default working directory (including the ending backslash); this is optional -- otherwise, the roaming directory will be used | No
USEUSER | A boolean ("true"/"false") to tell Stencyl whether or not to append the Windows user's login name to the workspace path above; this way, every user can have his or her own workspace (e.g., \\share\students\stencyl\johndoe) | No
PROXYUSERNAME | Username for your proxy | No
PROXYPASSWORD | Password for your proxy | No
PROXYHOST | IP address/hostname for your proxy | No
PROXYPORT | Port for your proxy | No

#### Example: Setting a Username and Password

Suppose that our username is **ImaginaryAcademy** and our password is **password** -- which in turn is **5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8** when put into our [sha1() generator](http://www.stencyl.com/users/hashForm).

This is what you'd run in msiexec.

```
msiexec /I Stencyl.msi DEFAULTUSERNAME="ImaginaryAcademy" DEFAULTPASSWORD="5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"
```


## Customizing the Installer (Alernate Approach)

> We **strongly** recommend setting properties as described in the pervious section. If you don't wish to use the properties approach, you can edit the installer source directly as described in the sections below.

#### Changing the Default Workspace Directory

1. Open up **installer/src/UI.wxs** in a text editor.
2. Locate the following line (Line 31)

  ```
  <Control Id="WorkspaceEdit" Type="Edit" X="45" Y="85" Width="220" Height="18" Property="WORKDIRECTORYROOT" Text="{80}" />
  ```

3. Add a **default** attribute to that XML element, with the value being the desired default path for the workspace. Like the following...

  ```
  <Control Id="WorkspaceEdit" Type="Edit" X="45" Y="85" Width="220" Height="18" Property="WORKDIRECTORYROOT" Text="{80}" default="DIRECTORYGOESHERE"/>
  ```

4. Save the file.
5. Rebuild the MSI (step 6 in the first section).


#### Specifying a Default Username / Password

1. Open up **installer/src/Ui.wxs** in a text editor.
2. Locate the following line (Line 7).

  ```
  <Control Id="NameEdit" Type="Edit" X="45" Y="85" Width="220" Height="18" Property="DEFAULTUSERNAME" Text="{80}" />
  ```

3. Add a **default** attribute to that XML element, with the value being your Stencyl account name. (the username, not the e-mail). Like the following...

  ```
  <Control Id="NameEdit" Type="Edit" X="45" Y="85" Width="220" Height="18" Property="DEFAULTUSERNAME" Text="{80}" default="YOURUSERNAME" />
  ```

4. Do the same thing with the following line (Line 9), which sets the default password. Note that the password you type in here should already have **sha1() hashing** applied to it. Visit [this page](http://www.stencyl.com/users/hashForm) to obtain this.

  ```
  <Control Id="PasswordEdit" Type="Edit" Password="yes" X="45" Y="122" Width="220" Height="18" Property="DEFAULTPASSWORD" Text="{80}" default="YOUR-HASHED-PASSWORD"/>
  ```

5. Save the file.

6. Rebuild the MSI (step 6 in the first section).


#### Specifying Proxy Details

Same process as described in the prior section. This time, look at lines 54, 56, 58 and 60. Add a default attribute to these XML elements and stick in the desired value into that.

```
<Control Id="NameEdit" Type="Edit" X="45" Y="85" Width="220" Height="18" Property="PROXYUSERNAME" Text="{80}" />
```

```
<Control Id="PasswordEdit" Type="Edit" Password="yes" X="45" Y="122" Width="220" Height="18" Property="PROXYPASSWORD" Text="{80}" />
```

```
<Control Id="HostEdit" Type="Edit" X="45" Y="159" Width="170" Height="18" Property="PROXYHOST" Text="{80}" />
```

```
<Control Id="PortEdit" Type="Edit" X="235" Y="159" Width="30" Height="18" Property="PROXYPORT" Text="{5}" />
```


## Creating an MSI Installer for Stencyl

We are providing these instructions to [schools](https://www.stencyl.com/education/pricing/) that wish to deploy Stencyl over a network using an MSI installer.


## How To: Generating an MSI

At this time, you must build the MSI installer yourself described below. We do not provide a pre-built MSI at this time.

1. Install [WiX 3.9](https://wix.codeplex.com/releases/view/136891) from the official website.
2. Add WiX's bin folder to your PATH. ([Here's how](https://msdn.microsoft.com/en-us/library/gg513936.aspx))
3. Download and Install the latest [public release](https://www.stencyl.com/download/) of Stencyl. 
4. [Download this ZIP package](https://static.stencyl.com/edukit/Stencyl-MSI-Generator-3.zip). It contains a WiX project for generating an MSI. Unzip it.
5. Copy the contents of your Stencyl install to the subfolder (inside the unpacked ZIP package) called **dist**.
6. From the command line, cd to the WiX project's folder and run **generate_installer.bat**

If all goes well, an MSI will pop up after some time - usually within 5 - 10 minutes.

If building the MSI fails, please [contact us via e-mail](https://www.stencyl.com/about/contact/).


## How To: Setting Properties

One key purpose of an MSI is to automate installation across many computers. In order to fully automate the installation process, you will want your ActiveDirectory administrator to set the following properties using [msiexec](https://stackoverflow.com/questions/458857/how-to-make-better-use-of-msi-files) or [Orca](https://docs.microsoft.com/en-us/windows/win32/msi/orca-exe).

#### The Properties

Here are the properties you can configure prior to installation. 

Property Name | Description | Required?
--- | --- | ---
**DEFAULTUSERNAME** | Your school's Stencyl username | Yes
**DEFAULTPASSWORD** | The *SHA1 hash* of the account's password (visit [this page](https://www.stencyl.com/users/hashForm) to get it) | Yes
**INSTALLDIR** | Installation directory | Optional but recommended
WORKDIRECTORYROOT | The default working directory (including the ending backslash); this is optional -- otherwise, the roaming directory will be used | No
USEUSER | A boolean ("true"/"false") to tell Stencyl whether or not to append the Windows user's login name to the workspace path above; this way, every user can have his or her own workspace (e.g., \\share\students\stencyl\johndoe) | No
PROXYUSERNAME | Username for your proxy | No
PROXYPASSWORD | Password for your proxy | No
PROXYHOST | IP address/hostname for your proxy | No
PROXYPORT | Port for your proxy | No
FORGEENABLED | A boolean ("true"/"false"). Set to "false" to disable access to StencylForge | No

#### Example: Setting a Username and Password

Suppose that our username is **ImaginaryAcademy** and our password is **password** -- which in turn is **5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8** when put into our [sha1() generator](https://www.stencyl.com/users/hashForm).

This is what you'd run in msiexec.

```
msiexec /I Stencyl.msi DEFAULTUSERNAME="ImaginaryAcademy" DEFAULTPASSWORD="5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"
```

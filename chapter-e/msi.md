## How to Generate an MSI

1. Install [WiX 3.9](https://wix.codeplex.com/releases/view/136891) from the official website.
2. Add WiX's bin folder to your PATH. ([Here's how](https://msdn.microsoft.com/en-us/library/gg513936.aspx))
3. Download and Install the latest public release of Stencyl. 
4. [Download this ZIP](http://static.stencyl.com/edukit/Stencyl-MSI-Generator-3.zip). It contains a WiX project for generating an MSI. Unzip it.
5. Then, copy the contents of your Stencyl install to that that folder under a folder called **dist**.
6. From the command line, cd to the WiX project's folder and run **generate_installer.bat**

If all goes well, an MSI will pop up after some time (5-10 minutes).

If it fails, please contact us via e-mail.

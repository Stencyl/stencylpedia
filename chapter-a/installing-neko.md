## What is Neko VM?

Neko VM is an important part of the Haxe toolkit, which Stencyl uses to build games. Due to macOS security restrictions, we cannot run neko without installing it.


## How to install Neko (with Stencyl 3.4)

The first time that you try to test a game, if Stencyl doesn't detect that Neko is installed, it will ask you to enter your system password and install Neko for you.

1. Make sure you're logged in to an admin account. The account must be password-protected.

   * If you don't have access to an admin account, ask the system administrator for help.
   
   * If your admin account doesn't have a password, Stencyl can't obtain the necessary permissions to install Neko. Add a password to the account.
   
2. Open Stencyl and try to test a game.

3. Enter the password for the currently logged-in admin account and press "OK".


## Troubleshooting

If you have a previous neko install which is broken or a wrong version, make sure to remove that first.

```
osascript -e "do shell script \"
rm -rf /usr/local/lib/neko
rm /usr/local/lib/libneko.dylib
rm /usr/local/bin/neko
rm /usr/local/bin/nekoc
rm /usr/local/bin/nekotools
\" with administrator privileges"
```

Make sure your `/usr/local` permissions are correct.

```
osascript -e "do shell script \"
chmod 755 /usr/local/lib
chmod 755 /usr/local/bin
\" with administrator privileges"
```

If Neko still fails to install, ask on the forum for help.

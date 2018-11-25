# Ubuntu-ARM64-RPi
An Ubuntu 18.10 image for the Raspberry Pi 3 built upon the standard Ubuntu ARM64 base.

This is a minimal Ubuntu 18.10 image for the Raspberry Pi 3 (as well as the Pi 2 Rev 1.2). It does not come with a desktop environment preinstalled, so you must install one manually if you want a GUI.

You can either install lubuntu-desktop, xubuntu-desktop, ubuntu-mate-desktop, or kubuntu-desktop. Alternatively, if your SD card is big enough, you could install the Ubuntu Studio desktop along with the software found in Ubuntu Studio.
ubuntu-desktop (GNOME 3) and ubuntu-unity-desktop (The default desktop environment in Ubuntu versions 17.04 and older) do not work since they require 3D compositing. kubuntu-desktop is slow unless you turn off desktop effects.

Default username is ubuntu, default password is ubuntu. It is recommended to either create a new account with sudo privileges and then use that account to delete the default account, or create a new account with sudo privileges and change the password of the ubuntu account to something secure.

Image is coming soon.

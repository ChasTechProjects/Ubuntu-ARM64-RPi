# Ubuntu-ARM64-RPi
Ubuntu 18.04 desktop images for the Raspberry Pi 3 built upon the standard Ubuntu ARM64 base.

These are Ubuntu 18.04 desktop images for the Raspberry Pi 3 built upon the standard Ubuntu ARM64 base.

They use the linux-raspi2 kernel instead of Raspbian's kernel. 

The following images are currently available:

* Ubuntu MATE 18.04
* Xubuntu 18.04

The following images will also be available at some point:

* Kubuntu 18.04
* Ubuntu Studio 18.04

Unfortunately, a Lubuntu 18.04 image cannot be built at the moment since lubuntu-desktop is not available for bionic arm64 at the moment.

Default username is ubuntu, default password is ubuntu. It is recommended to change your username and password. To change your password, simply run 'sudo passwd' in the terminal. You can change your username, but cannot do so while you're logged in as that user. So you'll have to change the root account password, reboot your system, login as the root user, and change your username from there. To do this, follow Valentin Uvega's instructions from <a href="https://askubuntu.com/questions/34074/how-do-i-change-my-username">this AskUbuntu discussion.</a>

The built-in wireless support, as well as sound (snd_bcm2835) works.

## Known Issues
* The linux-raspi2 kernel in bionic has not been updated since April 2018, meaning that it hasn't received the latest security patches and is not compatible with the Pi 3B+ out of the box. To fix the second issue, the latest bootloader files (bootcode.bin, *.elf, *.dat) from the Raspbian repositories were used after the linux-raspi2 kernel was installed.
* lubuntu-desktop is not available for arm64 in the bionic repositories, although it is available for cosmic arm64.

## Q&A

### My Pi hangs at the rainbow screen.

If your Pi hangs at the rainbow screen when booting one of these images, it means one of the following:

* You are using an incompatible Pi model. Ubuntu ARM64 only works on Pi's with the BCM2837 SoC.
* Your power supply isn't strong enough.

### Why aren't standard Ubuntu (GNOME 3) and Ubuntu Unity on the list of Ubuntu flavours to be ported to the Pi?

GNOME 3 and Unity are very resource heavy desktop environments and would be unusable on 1GB RAM. These desktop environments also require 3D compositing, something the linux-raspi2 kernel does not provide.

### Why does only one image get uploaded at a time? 

Uploading files (especially ones larger than 1GB) to GitHub takes a long time. If I were to upload two images at the same time to GitHub, it would slow down the overall upload speed. To speed up the upload time, I compress the images using the 7z archive format.

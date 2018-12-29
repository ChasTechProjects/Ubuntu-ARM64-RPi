# Ubuntu-ARM64-RPi
Ubuntu 18.04 desktop images for the Raspberry Pi 3 built upon the standard Ubuntu ARM64 base.

These are Ubuntu 18.04 desktop images for the Raspberry Pi 3 built upon the standard Ubuntu ARM64 base.

They use the linux-raspi2 kernel instead of Raspbian's kernel. 

The following images will be available at some point:

* Ubuntu MATE 18.04
* Xubuntu 18.04
* Kubuntu 18.04
* Ubuntu Studio 18.04

Unfortunately, a Lubuntu 18.04 image cannot be built at the moment since lubuntu-desktop is not available for bionic arm64 at the moment.

Default username is ubuntu, default password is ubuntu. It is recommended to change your username and password. To change your password, simply run 'sudo passwd' in the terminal. You can change your username, but cannot do so while you're logged in as that user. So you'll have to change the root account password, reboot your system, login as the root user, and change your user's password from there. To do this, follow Valentin Uvega's instructions from <a href="https://askubuntu.com/questions/34074/how-do-i-change-my-username">this AskUbuntu discussion.</a>

## Known Issues
*The Raspberry Pi Hybrid kernel is used compiled with ARM64 support rather than the linux-raspi2 kernel.

*Currently, no WiFi, not even Ethernet, works. I've tried installing various packages such as wpasupplicant and resolvconf but same issue. Expect the image to be released when this issue is fixed. 

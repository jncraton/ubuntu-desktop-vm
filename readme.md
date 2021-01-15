Ubuntu Desktop VM Appliance
===========================

This is a minimal VM configuration for Ubuntu Desktop with Git, Python 3, C/C++ build tools, and the [Micro](https://github.com/zyedidia/micro) text editor preinstalled.

Installation
------------

- Download the `ova` [VM appliance](https://github.com/jncraton/ubuntu-desktop-vm/releases/download/v1.1/ubuntu-desktop.ova) file from the [releases](https://github.com/jncraton/ubuntu-desktop-vm/releases/latest)
- Run it in your VM host of choice

There no password required to login, but the default password for `sudo` access is "password".

Details
-------

This image is a fresh install of Ubuntu Desktop 20.04. It is configured with the following settings:

- 10G dynamically allocated image
- "Minimal" install
- Single partition without swap for a smaller final image

The following process was completed after installation to minimze the size of the final image:

- Skip SSO, livepatch, and reporting info to Canonical, and location services in welcome wizard.
- Removal of unecessary packages:
    - Sound (alsa, pulseaudio)
    - Wireless tools
    - Error reporting (whoopsie)
    - Automatic updates
    - Dictionaries
    - Text-to-speech
    - Snaps
    - Apparmor
    - Gnome tools
    - Ubuntu extras
- zero free space
- Compress image after poweroff

The complete process can be executed by running the included `clean` script on the guest followed by `vboxmanage modifymedium --compact disk.vdi` on the host.

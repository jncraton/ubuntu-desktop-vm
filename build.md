Build
=====

These instructions describe the process that is used to create this appliance from a fresh Ubuntu install.

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

The complete process can be executed by running the included `clean` script on the guest.
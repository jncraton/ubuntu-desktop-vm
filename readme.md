Ubuntu Desktop VM Appliance
===========================

This is a minimal VM appliance running Ubuntu Desktop with Git, Python 3, C/C++ build tools, and the [Micro](https://github.com/zyedidia/micro) text editor preinstalled.

![Ubuntu Desktop](media/screenshot.png)

Installation
------------

- Download the [VM appliance](https://github.com/jncraton/ubuntu-desktop-vm/releases/download/v1.7/ubuntu-desktop.ova) file from the [releases](https://github.com/jncraton/ubuntu-desktop-vm/releases/latest)
- Run it in your VM host of choice, such as [VirtualBox](https://www.virtualbox.org/) (Windows, MacOS, Linux) or [Virt-manager](https://virt-manager.org/) (Linux).

Password
--------

There is no password required to login, but the default password for `sudo` access is "password".

Sharing Files Between Host and Guest
------------------------------------

### Git

Git is provided to make it easy to interact with repositories located on external hosts. You can clone a repository from your host system over SSH using a command such as:

```
git clone ssh://{user}@{host}:{port}/path/to/repository
```

It is typical for the host to be assigned the IP `10.0.2.2` and SSH will default to using port 22.

Git repositories may also be accessed from hosted services such as Gitlab and Github.

### SSH

SSH can be used to login to remote systems. Tools such as `scp` can be to copy files over SSH. 

If desired `sshfs` can be used to mount a path from the host system on the guest system.

# VirtualBox Guest Additions

VirtualBox guest additions are installed, so the "Shared Folder" functionality provided by this software should work correctly.

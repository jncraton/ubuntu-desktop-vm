Ubuntu Desktop VM Appliance
===========================

This is a minimal VM appliance running Ubuntu Desktop with `git`, `python3`, `gcc`, `make`, and the [`micro`](https://github.com/zyedidia/micro) text editor preinstalled.

![Ubuntu Desktop](media/screenshot.png)

Installation
------------

- Ensure that you have appropriate virtualization software such as [VirtualBox](https://www.virtualbox.org/) (Windows, MacOS, Linux) or [Virt-manager](https://virt-manager.org/) (Linux) installed.
- Download the [VM appliance](https://github.com/jncraton/ubuntu-desktop-vm/releases/download/v1.9/ubuntu-desktop.ova) and [import and run](https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html) it with your virtualization software.

Getting Started
---------------

If you've not had experience with a Linux or Unix command-line interface, you may want to consult [a tutorial](https://ubuntu.com/tutorials/command-line-for-beginners#3-opening-a-terminal) to help you become familiar with the basic commands.

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

### VirtualBox Guest Additions

VirtualBox guest additions are installed, so the "Shared Folder" functionality provided by this software should work correctly.

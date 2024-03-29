# Arch Linux

- [How to Install Arch Linux [Step by Step Guide]](https://itsfoss.com/install-arch-linux/)
- [7 Essential Things To Do After Installing Arch Linux](https://itsfoss.com/things-to-do-after-installing-arch-linux/)
- [Create a Sudo User on Arch Linux](https://www.vultr.com/docs/create-a-sudo-user-on-arch-linux)
- [Install Visual Studio Code Arch Linux](https://linuxhint.com/install_visual_studio_code_arch_linux/)
- [Install and Configure NFS](https://linuxhint.com/install_configure_nfs/)
- [ArchLinux 2017.10.01: Install nfs-utils for NFS client](https://www.hiroom2.com/2017/10/20/archlinux-20171001-nfs-utils-client-en/)
- [How to install Xfce Desktop on Arch Linux](https://ebblr.com/how-to-install-xfce-desktop-on-arch-linux)
- [How to Install GNOME in Arch Linux](https://phoenixnap.com/kb/arch-linux-gnome)
- [How to Properly Install and Setup KDE Plasma on Arch Linux](https://itsfoss.com/install-kde-arch-linux/)
- [Pacman command in Arch Linux](https://www.geeksforgeeks.org/pacman-command-in-arch-linux/)
- [The Arch Linux Handbook](https://www.freecodecamp.org/news/how-to-install-arch-linux/)
- [How To Fix “invalid or corrupted package (PGP signature)” Error In Arch Linux](https://ostechnix.com/fix-invalid-corrupted-package-pgp-signature-error-arch-linux/)
- [Guide to install Arch Linux using archinstall script](https://www.debugpoint.com/archinstall-guide/)

## Arch on VMWare

- [Arch Linux VMware ESXi](https://gist.github.com/kz0/56b59fb1987b27b9a059e59c93a5edfb)

## Arch on Hyper-V

- [Install Arch Linux on Windows 10 Hyper-V](https://dzone.com/articles/install-arch-linux-on-windows-10-hyper-v)
- [Arch Linux Wiki - Hyper-V](https://wiki.archlinux.org/index.php/Hyper-V)
- [Package clash with Arch; Enhanced session not working in Arch](https://github.com/microsoft/linux-vm-tools/issues/127)
- [Arch install hangs on Windows 11 Hyper-V VM](https://superuser.com/questions/1728001/arch-install-hangs-on-windows-11-hyper-v-vm)

## xrdp on Arch

1. Install xrdp AUR or xrdp-git AUR (Xvnc only) from:

- [Xrdp - ArchWiki](https://wiki.archlinux.org/index.php/xrdp)

  following:

- [How to install software/packages from AUR (Arch User Repository)](https://www.archlinuxuser.com/2013/01/how-to-install-softwarepackages-from.html)

2. Edit .xinitrc like so:

```bash
#  me - comment out below lines
#twm &
#xclock -geometry 50x50-1+1 &
#xterm -geometry 80x50+494+51 &
#xterm -geometry 80x20+494-0 &
#exec xterm -geometry 80x66+0+0 -name login

# me - start xfce:
exec dbus-launch xfce4-session
```

  this was taken from below:

- [XRDP GNOME Session Fails to Start](https://bbs.archlinux.org/viewtopic.php?id=261174)

3. Select Xvnc instead of Xorg in RDP session login

4. For xrdporg install xrdp AUR and xorgxrdp AUR.

- [SOLVED: "ERROR: One or more PGP signatures could not be verified!"](https://bbs.archlinux.org/viewtopic.php?id=277876)

## Docker & Kubernetes

- [How to Install and Use Docker on Arch Linux](https://www.linuxtechi.com/install-use-docker-on-arch-linux/)
- [Install and configure Kubernetes on Arch Linux](https://dnaeon.github.io/install-and-configure-k8s-on-arch-linux/)

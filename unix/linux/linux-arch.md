# Arch Linux

- [How to Install Arch Linux [Step by Step Guide]](https://itsfoss.com/install-arch-linux/)
- [7 Essential Things To Do After Installing Arch Linux](https://itsfoss.com/things-to-do-after-installing-arch-linux/)
- [Create a Sudo User on Arch Linux](https://www.vultr.com/docs/create-a-sudo-user-on-arch-linux)
- [Install Visual Studio Code Arch Linux](https://linuxhint.com/install_visual_studio_code_arch_linux/)
- [Install and Configure NFS](https://linuxhint.com/install_configure_nfs/)
- [ArchLinux 2017.10.01: Install nfs-utils for NFS client](https://www.hiroom2.com/2017/10/20/archlinux-20171001-nfs-utils-client-en/)
- [How to install Xfce Desktop on Arch Linux](https://ebblr.com/how-to-install-xfce-desktop-on-arch-linux)
- [Pacman command in Arch Linux](https://www.geeksforgeeks.org/pacman-command-in-arch-linux/)
- [The Arch Linux Handbook](https://www.freecodecamp.org/news/how-to-install-arch-linux/)
- [How To Fix “invalid or corrupted package (PGP signature)” Error In Arch Linux](https://ostechnix.com/fix-invalid-corrupted-package-pgp-signature-error-arch-linux/)

## Arch on Hyper-V

- [Install Arch Linux on Windows 10 Hyper-V](https://dzone.com/articles/install-arch-linux-on-windows-10-hyper-v)
- [Arch Linux Wiki - Hyper-V](https://wiki.archlinux.org/index.php/Hyper-V)
- [Package clash with Arch; Enhanced session not working in Arch](https://github.com/microsoft/linux-vm-tools/issues/127)

## xrdp on Arch

1. Install  xrdp-git AUR and  xorgxrdp-git AUR  from:

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

## Docker

- [How to Install and Use Docker on Arch Linux](https://www.linuxtechi.com/install-use-docker-on-arch-linux/)

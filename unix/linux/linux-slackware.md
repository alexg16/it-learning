# Slackware Linux

- [The Slackware Linux Project](http://www.slackware.com/)
- [Watch "How to Install Slackware Linux 14.2 + Review + VMware Tools on VMware Workstation Tutorial [HD]" on YouTube](https://youtu.be/ni-Fltd_ASo)
- [Installing VMware Tools in Slackware (14) - mkdir /etc/pam.d](https://lifeforce4.wordpress.com/2013/05/31/installing-vmware-tools-in-slackware-14/)
- [Slackware as a VMWare Guest - patch did not work - install sequence did after /etc/pam.d directory made](https://docs.slackware.com/howtos:misc:virtualisation:vmware_guest)
- [Installing vmtools](https://github.com/vmware/open-vm-tools/issues/653)

- place the following in /etc/rc.d/rc.local

```shell
/usr/bin/vmtoolsd -b /var/run/vmtoolsd.pid
```

- [Neofetch](https://slackware.pkgs.org/current/slackonly-x86_64/neofetch-3.2.0-noarch-1_slonly.txz.html)
- [Switch to a generic kernel](https://docs.slackware.com/slackware:beginners_guide)

- [Installing updates using slackpkg](https://docs.slackware.com/slackware:beginners_guide)

```shell
Blacklist the following kernel packages in “/etc/slackpkg/blacklist”:
kernel-generic
kernel-generic-smp
kernel-huge
kernel-huge-smp
kernel-modules
kernel-modules-smp
```

- [Upgrading Slackware to a New Release](https://docs.slackware.com/howtos:slackware_admin:systemupgrade)

- [Is Slackware the Right Linux Distribution for You? What You Need to Know](https://www.makeuseof.com/tag/is-slackware-the-oldest-remaining-linux-distribution-right-for-you/)
- [Watch How to Install Slackware 15.0 on PC Slackware Linux Install 2022 Installing Slackware 15 on PC](https://www.youtube.com/watch?v=ygSyKr9Mgno&t=70s)

## xrdp

- [Any advice on building and running xrdp and xorgxrdp on Slackware?](https://www.linuxquestions.org/questions/slackware-14/any-advice-on-building-and-running-xrdp-and-xorgxrdp-on-slackware-4175617278/page2.html)
- [14.2 > System > xrdp (0.9.12)](https://slackbuilds.org/repository/14.2/system/xrdp/#)
- [SlackBuild Scripts](https://www.slackwiki.com/SlackBuild_Scripts)
- [SlackBuild scripts - more](https://docs.slackware.com/slackware:slackbuild_scripts)

```shell
go into output directory /tmp and run make "installpkg"
```

- place the following in /etc/rc.d/rc.local to autostart xrdp and xrdp-sesman

```shell
if [ -x /usr/sbin/xrdp ]; then
  /usr/sbin/xrdp &
fi
if [ -x /usr/sbin/xrdp-sesman ]; then
  /usr/sbin/xrdp-sesman &
fi
```

- [Runit](https://docs.slackware.com/howtos:slackware_admin:runit)

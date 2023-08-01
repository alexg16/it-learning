# Fedora

- [How to install, start and connect to SSH Server on Fedora Linux](https://linuxconfig.org/how-to-install-start-and-connect-to-ssh-server-on-fedora-linux)
- [Install Xrdp Server to connect to Fedora Desktop from the Windows Remote Desktop feature](https://www.server-world.info/en/note?os=Fedora_33&p=desktop&f=7)
- [Repeated authentication requests in remote session](https://bugzilla.redhat.com/show_bug.cgi?id=1478345)
- [How to Install Visual Studio Code Editor in Fedora and CentOS](https://tecadmin.net/install-visual-studio-code-editor-in-fedora)
- [How to remove old unused kernels on Fedora/Linux](https://www.flyhiee.com/knowledge/how-to-remove-old-unused-kernels-on-fedora-linux/)
- [Fedora 35 Released! Here’s What’s New And How To Upgrade](https://fossbytes.com/fedora-35-released-how-to-update)
- [How to Roll Back the Kernel in Linux](https://www.howtogeek.com/740797/how-to-roll-back-the-kernel-in-linux/)
- [Excluding Packages From Transactions](https://docs.fedoraproject.org/en-US/quick-docs/dnf/#exclude-package)
- [Installing Chromium or Google Chrome browsers](Installing Chromium or Google Chrome browsers)

## Docker

- [Install Docker Engine on Fedora](https://docs.docker.com/engine/install/fedora/)

```shell
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 
docker run hello-world
```

- [How To Upgrade To Fedora 36 From Fedora 35 [Workstation And Server]](https://ostechnix.com/upgrade-to-fedora-36-from-fedora-35/)

```shell
Download complete! Use 'dnf system-upgrade reboot' to start the upgrade.
To remove cached metadata and transaction use 'dnf system-upgrade clean'
The downloaded packages were saved in cache until the next successful transaction.
You can remove cached packages by executing 'dnf clean packages'
```

- [How to boot an earlier kernel on Fedora](https://fedoramagazine.org/boot-earlier-kernel/)

To boot an earlier kernel in Fedora, you can use one of the following methods:

1. Install the python3-dnf-plugins-extras-versionlock package by running the command `sudo dnf install python3-dnf-plugins-extras-versionlock`. Then add a version lock for the version desired by running the command `sudo dnf versionlock add kernel-<version number>`¹.

2. Identify the kernel to be set to boot by default by running the command `grubby --info=ALL | grep '^title=' | sed 's/title=//'`. Then use the following command to set the default kernel to boot: `sudo grubby --set-default-index=<index number>`¹.

I hope this helps! Let me know if you have any other questions.

Source: Conversation with Bing, 8/1/2023
(1) How to boot an earlier kernel on Fedora - Fedora Magazine. https://fedoramagazine.org/boot-earlier-kernel/.
(2) Grub2: How to boot Fedora to an old kernel? - SysTutorials. https://www.systutorials.com/grub2-how-to-boot-fedora-to-an-old-kernel/.
(3) Remove older versions of kernel from boot loader in Fedora. https://medium.com/@sulokit/remove-older-versions-of-kernel-from-boot-loader-in-fedora-ce97886e8caa.
(4) Manually Upgrading the Kernel :: Fedora Docs. https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/kernel-module-driver-configuration/Manually_Upgrading_the_Kernel/.

The index number is the number assigned to each kernel in the GRUB menu. You can view the index of any of the kernel listed by running the command `grubby --info [kernel-filename] | grep index`. For example, if you want to view the index of `/boot/vmlinuz-4.18.0-80.11.2.el8_0.x86_64`, you can run the command `grubby --info /boot/vmlinuz-4.18.0-80.11.2.el8_0.x86_64 | grep index`. The output will show you the index number of that kernel¹.

I hope this helps! Let me know if you have any other questions.

Source: Conversation with Bing, 8/1/2023
(1) How to Change the default kernel (boot from old kernel ... - The Geek Diary. https://www.thegeekdiary.com/how-to-change-the-default-kernel-boot-from-old-kernel-in-centos-rhel-8/.
(2) 12 practical grubby command examples (cheat sheet). https://www.golinuxcloud.com/grubby-command-examples/.
(3) How to Set Default Entry for the Grub Menu | Baeldung on Linux. https://www.baeldung.com/linux/grub-set-default-entry.
(4) Chapter 7. Making persistent changes to the GRUB boot loader. https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_monitoring_and_updating_the_kernel/assembly_making-persistent-changes-to-the-grub-boot-loader_managing-monitoring-and-updating-the-kernel.


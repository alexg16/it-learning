# Hyper-V

- [Creating a Hyper-V Template](http://www.agileit.com/news/creating-a-hyper-v-template/)
- [Clone a Ubuntu server in Hyper-V](https://4sysops.com/archives/clone-a-ubuntu-server-in-hyper-v-2012-r2/)
- [Deploy Hyper-V on Windows Server](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/deploy/deploy-hyper-v-on-windows-server)
- [Enhanced Session for Kali Linux](https://gist.github.com/mimura1133/25451be04929d65993e0fb658d0b6890)
- [Export and Import virtual machines](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/deploy/export-and-import-virtual-machines)
- [How to Clone VM in Hyper-V](https://techjourney.net/how-to-clone-vm-virtual-machine-in-hyper-v/)
- [Hyper-V PowerShell Commands for Windows Server 2016: List & Uses](https://study.com/academy/lesson/hyper-v-powershell-commands-for-windows-server-2016-list-uses.html)
- [Move-VMStorage - PowerShell](https://docs.microsoft.com/en-us/powershell/module/hyper-v/move-vmstorage?view=win10-ps)
- [Nested Virtualization](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/user-guide/nested-virtualization)
- [RUN A NESTED VM ON KVM / QEMU VM IN HYPER-V](https://timothygruber.com/hyper-v-2/run-a-nested-vm-on-kvm-qemu-vm-in-hyper-v/)
- [REMOTELY MANAGING HYPER-V SERVER IN A WORKGROUP OR NON-DOMAIN](https://timothygruber.com/hyper-v-2/remotely-managing-hyper-v-server-in-a-workgroup-or-non-domain/)
- To remove the local subnet restriction on public networks and allow
remote access from any location, run the following command:

  ```Set-NetFirewallRule –Name "WINRM-HTTP-In-TCP-PUBLIC" –RemoteAddress Any```

  <http://www.powershellhelp.space/about/about_remote_troubleshooting-psv5.php>

- [How to Fix WinRm Firewall Exception Rule When Enabling PS Remoting](https://www.faqforge.com/powershell/fix-winrm-firewall-exception-rule-enabling-ps-remoting/)
- [Set up hosts for live migration without Failover Clustering](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/deploy/set-up-hosts-for-live-migration-without-failover-clustering)
- [What is the Hyper-V Virtual Switch and How Does it Work?](https://www.altaro.com/hyper-v/the-hyper-v-virtual-switch-explained-part-1/)
- [Support for USB access in Windows Server 2012 R2 Hyper-V through Microsoft’s new Virtual Machine Enhanced Session Mode](http://www.msserverpro.com/support-for-usb-access-in-windows-server-2012-r2-hyper-v-through-microsofts-new-virtual-machine-enhanced-session-mode/)
- [Set up a NAT network](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/user-guide/setup-nat-network)
- [Where did the native NAT switch go in Windows 10 1607](https://4sysops.com/archives/where-did-the-native-nat-switch-go-in-windows-10-1607/)
- [Windows 10 1709 Hyper-V Networking Enhancement](https://blogs.technet.microsoft.com/nextnextfinish/2018/02/02/windows-10-1709-hyper-v-networking-enhancement/)
- [Run Hyper-V and VirtualBox on the same machine](https://derekgusoff.wordpress.com/2012/09/05/run-hyper-v-and-virtualbox-on-the-same-machine/)
- [Create NAT Rules for the Hyper-V NAT Virtual Switch](https://petri.com/create-nat-rules-hyper-v-nat-virtual-switch)

## Storage

- [How to use iSCSI Targets on a Windows Server](https://kb.synology.com/en-global/DSM/tutorial/How_to_use_iSCSI_Targets_on_a_Windows_Server)
- [How to Use iSCSI Targets on Windows Computers with Multipath I/O](https://kb.synology.com/en-global/DSM/tutorial/How_to_Use_iSCSI_Targets_on_Windows_Computers_with_Multipath_I_O)
- [Hyper-V Cluster MPIO iSCSI Installation and Configuration](https://www.virtualizationhowto.com/2018/08/hyper-v-cluster-mpio-iscsi-installation-and-configuration/)
- [How to use iSCSI Targets on Windows computers with Multiple Connections per Session (MC/S) support](https://kb.synology.com/en-global/DSM/tutorial/How_to_use_iSCSI_Targets_on_Windows_computers_with_Multiple_Connections_per_Session_MC_S_support)

### Server Core

- [Configure Jumbo Frames using powershell in Hyper-v Server](https://www.itwithsathish.com/2021/04/29/configure-jumbo-frames-using-powershell-in-hyper-v-server/)

```
Set-NetAdapterAdvancedProperty -Name “NIC2” -RegistryKeyword “*JumboPacket” -Registryvalue 9014
ping 192.168.1.1 -f -l 8500
```

- [How to Use iSCSI Targets on Windows Computers with Multipath I/O](https://kb.synology.com/en-global/DSM/tutorial/How_to_Use_iSCSI_Targets_on_Windows_Computers_with_Multipath_I_O)

- [Configure MPIO and iSCI on core](https://www.virtualizationhowto.com/2018/08/hyper-v-cluster-mpio-iscsi-installation-and-configuration/)

```
mpiocpl
iscsicpl
```

- verify:

```
mpclaim -s -d
```

- Use DISKPART to attach existing iSCi disk

```
diskpart
select Disk 3
online
attributes disk
attributes disk clear readonly
import
```

- [Import a foreign disk](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/import_1)
- [How to Fix “Current Read Only State Yes”](https://www.diskpart.com/articles/current-read-only-state-yes-1881.html)

- or format a new disk:
- [Initialize Disk to GPT or MBR from CMD Diskpart](https://macrorit.com/partition-magic-manager/initialize-disk-gpt-mbr-from-cmd-diskpart.html)

- [How to Install Hyper-V on Windows Server Core](https://petri.com/how-to-install-hyper-v-on-windows-server-core/)

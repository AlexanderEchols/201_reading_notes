# **Day 10**

***Veeam. What is it and who cares?***

Veeam Backup Free Edition is a free tool for backing up VMs in both VMware and Hyper-V environments. The best part about Veeam is that they just released a new updated version (v7) that delivers important new features and capabilities. Here are 12 features discussed in previous editions of Veeam.
1. VeeamZIP Backup
2. Veeam Explorer for Exchange
3. Veeam Explorer for Storage Snapshots
4. Veeam Explorer for SharePoint
5. Quick Migration for VMware
6. File Copy Job
7. VM Copy Job
8. FastSCP Editor
9. Native tape support
10. File level recovery from backup
11. Whole VM recovery from backup
12. VM file recovery from backup (VMX, VHD, VMDK, etc.)

**VeeamZip** creates an ad-hoc backup of a running vm. This allows one to copy a backup w/out having to turn of the original VM. Using VeeamZip is easy, all one needs to have are the VM you want to backup and where your resulting backup will go. Once the VM has been backed up, the backed up version is then compressed thus requiring significantly lower backup storage requirements. Typically, when used on a single VM, the disk savings will be about half what the VM actually uses in disk space. Useful when:

	1. You need to update or patch a VM.
	2. You need to archive a VM.
	3. You need to copy a VM to a remote host or test lab. 

VeeamZIP is efficient. The processing engine is fast, and optimizations include parallel processing of virtual disks, filtering out empty blocks, and more.  

With it having Powerful and Flexible restores it supports a number of recovery scenarios, including an entire VM, guest OS files and individual application items  Some of those more are:

	1.RestoringVM files (.vmdk, .vmx and others for VMware: the Hyper-v files such as .vhd, .vhdx, and .xml etc) will restore VM files from deduplicated, compressed backups w/out needing to extract the full VM.
	2. Restoring an entire VM to the previous location or any other.
	3. Restoring VM disks (VMware). Used incase of corruption
    4. Restoring guest OS files. Can be done for both FAT and NTFS systems
	5. Restoring individual Microsoft Exchange and SharePoint items.

With Quick Migration (VMware) one has the ability to move a vm between hosts or datastores w/ minimal downtime and w/out the need of cluster, share storage, VMware Vmotion or Storage vMotion

***Wait can you do more?***

On top of the enhanced capabilities of the described above, we have another 7 new features.

1. Native tape support: Tapes are necessary because the are portable long-term storage the is inexpensive. Companies still use tapes as archives or offsite backups. With this new ability one can store individual files and VM backups on standalone tape drives and tape libraries. This is also a good replacement for NTBackup(discontinued)

2. Advanced support for VMware vCloud Director. implements enhanced backup and recovery support for VMware vCloud Director (vCD).


3. Veeam Explorer for microsoft SharePoint. Free tool built into veeam backup.This makes it easy to pull the whole VM image into production storage saving space. Doesn’t require installation of agents and restores only take a few seconds.  This makes it easy to:
    
    a. Search for individual item inside of backups

    b. Recover items quickly and without agents
    
    c. Send restored items as email attachments to specific users

4. Veeam Explorer for Microsoft Exchange. Same as the SharePointit provides quick and easy restore of items  from backups of microsoft exchange VMs. one can search for individual Exchange items (email, notes, etc), save mailbox items and send recovered items as attachments via email.
5. Parallel processing of virtual disks within VMs. Simultaneously handle several virtual disks inside one VM, improving VeeamZIP performance. This will reduce the amount of time snapshots exist, in turn reducing the time it takes to merge a snapshot with a vm after backup completes. 
6. Ignoring empty blocks. Detects and does not backup empty blocks w/in virtual disks being backed up
7. Hardware-accelerated compression.is the new default compression algorithm in v7. This new default lets VeeamZIP take into account available CPU resources on a backup server. This enables a “smart” compression algorithm using SSE extensions which reduces the workload on backup proxies. Also reducing server usage up to 10 times compared to previous compression levels. 

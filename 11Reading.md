# **Day 11**

***Where’d my SSD data go?***

Unlike Hdds, SSDs are hard to tell when they are about to do a complete shutdown, It is hard to see the warning signs. Below are some of the common indicators that your SSD is experiencing physical issues or approaching its read/write cycle limit:


1. Bad blocks: Storage segments that impede data storage and retrieval functions.
Key symptoms include Saving, reading, and moving files may result in failure; apps may be slow or crash frequently; may receive prompts to repair the file system; performance steadily decreases especially with large files.


Best way to prove your theory of Bad Blocks is to run software that searches for physical defects, if your SSD is damaged you’ll want to back up all your essential files and replace your SSD.

2. File System Repair: can’t find anything wrong using physical defect software, it could be a connector port issue. (its now that you want to back up integra files) this is where either Disk Utility(Mac users), fsck utility(Linux users) or using another freeware or premium software options.

3. Crashing: if the system continually crashes then starts working after several reboots, then your ssh is probably failing. Try the following; 
    * run software to assess the performance of your SSH, 
    * reinstall your OS after clearing the data on the partition set, or formatting the drive. Even if it starts working after doing any of these you still may want to replace the SSD.
4. Read-only mode: rare but on occasion an SSD can be corrupted to the point that it is only able to read your gonna wanna replace that fast.

***Now we see. How we fix?***

First we need to find the source of the issue. If the error is physical, I.E. hardware dmg or degraded flash cells, you’ll probably need to replace the SSD. 
If the error is logical, I.E. bad blocks, software malfunction, malware, outdated firmware, etc. it may be able to be repaired. Some options include:
Formatting the drive and redownloading the OS.
Power cycling the SSD: used when the drive is corrupted through power failure. 
Idling in the boot meny.
Updating SSD firmware
Updating drivers. 



***Is it gone forever?***

That depends on the situation, in an event where the physical or firmware damage is too extensive the drive and data on it may be lost forever. Sometimes though the corrupted drive may come back with the right approach, but that data still may not be salvageable
SSDs also has the ability to issue an Advanved Technology Attachment (ATA) command, Known as TRIM, to tell an OS which data blocks can be cleared. This increases both the performance and service life of an SSD. Using TRIM also creates complications in the retrival of data in the event of SSD corruption. Unlike traditional hard drive protocols, TRIM erases data completely upon deletion. Which means the data is gone before the block have ever been overwritten by a new file. SSDs with TRIM may lose their data forever, even if they are brought back to the land of the living. With the right tools all of these complications mentioned above may be concurred. One of these tools is known as the recovery wizard, this wizard can scan SSDs for deleted files and allow MSPs to restore partitions or any individual files they may need.

***Proactive VS reactive:***

In my humble opinion it is better to be proactive and follow best practices to prevent problems before they become full-blown failures. Below are some of those best practices one may want to implement to protect your SSDs performance and data retention.
Download a program from a selection of existing free software options designed to monitor SSD health by tracking operating temperature and performance metrics
When investing in a new SSD, buy strategically. Many SSDs come equipped with S.M.A.R.T. (Self-Monitoring, Analysis, and Reporting Technology) that warns users of potential failure and prompts them to take preventative measures
Have a backup strategy. Backup data regularly and routinely, even if your SSD was purchased recently and appears to be in good health. Unexpected corruption, power surges, viruses, or physical harm could befall your drive and cause permanent data loss. You truly never know what could happen—which is why valuable data should always be duplicated somewhere secure


### ***Part 2:***
***DBAN says bye, bye:***

This is a guide on using DBAN to erase all the files and folders on your hard drive.
1. Download DBAN(Darik’s Boot & Nuke) from SourceForge.
2. Save the DBAN ISO file to your computer somewhere easy to find.
3. Burn the DBAN ISO file to a USB device. Not copied, burned.
4. Restart the system and boot into the DBAN disc or USB device.
5. Choose an option from the DBAN main menu
    * Choosing F3 will open a quick commands screen. This is quick, so it wont ask for verification. 
6. Choose which hard drives to wipe w/ interactive mode. 
7. Wait for DBAN to erase the hard drives
8. Verify DBAN success in erasing the hard drives

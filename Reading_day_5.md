# **Day 5:**

## ***SMB Ports and who docks in em:***

### **Server Message Block Protocol (SMB Protocol):** 
Client serverd communication protocol used to share access to files, printers, serial ports, and data on a network. also carries transaction protocols for authenticated inter-process communication. This is a way for computers to communicate

### **The how behind the protocol:**

SMB starts when a client makes a specific request and the server responds accordingly (known as "response-request protocol") and this facilitates file shares between networked computers.
upon connection the application or user can request a file server and then gain access to various resources. w/ this a user can open, read, move, create, & update files on the remote server.

originally designed in 83 w/ the goal of turning the DOS INT 21h local file access into a networked file system. it was also originally designed to run on top of NetBIOS over TCP/IP (NBT) using the ip ports 137, 138 & 139
Software apps that run on a NetBIOS	session service locate and id each other by their NetBIOS names over TCP port 139.

### **Ports 139 and 445 Whos using them, and why?**

SMB requires an open port on a computer server to communicate w/ other systems. those ports are usually 139 and (ding. ding. ding. We have a winner) 445/

-139 is used by dialects that communicate over NetBIOS. acts as a transport layer protocol designed to use in windows OS over a network.

-445 used by newer virsions of SMB  (2000 and on) on top of a TCP stack, letting SMB communicate over the internet. meaning one may use IP adddresses in order to use SMB like file sharing. 

In order to check if a port is open, use the **netstat** command. there are known security issues w/ exposing these ports so be cautious. Always make sure your open ports arenot misconfigured (how do we do that, right?), unpathced, vulnerable to exploits, and finally, make sure you have strong network security rules in place. 
 
 ### **How do we command the command line? Tools.**

Not all users can run all commands, you have Standard privileges that run apps as a normal user. Standard is ok for alot of commands but for some, you need elevated privileges. This is done by being part of the Administrators group. If you wish to use the cmd as an admin you just select "run as an admin" but be careful as using the terminal as an administrator gives you the access to really muddy up your machine so be sure you know what you are doing.
use the **help** command to learn more about another command or tool you are about to use, syntax as follows: **help chkdsk**, another (faster way) is: **chkdsk /?**.

close the prompt with **exit** command

**dir** command: list files and directories you are currently working in

**cd** will change the directory, use a \ to specify the folder name or valume

**..** two dots/periods will move you to the folder above your current working one

use the **shutdown** command to (you guessed it) shutdown the computer. there are several flags that you add to determine the time, if you are going to fully shutdown or do a shutdown and reboot, or to abourt a shut down in progress. I.E:

wait 60 seconds, then shut down
	
    shutdown /s /t 60

shutdown and restart after 180 seconds
	
    shutdown /r /t 180

abourt the countdown

	shutdown /a

*Deployment Image Servicing and Management tool(**dism**) is used to manage Windows imaging format(WIM) files. some of the things one can do are;

- Get info about an image
- update applications
- Manage drivers
- manage updates
- Mount an image

**system file checker(sfc)** will scan integrity of all protected system files

**chkdsk** will check the disk, however there are some flags that are useful to know. the following code will fix logical file system errors on the disk
	
    chkdsk /f

this one will first run the above, then locate bad sectors and recover readable info

	chkdsk/r 

Sometimes, if the volume is locked, you may need to schedule the run to accure during startup. which is done when you simply type in the command and get the error that the volume is used up.

**DiskPart** will help you manage disk configurations 

if you want to manage tasks you don't need a task manager. you can use one of the following two commands

**tasklist** to dislplay a list of currently running processes, works on local or remote machines.

**taskkill** to terminate a task via id(PID) or image name. I.E.

	TASKKILL /IM notepad.exe (will kill all instances of notepad)
	TASKKILL /PID 1483 /T (would only kill the notepad asscociated with the PID)
Group policy will manage computers in an Active Directory Domain and is usually updated at login. syntax as follows;

To force a group policy update, one would simply use

	gpupdate /target:{computer or user} /force

To Verify policy settings for a computer or user you would use

	gpresult /r
	gpresult /user sgc/knott /v
**Formate** command lets you format a disk for use with Windows, BE CAREFUL - formating will delete all data on a disk

One quick way to copy a file or multiple files and move them to another area is the copy command. there are two flags we are going to focus on today with the copy command, and they are:

	copy /v - which varifies that the new files are written correctly and is very useful for moving things onto an external drive (thumb, hard, or solid)
	copy /y - which supresses prompting to confirm you want to overwrite an existing destination file

In order to copy full directory trees and files, one may use the **xcopy** command, designed to copy all files and directories inside a directory tree or instead we will probably want to use the Robust Copy command ( and not just because it reaminds me of robocop) which is **robocopy** and included in Windows 7, 8.1, and 10

**regedit.exe** Registry Editor: Make changes to Registry values; can be used to make selective backups. Prior to Windows XP, there were two editors: 
regedit.exe and regedt32.exe.

**defrag.exe** Disk Defragmenter: Used from the command line, or graphically through the Microsoft Management Console (MMC) and dfrg.msc.

**perfmon.exe** Perfomance console: View detailed performance information

**msconfig.exe** System Configuration Tool: Reconfigure the boot process for troubleshooting and diagnosing the boot process

**msinfo32.exe** System info: View hardware and configuration information for your computer
**eventvwr.msc** Event Viewer: Logging component of the operating system; the central location for all logging activity.
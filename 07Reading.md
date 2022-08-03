# **Day 7**

### ***Powershells and whats their power?***

Powershell is a CLI made by Microsoft, enables  admins to manage computer from the command line. Also is a scripting language, built on .NET which can be used for automating admin tasks and configuration management. 
Power shell tasks done using cmdlets to perform a wide variety of actions from checking the size of a file to spinning up hundreds of servers in the cloud.

### ***PS VS the rest:***
Powershell is made for doing things like managing a technology environment, while the rest (Javascript, Java, Python etc) are used to create new things (apps, websites, etc)

#### ***Whos using it?***
Admins, engineers or architects.

Typically, admins and engineers have their preferred os (Windows or Linux) based on preference or environment. Usually in the following scenario 

	*Linux>Bash>Python
	*Windows>Powershell>C#
Although now that Bash is available on Windows and Powershell is available on Linux people are being less picky about the system they work in.

***How they differ:***

There are a few differences worth noting here for one Bash works with strings while Powershell works with Objects. Another is that Bash passes output and input as plain text. Making it easy to move info to the next program. Powershell, on the other hand, works as a complete scripting environment. PowerShell scripts share complex data, passing entire data object structures between commands.

Bash can be cumbersome with its need of so much string manipulation and parsing to get info, however, all of Bash’s tools with a simple string that makes it easy to pass info around. With PowerShell one can move complex daya with very little effort due to the ability to easily pass objects between cmdlets. 

While they have their similarities and the lines between the two are blurring, most Linux users prefer Bash while most Windows users will take PowerShell. Basically it boils down to which you prefer to work with, Strings or Objects.

## **Part 2:**
This reading is about the fact that malware may be on the way out. In 2018, according to IBM’s X-Force research teams, only 43% of the attacks analyzed used regular Malware practices. The rest used Powershell scripts. This means that admins can no longer solely rely on detecting malicious executables and similar data on hard drives or other storages. These attacks, instead of forcing the machine to download, save, and execute a trojan payload. The attack is run entirely in memory using powershell. Which can then be used to do anything from steal passwords to mine crypto. One way to stop this is to require scripts be digitally signed. Powershell can be used to forego the file system and inject malicious code directly into memory, making it harder to find the nefarious activity, and often evading security controls designed to detect malware deployments. 

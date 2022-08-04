# **Day 08(wed)**

***Windows registry: What can you do?***

Windows registry is a collection of databases. With both system-wide(applies to all users) nand user-specific settings stored in the C:\Windows\System32\Config\  directory. And the user-specific keys are stored in a NTUSER.dat file (which can’t be edited directly) located at C:\Windows\Users\Name directory. One never needs to deal with these files. When you sign into Windows the settings are loaded from these files into memory. A launched program has the ability to check the registry stored in memory to find its configuration settings. If you change a programs settings, those same settings are changed in the registry. Upon sign out and shutdown of your machine, the state of the machine is saved to the disk. 

There are folder-like “keys and “values” that are contained inside the registry, those “keys” can contain numbers, text, etc. The registry is made up of multiple groups(called “hives”) of keys and values (I.E. HKEY_CURRENT_USER and HKEY_LOCAL_MACHINE) 

Not all programs have to (or chose to) use the registry. Some only use it for partial settings. Other settings may be stored in your Application Data folder.

If you really want to edit the registry (which is probably not necessary) it is done so through the Registry Editor. Now the registry is a right mess, so you’re going to want to look up some “registry hacks” online to find what settings to change. Exceptionally useful when looking for options that are normally not exposed by Windows. 

To open the Registry editor use Windows+r to open the “Run Dialog” box. Inside the box type “regedit” press enter. You will need to give the Registry Editor the ability to modify system settings, which is done agreeing to the User Account Control prompt that pops up


In windows 10, one can just copy-paste an address into the Registry Editor’s address bar.

Another way one may edit the registry is by downloading and running .reg files, these hold a change that is applied when you run them. Only download & run .reg files from trusted sources. If you worry about them then right-click on the .reg file and open it in Notepad as it is just a txt file. There is also always the option of creating your own registry hack files. A .reg file holds multiple settings, so you could create a .reg file that automatically applies all your favorite registry hacks and configuration tweaks to a windows pc when run.

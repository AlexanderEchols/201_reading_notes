# reading_notes
All my reading notes from Cyber sec training in Codefellows
Day 1: System Restore: who’s doing them, and why?
System restore is one of the most useful utilities when trying to fix major problems in windows. Basically, the System Restore allows one to revert a previous software, registry, and driver configuration known as a restore point. As most windows problems involve issues w/ at least one of those aspects of your OS, this tool is good to use early on in the troubleshooting process.

It is very easy to use and (on average) take anywhere from 10 - 30 minutes. Simply go to the Control Panel > System > system protection > click System Restore > next > select the time you wish to restore too > click next > confirm > finish (I would advise to always click the “scan for affected programs” box, to see what all is changed). Once started, system restore can’t be interrupted. If running from safe mode then the changes to your computer can’t be undone. Will have to restart so close anything you have running. Upon completion of the system restore, be sure to go back and check the issue was resolved. If the problem is not solved and you have an earlier date to choose from, do that. If not then continue down the troubleshooting methodology. If the System Restore caused additional problems, you can undo a system restore in windows.

Day 2: GIT/VSCode what are they and why?
GitHub = code hosting platform for version control and collaboration. 

VSCode = a lightweight, powerful source code editor. Comes w/ built-in support for JavaScript, TypeScript and Node.js also a bunch of extensions for langage, runtime, etc. 

Shellshock and friends:
Shellshock is one of the oldest known bugs in computer history. In 2014 security researchers discover a bug called Heartbleed, which was in an open source software for years. 

The Start: in 1987 Brian Fox drove from Boston to Santa Barbara w/ 2 massive reels full of software code and data which held a program called Bash, a tool built for UNIX OS but tagged w/ a license that let anyone use the code and even redistribute it to others. This was all part of the Free Software Movement, the idea was to gradually rebuild all of the components of the UNIX OS into a free product called GNU. The beginning of open source software. After setting up in Santa Barbara, Fox started working on Bash again, but so did a bunch of other engineers too. Bash found its way onto tens of thousands of machines. Around 1992 one engineer typed a bug into the code and it wasn’t found until 2014, this indicates a rather significant problem with Fox’s ancient program, called Shellshock, and it could allow hackers to wreak havoc on the modern internet. 
Because the net is built on software that gets endlessly used and reused, it’s littered with code that is decades old and never gets audited for security bugs. Today Bash is used by Google, Facebook, and every other big name on the internet

A Shell provides you w/ an interface to the UNIX System. It is an environment in which we can run our commands, programs, shell scripts, etc. 
Various styles of shell:
*Shell Prompt

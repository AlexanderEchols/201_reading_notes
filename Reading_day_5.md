SMB Ports and who docks in em:
Server Message Block Protocol (SMB Protocol): Client serverd communication protocol used to share access to files, printers, serial ports, and data on a network. also carries transaction protocols for authenticated inter-process communication. 
This is a way for computers to communicate
The how behind the protocol:
SMB starts when a client makes a specific request and the server responds accordingly (known as "response-request protocol") and this facilitates file shares between networked computers.
upon connection the application or user can request a file server and then gain access to various resources. w/ this a user can open, read, move, create, & update files on the remote server.
originally designed in 83 w/ the goal of turning the DOS INT 21h local file access into a networked file system. it was also originally designed to run on top of NetBIOS over TCP/IP (NBT) using the ip ports 137, 138 & 139
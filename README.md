# chordProtocol
Read ME

In this Project , Bidirectional chord protocol for distributed environment along with enhance feature such as caching, has been implemented by using socket programming under multithreaded environment.

Files :

This project contains below files

AntiFinger.java
Finger.java
Fix_finger.java
LRUCache.java
MyClient.java
MyNetwork.java
MyServer.java
Node.java
NodeInfo.java
Operation.java
P3.java
ServerThread.java


Execution Steps:

Downlaod all the files in a directory.

1) Compile the JAVA files using command and steps

javac <file name>.java


2) Execute the file using command
Java P3 <HostId>  (Note : Host ID should be unique for each nodes which are part of distributed system)


-Run the above command on multiple machines which are a part of distributed System.
-Add all hosts from a bootstrap machine by using command and format:

add <hostID>,<ip address>,<port>  (E.g : add 10,192.168.1.5,54622)

This command will establish connection with all hosts and shares the details of all host information with each host in a distributed system.


-Delete Command syntax:

delete <hostID>  (E.g delete 15)

This command will forward the delete request to all hosts in system. Host which is going to be deleted would distribute and transfer all its data to it’s successor neighbor in chord ring 
and after that it will exit from the system.


Useful Commands to work with Data Operation :

OUT - out command will simply put data on responsible node (E.g : out table, out chair )
IN - in command will get the data from responsible node (E.g : in table, in chair )
printFinger - This command will print the finger table of current node on console
printAntiFinger - This command will print the Anti finger table of current node on console
printData - This command is used to print out the keys which resides in that node.
nodeDetail - This command is used to print all the information about node’s successor and predecessor node. 
paChord - his command is used to print out the hops taken for each key searched in the traditional chord.
paEnhanced - This command is used to print out the hops taken for each key searched in our modified enhanced chord.
storeWordFile - This command is used to process all the data from a text file and to store the same on each responsible node.
		This command should fire first before using waWithCache or waWithOutCache command.
waWithCache - This command is used to generate a data request (in data request) by reading a input text file from current node. This command would serve the data request by using cache 
	     (E.g waWithCache data_1) where data_1 is input text file.
waWithOutCache - This command is used to generate a data request (in data request) by reading a input text file from current node. This command would serve the data request without using cache 
	     (E.g waWithOutCache data_1) where data_1 is input text file.

                                                                                                                                                                                          1,1           Top

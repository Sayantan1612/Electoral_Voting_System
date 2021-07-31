# Electoral_Voting_System
Project Name : Electoral Voting System.

->Based on Computer Networks: Connect Multiple computers so that data transfer can take place in between.
->Built on TCP, which is a connection-oriented protocol.
->Client acts as the voter and server is the electoral database.
->Registered candidates are allowed to vote, Non-registered can first register themselves and then vote. No duplication is allowed.

Consists of three files:
1. Votes.txt -> Those voted.
2. Candidates.txt -> candidature List for the election
3. Voters.txt -> List of voters.

-> The Client-Server Paradigm used here is TCP/IP Protocol which is a reliable and connection oriented Protocol.


->Implementation:

->Without using of Threads, We used the Listening Property of TCP built in Server for the same.
The entire Process Involves few steps & functions:	

->Socket creation- To perform network I/O, the first thing a process must do is call the socket function, specifying the type of communication protocol desired (TCP using IPv4, UDP using IPv6, Unix domain stream protocol, etc.),used by both Server & Client.
From the application layer point-of-view, the communication between client process and server process takes place through the sockets, created at two ends. It’s positioned b/w Application and Transport Layers.

->Binding- After creation of the socket, bind function binds the socket to the address and port number specified in addr(custom data structure),only by Server. 

-> Listen- It puts the server socket in a passive mode, where it waits for the client to approach the server to make a connection,only by Server.

-> Accept- It extracts the first connection request on the queue of pending connections for the listening socket, sockfd(socket already created), creates a new connected socket, and returns a new file descriptor referring to that socket,only by Server.

->Send- The send function is used to send data over stream sockets or CONNECTED datagram sockets, used by both Client & Server. 

->Recv- The recv function is used to receive data over stream sockets or CONNECTED datagram sockets,used by both Client & Server. 

-> Connect- The connect() system call connects the socket referred to by the file descriptor sockfd to the address specified by addr. Server’s address and port is specified in addr, used only by Client.


-> Why not UDP?
UDP is a connection-less unreliable data-gram, so there is no Listen Function and data-grams can come in any order and from any source and it would involve the use of concept of threads and forks.

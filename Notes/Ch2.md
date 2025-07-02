# Network Application Architectures
Client-server architecture there is an always-on host, called the server, which services requests from many other hosts, called clients.
clients do not directly communicate with each other
the server has a fixed, well-known address, called an IP address
P2P architecture there is minimal (or no) reliance on dedicated servers in data centers. Instead the application exploits direct communication between pairs of intermittently connected hosts, called peers.
not owned by the service provider
desktops and laptops controlled by users, with most of the peers residing in homes, universities, and offices
Self-scalability
cost effective  
Less  security, performance, and reliability → decentralized
Processes Communicating
Processes on two different end systems communicate with each other by exchanging messages across the computer network.
A network application here means any program (process) that is running on end-system e.g Web app
In the context of a communication session between a pair of processes, the process that initiates the communication (that is, initially contacts the other process at the beginning of the session) is labeled as the client. The process that waits to be contacted to begin the session is the server.
Any message sent from one process to another must go through the underlying network. A process sends messages into, and receives messages from, the network through a software interface called a socket.
A socket is the interface between the application layer and the transport layer within a host.
To identify the receiving process, two pieces of information need to be specified: 
(1) the address of the host and 
(2) an identifier that specifies the receiving process in the destination host.
The host is identified by its IP address.
The sending process must also identify the receiving process (more specifically, the receiving socket) running in the host. This information is needed because in general a host could be running many network applications. A destination port number serves this purpose.
When you develop an application, you must choose one of the available transport-layer protocols. The services that a transport-layer protocol can offer to applications invoking it are:
reliable data transfer, 
throughput, 
timing, and 
security.

If a protocol provides such a guaranteed data delivery service, it is said to provide reliable data transfer.
Throughput in the context of a communication session between two processes along a network path, is the rate at which the sending process can deliver bits to the receiving process. The application could request a guaranteed throughput of r bits/sec, and the transport protocol would then ensure that the available throughput is always at least r bits/sec. Applications that have throughput requirements are said to be bandwidth-sensitive applications. Elastic applications can make use of as much, or as little, throughput as happens to be available.
Timing guarantees can come in many shapes and forms. An example guarantee might be that every bit that the sender pumps into the socket arrives at the receiver’s socket no more than 100 msec later.

# TCP Services

# What is TCP/IP Model?
#protocol
Also called TCP/IP Stack

It is an alternative to the [[OSI MODEL]] 
It has only 4 layers
Most modern computer networks are TCP/IP-based

The Layers of this model are:
1. [[Network Interface Layer]]  - Describes how to transmit bits across a network and determine how the network medium is goin to be used.
2. [[Internet Layer]] - Where  data is taken and packaged into IP datagrams.
	- In this layer, some concepts covered include;
	  -> [[Internet Protocol (IP)]]
	  -> [[ICMP]]
	  -> [[ARP]]
	  -> [[Reverse ARP]]
3. [[Transport Layer]] - Defines the level of service and the status of the connection being used by [[Transmission Control Protocol (TCP)]], [[UDP]] or [[RTP]]
4.  [[Application Layer]] - Dictates how programs are going to interface with the transport layer by conducting session management.
	- Combines the 3 top layers of the [[OSI MODEL]]
	- This is the layer that the user interact with some sort of a program.
	
	

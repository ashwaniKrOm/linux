## SneakerNet :-
Initially computers did not communicate with each other, they were isolated. For transferring any file from computer A to B, a physical
storage (magnetic tape, punch card, floppy disk) device was used. The process is called SneakerNet. 

Networking develop to solve the sneakerNet.

## Networking :-
A setup which allow devices to communicate with each other.

## LAN (Local Area Network):-
Connecting computers with a network cable.

-easy file sharing
-can use shared resource (say common printer)
-can access shared server 

### Problem : if 100 computers are connected with single network cable, how computers will know whom(target computer) to share the data.
### Solution : Ethernet and MAC Address

## Ethernet :-
It is a LAN technology which defines the communication rules, means how the data frames will be shared by devices on LAN.

## MAC Address :-
Computer A will identify computer B(target computer) to share data via MAC Address of computer B's network interface. 
Note : MAC Address associated with Network Interface. A device can have multiple network interface which means a device can have multiple MAC Addresses.

### Network Interface :-
A computer can have multiple network interface for different purpose. Exp: Wi-Fi Adapter, Ethernet Adapter, etc

### Problem : Collision (suppose computer A and computer B both wants to share data to each other at same time.)
### Solution : CSMA

## Ethernet CSMA (Carrier Sense Multiple Access) :-
Carrier Sense : it checks whether communication medium is busy or free.
Multiple Access : it allow multiple devices to use same medium

Suppose both computer checks at same time and they found free medium, then shared at same time. That's why, CSMA only reduces chances of collision.

## Exponential Back-off :-
Suppose collision occurred and they can't start sharing at the same time again. So, waiting mechanism is used here.
- collision occurred
- computers select a random waiting time
- after waiting, they again transmit
- If somehow collision occurred continuously,the waiting time range exponentially increases. This approach is called Exponential Back-off

### Interview :-
Using Modern switched, full duplex Ethernet has normally zero chances of collision but Ethernet CSMA can have chances of collision, So CSMA/CD are rarely used

## Switch :-
Switch is like a receptionist who knows each professor and their cabin. Switch uses MAC Address of computers to forward the data frames.

Exp: ComputerA on Port1, ComputerB on Port2, ComputerC on Port3. ComputerA sharing data frames to ComputerB
- Switch checks incoming data frame's source MAC Address
- Switch Prepares a table where it maps source MAC Address with incoming port
- It checks destination MAC Address in the table
- If destination MAC is known, switch forwards the data frame.

Switch = forwarding data frames over local network on the basis of device's MAC Address
- Switch : work with MAC Addresses
- Router : work with IP Addresses

## Routing :-
Delivering data to the destination. Exp: ComputerA (India) and ComputerB (America), data has to travel over multiple networks.

### Circuit Switching :-
A dedicated/reserved communication path between two devices. Exp: Traditional telephone system which establishes a dedicated circuit between two devices.

### Message Switching :-
Suppose you are sending a message. Source -----> Intermediate Node (like a queue) --------> destination

Intermediate Node will store the message from source and deliver to target as per routing information. There can be some delay.

### Hop Count & Hop Limit :-
Suppose data is delivering through multiple routers. Source ---> Router A ---> Router B ---> Router C ---> Destination

These routers are here called hops and data packet delivers through the IP Address. if the routing configuration is wrong, packet may
loop in between the routers(hops). 

Router A ---> Router B ---> Router C ---> Router A 

The solution is TTL and Hop Limit because we can't allow packet to loop infinitely.
- IPv4 : TTL (Time To Live) for data packets
- IPv6 : Hop Limit
For each packet, these respective values decreases with move. Once value = 0, the packet discarded.

## Packet Switching :-
Data gets divided into smaller packets where each packet contains the network information. Packets travel through multiple networks and 
reconstruct at the destination.

Exp: Transfer 100 MB file via multiple data packets.

## IP Address :-
It is a network layer address which is used to route packet from source to destination. 

Exp: If your laptop is connected to Wi-Fi then the IP Address of network Interface can be used to route packets.

## Network Congestion :-
suddenly traffic increases 
- packets may delay
- queue may full
- packets may drop

Network Congestion control is a mechanism which manages queue and transport protocols in case of heavy traffics

## ARPANET :-
It was a packet switched computer network which defined the communication between two geographical separated computers through packet-switched networking.

## IoT :-
The modern example of networking. Those physical devices which collect and exchange data through sensors, software and network connectivity.
- Smart AC
- Smart TV
- Smart Refrigerator




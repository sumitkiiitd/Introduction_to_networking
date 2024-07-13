# Networking Quiz

## Question 1
**What is data encapsulation?**  

- The process of breaking down the different functionalities of network communication into layers, in order to make communication easier.
- **The process of adding extra information at each layer of the OSI model while information flows from one host to another.**
- The process that specifies how data is packetized, addressed, transmitted, routed, and received.

## Question 2
**A company has a teleconferencing system that utilizes VOIP technology. This system uses UDP as the transport. What will happen if UDP datagrams arrive at their destination out of sequence?**

- UDP will send a ICMP information request to the sending host.
- **UDP will pass the information in the datagrams up to the next layer in the order they arrived.**
- UDP will not acknowledge the datagrams but will wait for the retransmission of the datagrams.
- UDP will drop the datagrams.

## Question 3
**What is one purpose of the TCP three-way handshake?**

- Requesting the destination to transfer a binary file to the source.
- Sending echo requests from the source to the destination host to establish the presence of the destination.
- Determining the IP address of the destination host in preparation for data transfer.
- **Synchronizing between source and destination in preparation for data transfer.**

## Question 4
**What is the purpose of a router in the network?**

- To provide the connection points for the media.
- **To interconnect networks and choose the best path between them.**
- To provide the means by which the signals are transmitted from one networked device to another.
- To serve as the end point in the network, sending and receiving data.

## Question 5
**What is the difference between HTTP and HTTPs?**

- HTTP runs on the client while HTTPs runs on the server.
- **HTTPs uses encryption.**
- HTTP is an application layer protocol while HTTPs provides the transport service.
- HTTP uses TCP as the transport layer protocol while HTTPs uses UDP.

## Question 6
**What is the meaning of the output MTU 1500 Bytes?**

- The maximum packet size that can traverse this interface is 1500 bytes.
- **The maximum frame size that can traverse this interface is 1500 bytes.**
- The minimum packet size that can traverse this interface is 1500 bytes.
- The maximum number of bytes that can traverse this interface per second is 1500.

## Question 7
**What is the purpose of a switch in the network?**

- To connect separate networks and filter the traffic over those networks so that the data is transmitted through the most efficient route.
- To serve as the end point in the network, sending and receiving data.
- **To provide network attachment to the end systems and intelligent switching of the data within the local network.**
- To choose the path over which data is sent to its destination.

## Question 8
**Switch ‘leaf1’ needs to send a frame to a host with the following MAC address of 00b0.d056.efa4. Based on the MAC address table shown here, what will switch ‘leaf1’ do with the frame?**

- Send an ARP request out all of its ports.
- Drop the frame because it does not have an entry for that MAC.
- **Flood the frame out all of its ports.**
- Forward the data to its default gateway.

## Question 9
**Why will a switch never learn a broadcast address?**

- Broadcast addresses use an incorrect format for the switching table.
- Broadcast frames are never sent to switches.
- A broadcast address will never be the source address of a frame.
- A broadcast frame is never forwarded by a switch.

## Question 10
**Host A sends an initial frame to Host B. What is the first thing the switch will do?**

- It will add address 00:0b:db:95:2e:e9 to the MAC address table.
- It will add address 00:0a:8a:47:e6:12 to the ARP table.
- **It will add address 00:0a:8a:47.e6:12 to the MAC address table.**
- It will add address 00:0b:db95.2e:e9 to the ARP table.

## Question 11
**In a layer-3 data center design how can you achieve multipath support?**

- An MSTP instance per VLAN group can be configured.
- A layer-3 design cannot support multipath.
- **STP with ECMP can be configured.**
- BGP with ECMP can be configured.

## Question 12
**In a layer-2 data center design how can you achieve multipath support?**

- **An MSTP instance per VLANs group can be configured.**
- A layer-3 design cannot support multipath.
- STP with ECMP can be configured.
- BGP with ECMP can be configured.

## Question 13
**BGP is an increasingly popular protocol for use in the data center thanks to the following properties: (Select two)**

- **Multipath support.**
- BGP was specifically designed for leaf-spine topologies.
- Periodic updates that allow fast convergence.
- **Scalable and stable.**

## Question 14
**Which two of these are used to prevent loops in a layer 2 network? (Select two)**

- RoH
- ECMP
- **STP**
- **MLAG**
- BGP

## Question 15
**What is the purpose of the Time To Live (TTL) field carried in an IP packet?**

- **To avoid packets from endlessly circulating in a loop.**
- To determine the number of routers the packet is allowed to traverse.
- To record the time it takes for a packet to get to the destination node.
- To determine what is the trip time allowed for a packet till it gets to the destination node.

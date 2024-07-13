# Ethernet Fundamentals

## Introduction
Welcome to the Ethernet Fundamentals unit. In this unit, we'll cover the basics of Ethernet technology and understand how data is forwarded in an Ethernet network. 

## Overview
- **Ethernet Technology Evolution and Standards**
- **Ethernet Specifics**:
  - MAC addresses
  - Ethernet frame structure
- **Ethernet Switches**:
  - MAC address tables

## OSI Model Layers
- **Data Link Layer**: Provides means to transfer data between network nodes and detect/correct errors from the physical layer.
- **Physical Layer**: Defines electrical or optical properties and transfer speed of the physical connection.

## Ethernet Evolution
- **1970s**: Introduced by Robert Metcalfe at Xerox Corporation, Palo Alto Research Center, California.
- **1980s**: IEEE 802.3 standard published.
- **Throughput**: 
  - Original: 10 Mbps
  - Mid-1990s: 100 Mbps
  - Current: Up to 400 Gbps

## Ethernet Basics
- **Communication**: Ethernet nodes on the same LAN communicate by sending Ethernet frames to each other.
- **MAC Address**: Unique identifier for Ethernet nodes, required for frame generation and forwarding.
- **NIC (Network Interface Card)**: 
  - Connects a node to the network (wired/wireless).
  - Functions at both physical and data link layers.
- **MAC Address Structure**:
  - 48 bits long, 12 hexadecimal digits.
  - Split into two halves:
    - OUI (Organizationally Unique Identifier): First 6 digits.
    - Serial Number: Last 6 digits.

## Commands to Identify MAC Addresses
- **Linux**: `ifconfig`
- **Windows**: `ipconfig`

## Ethernet Frame Structure
- **Payload**: Protocol data unit from the upper layer.
- **Header**:
  - **Destination MAC Address**: Specifies the intended node.
  - **Source MAC Address**: Specifies the sending node.
  - **Type Field (EtherType)**: Indicates the upper layer protocol type (e.g., IPv4 packet).
- **Trailer**:
  - **Frame Check Sequence (FCS)**: Used to detect corrupted frames.

## Ethernet Frame Sizes
- **Standard Frame**: 
  - Payload: 46 to 1,500 bytes.
  - Overall size: 64 to 1,518 bytes.
- **Jumbo Frames**: Payloads larger than 1,500 bytes (not a standard but supported by some vendors).
- **Collision Fragments (Runts)**: Frames less than 64 bytes, automatically discarded.

## Ethernet Switches
- **Function**: Hardware devices with multiple ports connecting Ethernet nodes.
- **Forwarding Frames**: Based on destination MAC address in the frame.
- **MAC Address Table**:
  - Maps destination MAC addresses to exit ports.
  - Populated dynamically as frames are received.

## Frame Forwarding Example
1. **Node A to Node B**: 
   - Node A sends a frame to Node B.
   - Frame received by switch on port 1.
   - Switch adds entry for MAC A to port 1.
   - Future frames to MAC A sent on port 1.
2. **Aging Time**: Dynamically learned entries have an aging time; if unused, they're flushed from the table.
3. **Static Entries**: Configurable and not aged out.

## Unknown Unicast Frames
- **Unknown Unicast**: No matching entry in the MAC address table.
- **Flooding**: Switch sends the frame to all ports except the incoming port.

## Broadcast and Multicast Frames
- **Broadcast Frames**: Destination MAC address with all bits set to one (FF:FF:FF:FF:FF:FF).
  - Switch floods broadcast frames.
- **Multicast Frames**: Destination MAC address with the least significant bit of the first octet set to one.
  - Traditionally flooded by switches.

## Layer 2 vs. Layer 3 Switching
- **Layer 2 Switching**: Operates at the data link layer, forwarding packets based on MAC addresses.
- **Layer 3 Switching**: Combines switch and router functionality, operating at the network layer based on IP addresses.
- **Multi-layer Switches**: Add flexibility to the network.

## Conclusion
Understanding Ethernet fundamentals, including MAC addresses, frame structure, and the role of switches, is crucial for networking. This knowledge forms the basis for more advanced topics in network design and management.

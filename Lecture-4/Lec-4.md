# Data Center Design Considerations

## Introduction

Welcome to the data center design considerations course. The purpose of this unit is to equip you with the basic knowledge to understand the main data center requirements and how they can be fulfilled.

## Overview

### What is a Network Topology?

A network topology is the schematic arrangement of elements such as links and nodes, which ultimately constitutes the structure of the network. It describes how devices on the network are connected and how data moves from one node to another.

### Key Considerations for Choosing a Network Topology

1. **Availability**
   - Maximum availability of network resources for critical applications.
   - Consider high availability features throughout the network.
   
2. **Reliability**
   - Network reliability is fundamental, especially where downtime and delays are unacceptable.

3. **Performance**
   - The topology of a network determines its performance, ease of fault location, error troubleshooting, and resource allocation.

4. **Future Growth**
   - Choose a topology that allows easy addition of new nodes without negatively affecting performance or user experience.

5. **Budget**
   - Find a balance between cost and suitability.

## Hierarchical Network Design

### Traditional Design: Hierarchical Network

- **North-South Traffic Patterns**: Suitable for client-server applications where the majority of data goes in and out of the data center.
- **Modularity**: Scales somewhat well but can face bottlenecks if uplinks between layers are oversubscribed.

## Modern Network Design: Leaf-Spine Architecture

### Leaf-Spine Design

- **East-West Traffic**: More data moves between servers and storage nodes, crucial for modern data centers.
- **Two-Layer Full-Mesh Topology**: Composed of leaf switches (connect servers to the network) and spine switches (connect leaf switches with each other).
- **Scalability**: Additional levels (e.g., super spine) can be added for larger networks.

## Layer 2 vs. Layer 3 Design

### Layer 2 Networks

- **Switching**: Networking devices make Layer 2 forwarding decisions.
- **MAC Address Table**: Maps MAC addresses to exit ports.
- **Challenges**: Does not scale well, lower bandwidth, harder to achieve redundancy and multipath support.

#### Redundancy and Multipath Support

- **Redundancy**: Duplicate elements like switches or links to avoid single points of failure.
- **Multipath Support**: Allows traffic forwarding over multiple paths, increasing bandwidth and resource utilization.

### Challenges with Layer 2 Networks

- **Broadcast Storms**: Loops cause broadcast frames to circulate endlessly, consuming all bandwidth.
- **Spanning Tree Protocol (STP)**: Ensures a loop-free logical topology, but convergence times are too slow for modern data centers.
- **Rapid Spanning Tree Protocol (RSTP)**: Faster convergence but still wastes bandwidth due to blocked ports.
- **Multiple Spanning Tree Protocol (MSTP)**: Configures multiple STP instances for different VLANs to achieve load balancing.
- **Link Aggregation Group (LAG)**: Aggregates multiple physical ports into one logical port for higher bandwidth, load balancing, and high availability.
- **Multi-Chassis LAG (MLAG)**: Aggregates physical ports of two separate switches into one logical port, appearing as a single Layer 2 switch.

### Layer 3 Networks

- **Routing**: Routers or Layer 3 switches are configured for routing.
- **Routing Table**: Maps remote IP networks to next hop routers.
- **Equal Cost Multipath (ECMP)**: Allows packet forwarding over multiple best paths, supporting redundancy and load balancing.

#### Routing Protocols

- **BGP (Border Gateway Protocol)**: Preferred for its scalability and stability in large networks.
- **OSPF (Open Shortest Path First)**: Common but less scalable compared to BGP.

### Layer 3 Network Design Options

1. **Combined Layer 2 and Layer 3 Design**
   - **Layer 2 at the Leaf Level**: MLAG for redundancy.
   - **Layer 3 at the Spine Level**: ECMP for scalability and load balancing.
   - **Typical Deployments**: Data centers and big enterprises, high-scale bare metal and virtualized hosts.

2. **Full Layer 3 Design**
   - **Layer 3 from Host to Leaf to Spine**: ECMP for redundancy.
   - **Eliminates Layer 2 Protocols**: Requires routing on the host.
   - **Typical Deployments**: Highly virtualized environments with a high degree of host mobility.

## Conclusion

For modern data centers, a Layer 3 design is generally more suitable due to its scalability, redundancy, and ease of management.

---

Thank you for watching!

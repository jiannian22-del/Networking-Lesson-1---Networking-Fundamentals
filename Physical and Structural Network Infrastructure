# Module 03 — Network Architecture, Devices, and Transmission Media

## Learning Objectives
By the end of this module, you will be able to:
* Explain the differences between client-server and peer-to-peer network architectures.
* Describe the functions and applications of common networking devices.
* Understand how switches, routers, wireless access points, and modems work together.
* Identify common Ethernet cable categories and understand the purpose of RJ45 connectors.
* Explain the differences between copper and fiber-optic transmission media.
* Understand basic network performance concepts, including bandwidth, throughput, and latency.
* Configure and test a basic local area network (LAN) using Cisco Packet Tracer.
* Perform basic network connectivity troubleshooting using the `ping` command.

---

## 1. Client-Server vs. Peer-to-Peer Architecture
Network architecture describes how devices communicate, share resources, and provide services within a network. Two common approaches are **client-server architecture** and **peer-to-peer (P2P) architecture**.

### 1.1 Client-Server Architecture

#### Definition
Client-server architecture is a network model in which client devices request services or resources from a central server. The server processes these requests and provides the required information or service. A client can be a computer, smartphone, or application, while a server is a high-performance physical or virtual machine running specialized service software.

#### How It Works
1. **Request:** A client sends a service request to a server over the network.
2. **Processing:** The server receives, authenticates, and processes the request.
3. **Retrieval:** The server queries local databases or files to complete the request.
4. **Response:** The server sends the resulting data back to the client.
5. **Rendering:** The client displays or utilizes the returned information.

#### Example: Accessing a Website
When opening a web browser to visit a webpage:
* Your computer/browser acts as the **client**.
* The browser issues an **HTTP/HTTPS request** over the network to the web server.
* The web server processes the request and sends back HTML, CSS, and media files.
* The browser renders the website locally for the user.

#### Common Examples
* **Web Servers:** Deliver web page contents to browsers.
* **File Servers:** Provide centralized directory storage and file sharing.
* **Database Servers:** Host and manage structured data for corporate software.
* **Mail Servers:** Manage, route, and store electronic mail messages.
* **Authentication Servers:** Validate credentials and control user access (e.g., Active Directory).

#### Advantages & Disadvantages
* **Advantages:** Centralized administrative management, strict access control, reliable centralized backups, efficient resource sharing, and high scalability.
* **Disadvantages:** High initial hardware/licensing costs, continuous maintenance needs, potential single points of failure without redundancy, and total network dependency.

#### Real-World Example
In a corporate office, employees store their work files on a shared corporate file server. The file server manages access permissions, ensuring only authorized team members can open and edit specific files.

---

### 1.2 Peer-to-Peer (P2P) Architecture

#### Definition
Peer-to-peer architecture is a network model in which participating devices (**peers**) communicate and share resources directly with one another without requiring a dedicated central server. Each peer can act simultaneously as both a client and a service provider.

#### How It Works
1. **Discovery:** One peer locates another available peer holding a required resource.
2. **Connection:** Direct communication is established between the two endpoints.
3. **Exchange:** Data is shared or transferred directly between the peers.
4. **Local Management:** Each individual peer controls and manages its own locally shared resources.

#### Example: Direct Local File Sharing
Two laptops on the same Wi-Fi network exchange documents directly by sharing a local folder. Neither laptop relies on a server to manage or route the shared files.

#### Common Examples
* Direct LAN file transfers between personal computers.
* Distributed file distribution protocols (e.g., BitTorrent).
* Decentralized VoIP and messaging platforms.
* Distributed computing systems where devices contribute unused processing power.

#### Advantages & Disadvantages
* **Advantages:** Low implementation cost, simple setup for small sites, direct host-to-host transfers, and no reliance on expensive dedicated hardware.
* **Disadvantages:** Difficult centralized administration, security management risks across individual nodes, file unavailability when host peers are offline, and complex backup procedures.

#### Real-World Example
A small team working in a temporary field office shares project documents between two laptops using built-in operating system shared folders, avoiding the need to deploy a server infrastructure.

---

### 1.3 Client-Server vs. Peer-to-Peer Comparison

| Feature | Client-Server | Peer-to-Peer |
| :--- | :--- | :--- |
| **Architecture** | Clients request services from dedicated servers | Peers share resources directly with each other |
| **Management** | Centralized | Distributed across individual peers |
| **Dedicated Server** | Required | Not required |
| **Resource Storage** | Centralized server storage | Distributed across peer hard drives |
| **Security** | Centralized security policies | Managed independently per device |
| **Scalability** | High; suitable for enterprise environments | Variable; depends on active participating peers |
| **Cost** | Higher initial infrastructure & maintenance costs | Low initial costs using existing hardware |
| **Availability** | Dependent on server uptime and redundancy | Dependent on individual peer availability |
| **Primary Example** | Enterprise web, mail, or file servers | Local folder sharing or decentralized file transfer |

> **Note:** Client-server and P2P are conceptual models. Modern networks frequently combine both; for example, using client-server models for network authentication alongside P2P protocols for local media streaming.

---

## 2. Network Devices
Network devices are hardware components used to connect endpoints, direct traffic, secure boundaries, and extend signal range.

### 2.1 Network Interface Card (NIC)
A **Network Interface Card (NIC)** provides the physical interface between a computer and a network medium (wired Ethernet port or wireless Wi-Fi radio).
* **Primary Role:** Converts internal digital device data into physical network signals.
* **Addressing:** Hardcoded with a unique hardware address called a **MAC Address** for Layer 2 identification.
* **Examples:** Integrated motherboard Ethernet ports, PCI Wi-Fi cards, and USB-to-Ethernet dongles.

### 2.2 Switch
A **Switch** operates primarily at Layer 2 (Data Link) to connect multiple wired devices within the same Local Area Network (LAN).
* **Primary Role:** Inspects incoming Ethernet frame headers, builds a **MAC Address Table**, and forwards data frames exclusively to the specific physical port connected to the destination host.
* **Key Benefits:** Prevents unnecessary network traffic collisions compared to legacy hubs and supports Virtual LANs (VLANs).
* **Types:** Unmanaged (plug-and-play), Managed (configurable), Layer 2 (MAC-based), and Layer 3 (combines switching with IP routing).

### 2.3 Router
A **Router** operates at Layer 3 (Network) to forward IP packets between distinct, separate IP networks.
* **Primary Role:** Examines the destination IP address of incoming packets, consults its internal **Routing Table**, and routes the packet across the optimal path toward its destination.
* **Key Feature:** Acts as a boundary between broadcast domains. It strips incoming Layer 2 frame headers and encapsulates IP packets into new frames suited for the outgoing interface link.
* **Additional Functions:** Frequently supports Network Address Translation (NAT), DHCP services, and firewall protection.

### 2.4 Wireless Access Point (AP)
A **Wireless Access Point (AP)** allows Wi-Fi-enabled wireless clients to connect to a wired network.
* **Primary Role:** Broadcasts a network identifier (**SSID**) and bridges wireless radio traffic directly onto an Ethernet wired network segment.
* **Difference from Wireless Router:** A standalone Access Point simply bridges wireless traffic to a switch. A commercial "wireless router" combines a router, a switch, an access point, a DHCP server, and a firewall into a single physical chassis.

### 2.5 Modem
A **Modem** (Modulator-Demodulator) translates digital data from a local router into analog or radio-frequency signals suitable for an Internet Service Provider's (ISP) external transmission line (e.g., Coaxial Cable or DSL).
* **Note:** High-speed Fiber-optic connections replace traditional modems with an **Optical Network Terminal (ONT)**, which converts light signals into electrical Ethernet signals.

### 2.6 Firewall
A **Firewall** acts as a network security barrier, controlling inbound and outbound traffic according to strict, pre-configured security rules.
* **Primary Role:** Inspects packets based on IP address, port numbers, protocols, and connection states to block unauthorized access while permitting safe traffic.

### 2.7 Repeater
A **Repeater** receives incoming physical network signals, regenerates them back to original strength, and retransmits them to overcome physical cable or wireless distance limits and signal attenuation.

### 2.8 Bridge
A **Bridge** connects two separate physical LAN segments at Layer 2, filtering or forwarding traffic between them based on destination MAC addresses. Modern switches are essentially multi-port bridges.

### 2.9 Optical Network Terminal (ONT)
An **ONT** is the endpoint device installed at a customer premises in a Fiber-to-the-Home (FTTH) network. It converts fiber-optic light impulses into standard RJ45 electrical Ethernet connections for the local router.

### 2.10 Summary of Network Devices

| Device | Main Function | Layer / Use Case |
| :--- | :--- | :--- |
| **NIC** | Connects host system hardware to network media | Layer 1 / 2 interface component |
| **Switch** | Forwards frames based on MAC addresses within a LAN | Layer 2 internal network connectivity |
| **Router** | Forwards packets between different IP subnets | Layer 3 inter-network routing & internet access |
| **Wireless AP** | Bridges wireless Wi-Fi client traffic to a wired LAN | Layer 2 wireless access extension |
| **Modem / ONT** | Converts ISP access line signals into Ethernet data | Boundary translation for internet access |
| **Firewall** | Filters network traffic using security rule sets | Security boundary protection |
| **Repeater** | Regenerates weak physical signals | Signal distance extension |
| **Bridge** | Filters & links two local physical network segments | Legacy Layer 2 LAN interconnectivity |

---

## 3. Transmission Media
Transmission media provide the physical paths for network data signals. Choosing media impacts speed, link distance, cost, and interference immunity.

### 3.1 Ethernet Cables
Ethernet twisted-pair copper cables use pairs of insulated copper wires twisted together to cancel out electromagnetic interference (EMI) and crosstalk.

#### Common Ethernet Categories

| Category | Max Speed | Max Standard Distance | Common Applications |
| :--- | :--- | :--- | :--- |
| **Cat5e** | Up to 1 Gbps | 100 meters (328 ft) | Legacy and standard home/small office LANs |
| **Cat6** | 1 Gbps (10 Gbps up to ~55m) | 100 meters | Standard modern office LAN cabling |
| **Cat6a** | Up to 10 Gbps | 100 meters | High-speed enterprise networks and server links |

* **Pros:** Low cost, easy installation, supports Power over Ethernet (PoE).
* **Cons:** Limited to 100m total channel length, susceptible to high EMI environments.

### 3.2 RJ45 Connectors & Wiring Standards
Twisted-pair cables use standard **RJ45** (8P8C) modular plugs. Connectors are wired according to two standard pinout configurations:

| Pin | T568A Wire Color | T568B Wire Color |
| :---: | :--- | :--- |
| **1** | White/Green | White/Orange |
| **2** | Green | Orange |
| **3** | White/Orange | White/Green |
| **4** | Blue | Blue |
| **5** | White/Blue | White/Blue |
| **6** | Orange | Green |
| **7** | White/Brown | White/Brown |
| **8** | Brown | Brown |

* **Straight-Through Cable:** Uses the same pinout standard on both ends (T568B to T568B). Used to connect different device types (e.g., PC to Switch).
* **Crossover Cable:** Uses different standards on each end (T568A to T568B). Historically used to connect similar devices (e.g., Switch to Switch). *Modern devices use Auto-MDIX to automatically adjust pinouts.*

### 3.3 Fiber-Optic Cables
Fiber-optic cables transmit data using modulated light pulses through ultra-thin glass cores.

* **Single-Mode Fiber (SMF):** Microscopic glass core (~9 microns). Light travels along a single path using laser diodes. Used for long distances (up to tens of kilometers) such as ISP backbones and campus inter-building links.
* **Multimode Fiber (MMF):** Larger glass core (~50–62.5 microns). Uses LED or VCSEL sources allowing multiple light modes. Used for shorter, high-speed runs (up to ~550m) in data centers and server rooms.

### 3.4 Copper vs. Fiber-Optic Comparison

| Feature | Copper (Twisted-Pair) | Fiber-Optic Cable |
| :--- | :--- | :--- |
| **Signal Type** | Electrical pulses | Light pulses |
| **Interference Immunity** | Susceptible to EMI and crosstalk | Complete immunity to electrical/radio interference |
| **Maximum Distance** | 100 meters | Hundreds of meters to tens of kilometers |
| **Bandwidth Capacity** | Moderate to High (up to 10 Gbps) | Extremely high (100+ Gbps) |
| **Installation Cost** | Low material & tool costs | Higher material, transceiver, & installation costs |
| **Power Delivery** | Supports Power over Ethernet (PoE) | Cannot transmit electrical power |
| **Electrical Isolation** | No | Yes (prevents ground loops and surge damage) |

---

## 4. How Network Devices Work Together

### 4.1 Topology Integration Architecture

                   [ Internet ]
                        |
                 [ ISP Network ]
                        |
                  [ Modem / ONT ]
                        |
                 [ Router / FW ]
                 /             \
         (Wi-Fi Link)     (Ethernet Link)
             /                   \
    [ Wireless AP ]             [ Switch ]
      /         \               /        \
 [Laptop]    [Phone]        [ PC ]    [Printer]

1. **Local Communication:** A PC sends a document to the local Printer. Traffic passes directly through the **Switch** without needing to reach the Router.
2. **External Communication:** A Laptop requests a webpage over **Wi-Fi**. The **Access Point** bridges the radio frame onto the wired link, sending it to the **Router**. The router performs NAT, routes the IP packet to the **Modem/ONT**, and forwards it across the ISP to the **Internet**.

---

### 4.2 MAC Addresses vs. IP Addresses

| Property | MAC Address (Media Access Control) | IP Address (Internet Protocol) |
| :--- | :--- | :--- |
| **OSI Layer** | Layer 2 (Data Link Layer) | Layer 3 (Network Layer) |
| **Address Purpose** | Local delivery within the same network segment | Logical routing across interconnected networks |
| **Address Structure** | 48-bit Hexadecimal (e.g., `00:1A:2B:3C:4D:5E`) | IPv4: 32-bit (e.g., `192.168.1.1`), IPv6: 128-bit |
| **Assignment** | Burned into physical NIC hardware by manufacturer | Assigned logically via static configuration or DHCP |
| **Primary Device** | Switches (build MAC Address tables) | Routers (build Routing tables) |

---

### 4.3 Network Performance Concepts

* **Bandwidth:** The theoretical maximum data carrying capacity of a network connection under ideal conditions (e.g., a 1 Gbps interface link).
* **Throughput:** The actual measured rate of successful data delivery across a network over time, reduced by protocol overhead, hardware processing, and network congestion.
* **Latency:** The total time delay taken for a data packet to travel from its source origin to its destination point, measured in milliseconds (ms).

| Term | Operational Meaning | Measurement Metric |
| :--- | :--- | :--- |
| **Bandwidth** | Maximum theoretical speed limit of a link | Mbps or Gbps |
| **Throughput** | Actual speed of useful data payload transferred | Mbps or Gbps |
| **Latency** | Delay time spent in transit across the path | Milliseconds (ms) |

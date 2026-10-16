# Networking-Lesson-1---Networking basics
#### What is a computer network?
A computer network is an interconnected group of digital devices—ranging from desktop PCs, servers, and smartphones to networking hardware like routers and switches—linked together through wired media (such as Ethernet or fiber-optic cables) or wireless transmission (such as Wi-Fi or cellular networks). 

Instead of operating as isolated systems (standalone units), networked devices follow standardized communication protocols (such as TCP/IP) that govern how information is formatted, addressed, transmitted, routed, and received across the network infrastructure.

---

#### Why do devices communicate?
In modern computing, isolated computers are severely limited in utility. Devices communicate to break down physical boundaries, enabling seamless interaction between users, automated system-to-system data transfers, and distributed computing operations.

Without network communication, every computer would require its own dedicated peripherals, local storage for all files, and physical media (like USB drives) to transfer information manually between systems.

---

#### Core Reasons for Communication

##### 1. Data Sharing
Networks eliminate the need for manual file transfers via physical storage media.
* **Direct File Transfer:** Moving files between systems over protocols like SMB, FTP, or SSH.
* **Centralized Data Access:** Storing files in central repositories (databases, NAS devices, or cloud servers) so multiple users can read or update information simultaneously.
* **Real-time Synchronization:** Keeping application data, user profiles, and system backups synchronized across multiple endpoints.

##### 2. Communication
Networks serve as the underlying foundation for human-to-human and machine-to-machine interaction.
* **Messaging & Mail:** Transferring text communications via SMTP, IMAP, and instant messaging protocols.
* **Voice & Video:** Streaming real-time audio and video traffic using VoIP (Voice over IP) and RTP (Real-time Transport Protocol).
* **Machine Communication:** Telemetry, API requests, and system alerts sent between microservices or IoT endpoints.

##### 3. Resource Sharing
Networks allow expensive or high-capacity hardware and software assets to be pooled and shared among many users, maximizing utilization and reducing costs.
* **Hardware Resources:** Sharing centralized physical equipment like high-speed network printers, storage arrays, and high-performance computing clusters.
* **Software Resources:** Hosting centralized applications, databases, and licenses on network servers rather than installing individual instances on every workstation.
* **Internet Connection Sharing:** Routing hundreds of internal devices through a single gateway router and shared ISP connection.

---

#### Basic Example

Consider a small office environment containing **5 employee laptops**, **1 network printer**, **1 local storage server (NAS)**, and **1 Wi-Fi router**:

1. **The Setup:** The 5 laptops connect wirelessly to the Wi-Fi router. The router connects via Ethernet cable to both the printer and the storage server.
2. **Data Sharing in Action:** Employee A saves a project report directly to the storage server. Employee B opens that exact same report from their own laptop seconds later to review it.
3. **Communication in Action:** Employee A sends an internal instant message to Employee B over the local network to confirm the report is ready.
4. **Resource Sharing in Action:** Employee B clicks "Print" on their laptop. The print job travels across the local network to the shared office printer, eliminating the need for 5 separate printers on every des




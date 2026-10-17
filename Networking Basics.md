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

Consider a small office environment containing **5 employee PC**, **1 network printer**, **1 local storage server (NAS)**, and **1 Wi-Fi router**:
| Device | Packet Tracer Device | Quantity |
| :--- | :--- | :--- |
| Wi-Fi router | Wireless Router (e.g. WRT300N) | 1 |
| Employee PC | PC-PT | 5 |
| Storage server | Server-PT | 1 |
| Network printer | Printer-PT | 1 |
<img width="1018" height="470" alt="Component" src="https://github.com/user-attachments/assets/95e70b57-fb30-449c-9135-6c75d25bc2a1" />
<img width="558" height="332" alt="Connect" src="https://github.com/user-attachments/assets/ff080247-3221-41bd-8b7f-d2193f833723" />

1. **The Setup:** The 5 pc connect wirelessly to the Wi-Fi router. The router connects via Ethernet cable to both the printer and the storage server.
   1. Click the WRT300N router and open the GUI tab.
   2. Use DHCP to automatically assigns IP addresses to PCs when they join the network, so we do not need to configure every PC manually
<img width="639" height="590" alt="WiFi Router Setup 1" src="https://github.com/user-attachments/assets/dfc0bd70-1a5b-4e5f-85e9-cca29e1b93aa" />
<img width="556" height="239" alt="WiFi Router Setup 2" src="https://github.com/user-attachments/assets/fc4247a3-9abb-4039-b9c2-5b8dcd544d58" />
<img width="582" height="343" alt="WiFi Router Setup 3" src="https://github.com/user-attachments/assets/b3c9381f-2950-4c0a-a94e-eaa78b689b67" />
   3. Click a PC and open the Physical tab.
   4. Turn the PC off using its power button.
   5. Replace its Ethernet module with the WPC300N wireless module, if the module is available.
   6. Turn the PC back on.
   7. Open Desktop → PC Wireless or Config → Wireless, depending on our Packet Tracer version.
   8. Connect to OfficeWiFi and enter the Wi-Fi passphrase.
   9. Open Desktop → IP Configuration and select DHCP
<img width="182" height="87" alt="PC Setup 1" src="https://github.com/user-attachments/assets/16c05804-0fe5-493f-9354-119e3d6b774f" />
<img width="671" height="310" alt="PC Setup 2" src="https://github.com/user-attachments/assets/89f19634-0f80-4164-b07a-30ec6aff3f4f" />

3. **Data Sharing in Action:** PC0 saves a project report directly to the storage server. PC1 opens that exact same report from their own pc seconds later to review it.
   1. Click the server and open the Services tab.
   2. Select FTP from the service list.
   3. Turn the FTP service On.
   4. Create a user account, for examples PC0, and set a password. Enable the required file permissions.
   5. Repeat for others PC to demonstrate separate users' accounts.
   6. On PC0, open Desktop → Command Prompt and enter: ''ftp 192.168.1.10''
   7. Log in with the FTP username and password you configured.
   8. To upload a text file from the PC to the server, use: ''put report.txt''
<img width="760" height="509" alt="Setup FTP" src="https://github.com/user-attachments/assets/f88d3794-78a1-4dd3-a046-a7db717e4662" />
<img width="534" height="250" alt="Send FTP" src="https://github.com/user-attachments/assets/1df2a697-06e4-4ac4-80e3-c9daff27172d" />
<img width="514" height="151" alt="Sending Files" src="https://github.com/user-attachments/assets/aa827dd4-65ad-4d5b-ab82-97a26640f22c" />
    9. On PC1, connect to the same server: ''ftp 192.168.1.10''
   10. After logging in, retrieve the uploaded file: ''get report.txt''
<img width="406" height="326" alt="Gettiing Files" src="https://github.com/user-attachments/assets/c978368b-70a4-4a0c-a3fe-772d8b29a699" />

5. **Communication in Action:** PC0 sends an internal instant message to PC1 over the local network to confirm the report is ready.
<img width="809" height="112" alt="Simple PDU Check" src="https://github.com/user-attachments/assets/4f6254fc-01cb-43dc-aeb6-88bd7f1fa2bf" />






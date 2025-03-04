# Networking Fundamentals  
## Contents  
## Introduction  
Suppose we have some divided networks, our home network and a company network. To send a packet to the company network, our **router** is used to send the packet to the **ISP**, the ISP looks in the **DNS** to locate the company network and returns the **IP address**. Now as the IP address is known, our packet is sent directly to the company network via the ISP. The web server (company's) receives our packet with the request of what their website looks like, then it sends us back the packet with the data for the presentation of the website via the router of the company network to our IP address.  
## Network Types  
- Wide Area Network (WAN) - Internet  
  - Just a large number of LANs joined together. Many companies and govt. agencies will have an "Internal WAN" (Intranet)  
  - The primary way we identify if the network is a WAN is to use a WAN Specific routing protocol such as BGP and if the IP Schema in use is not within RFC 1918 (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16)
- Local Area Network (LAN) - Internal Networks (eg. Home or Office)  
- Wireless Local Area Network (WLAN) - Internal Networks accessible over Wi-Fi  
- Virtual Private Network (VPN) - Connects multiple network sites to one LAN  
- Global Area Network (GAN) - Internet (Book term)  
- Metropolitan Area Network (MAN) - Regional Network; multiple LANs (book term)  
- Wireless Personal Area Network (WPAN) - Personal Network; Bluetooth (book term)  
## Network Topologies  
- Connections  
  - Wireless Connections - Wi-Fi, Cellular, Satellite, and others  
  - Wired Connections - Coaxial cabling, Glass fiber cabling, Twisted-pair cabling, and others  
- Nodes - Network Interface Controller (NICs)  
  - Routers/Modems, Gateways, Firewalls, Switches
- Classifications  
  - 8 types of Network topologies - **Point-to-point, Star, Ring, Mesh, Bus, Hybrid, Daisy Chain, Tree**  
## Proxies  
- Common misconception that whenever an IP address changes, it is a proxy. However, A proxy is when a device or service sits in the middle of a connection and acts as a mediator. The mediator must be able to inspect the contents of the traffic. Without the ability to be a mediator, the device is technically a **gateway**, not a proxy.  
- The key types of proxies are -  
  - Dedicated Proxy / Forward Proxy 
    - Makes a request to a computer, computer carries out the request (eg. web filters in a corporate network for sensitive computers)  
    - Web browsers (like IE, Chrome, Edge, etc.) all obey the "System Proxy" settings by default. If the malware utilizes WinSock, it will likely be proxy aware without any additional code.  
    - If the org. only utilizes Firefox, it is highly improbable to get a proxy-aware malware as Firefox uses libcurl, and not WinSock.  
  - Reverse Proxy  
    - Filters incoming requests, opposite of Forward Proxy  
    - CloudFlare can withstand most DDOS attacks. Orgs. can filter the amount and type of traffic that gets sent to their webservers.  
    - Organizations may have **IDS (Intrusion Detection Systems)**, watching external web requests. If the attacker gains access to the organization over SSH, a reverse proxy can send web requests through the SSH Tunnel and evade the IDS.  
  - Transparent Proxy  
    - Client does not know about the existence of the proxy.  
    - Intercepts the client's connection request to the Internet and acts as a substitute instance.  
  - Non-Transparent Proxy  
    - We must be informed about the existence of the proxy.  
    - We and the software we want to use are given a special proxy config. that ensures the traffic to the Internet is first addressed by the proxy.  
## Networking Models  
### OSI Model  
  - Ref model that can be used to define and describe the communication between systems.  
  - Layers  
    - 7. Application Layer  
      - FTP, HTTP  
    - 6. Presentation Layer  
      - JPG, PNG, SSL, TLS  
    - 5. Session Layer  
      - NetBIOS  
    - 4. Transport Layer  
      - TCP, UDP  
    - 3. Network Layer  
      - Router, L3 Switch  
    - 2. Data-Link Layer  
      - Switch, Bridge  
    - 1. Physical Layer  
      - Network Card  
  - Layers 1 to 3 are media layers and 4 to 7 are host layers.  
### TCP/IP Model  
  - TCP/IP generic term for many network protocols.  
  - The protocols are responsible for the switching and transfer of data packets on the Internet.  
  - Name for entire protocol family, not just TCP and IP.  
  - Layers  
    - 4. Application  
    - 3. Transport  
    - 2. Internet  
    - 1. Link  
  - IP ensures that the data packet reaches its destination, and TCP controls the data transfer and ensures the connection between data stream and application.  
  - The main difference between TCP/IP and OSI is the number of layers, some of which have been combined.  
  - IP takes over the **logical addressing** of networks and nodes.  
  - Important tasks of TCP/IP  
    - Logical addressing(IP)  
    - Routing(IP)  
    - Error & Control Flow(TCP)  
    - Application Support(TCP)  
    - Name Resolution(DNS)  
### IP Addresses  
  - Within a single network, MAC address is enough for data exchange between hosts. However, if a host is on another network, the MAC address is not enough to establish a connection.  
  - Addressing on the internet is done via the IPv4 and/or IPv6 address, which is made up of the network address and the host address.  
  - 32-bit binary number combined into 4 bytes consisting of 8-bit groups ranging from 0-255.  
## Tools  
- Intrusion Detection Systems  
  - Suricata  
  - Snort  
- DNS Monitoring  
  - Sysmon  
- Proxies  
  - BurpSuite (Swiss army knife of HTTP Proxies, can be used to forward HTTP requests, can be configured to be a reverse proxy or transparent)  
## Networking Attacks  
- Spoofing  
- Man in the middle  
## Abbreviations  
- FQDN - Fully Qualified Domain Name (eg. www.hackthebox.eu)  
- URL - Uniform Resource Locator (eg. https://www.hackthebox.eu/example?floor=2&office=dev&employee=17)  
- DMZ - Demilitarized Zone  
- HTTP - HyperText Transfer Protocol  
- HTTPS - HyperText Transfer Protocol Secure (adds a layer of encryption to HTTP using SSL and TLS to protect the data being transferred)  
- OSI - Open Systems Interconnection  
- TCP - Transmission Control Protocol  
- IP - Internet Protocol  
- ICMP - Internet Control Message Protocol  
- UDP - User Datagram Protocol  
- MAC - Media Access Control  

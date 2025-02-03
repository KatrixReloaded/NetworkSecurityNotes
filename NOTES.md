# Networking Fundamentals  
## Contents  
## Introduction  
Suppose we have some divided networks, our home network and a company network. To send a packet to the company network, our router is used to send the packet to the ISP, the ISP looks in the DNS to locate the company network and returns the IP address. Now as the IP address is known, our packet is sent directly to the company network via the ISP. The web server (company's) receives our packet with the request of what their website looks like, then it sends us back the packet with the data for the presentation of the website via the router of the company network to our IP address.  
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
    - Bus Topology - No central network, all hosts connected to a transmission medium, one host sends, others receive.  
    - Star Topology - 
## Tools  
- Intrusion Detection Systems  
  - Suricata  
  - Snort  
## Networking Attacks  
- Spoofing  
- Man in the middle  
## Abbreviations  
- FQDN - Fully Qualified Domain Name (eg. www.hackthebox.eu)  
- URL - Uniform Resource Locator (eg. https://www.hackthebox.eu/example?floor=2&office=dev&employee=17)  
- DMZ - Demilitarized Zone  
- HTTP - HyperText Transfer Protocol  
- HTTPS - HyperText Transfer Protocol Secure (adds a layer of encryption to HTTP using SSL and TLS to protect the data being transferred)  
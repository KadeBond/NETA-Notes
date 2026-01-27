# CCNA Complete Study Notes
## Comprehensive Networking Fundamentals

---

## 1. Historical Development of Networking Technologies

### Early Computer Connections (1960s-1970s)
- **ARPANET (1969)**: First packet-switching network, precursor to the Internet
- **Mainframe terminals**: Dumb terminals connected to central mainframes
- **Point-to-point connections**: Direct cable connections between computers
- **Circuit switching**: Dedicated communication paths (telephone-based)

### The Ethernet Revolution (1970s-1980s)
- **Ethernet (1973)**: Developed by Xerox PARC, became IEEE 802.3 standard
- **CSMA/CD**: Carrier Sense Multiple Access with Collision Detection
- **Coaxial cable networks**: 10BASE5 (Thicknet) and 10BASE2 (Thinnet)
- **Token Ring**: IBM's alternative topology using token-passing

### Internet Protocol Suite (1980s)
- **TCP/IP standardization (1983)**: ARPANET switches to TCP/IP
- **DNS (1984)**: Domain Name System replaces host files
- **Fiber optic deployment**: Higher bandwidth, longer distances

### Modern Era Milestones (1990s-Present)

#### Wi-Fi Evolution
- **802.11 (1997)**: Original wireless standard, 2 Mbps
- **802.11b (1999)**: 11 Mbps, 2.4 GHz
- **802.11g (2003)**: 54 Mbps, 2.4 GHz
- **802.11n (2009)**: 600 Mbps, MIMO technology
- **802.11ac (2013)**: Gigabit speeds, 5 GHz
- **802.11ax/Wi-Fi 6 (2019)**: Improved efficiency, multi-user MIMO

#### Mobile Networks
- **1G (1980s)**: Analog voice
- **2G (1991)**: Digital voice, SMS
- **3G (2001)**: Mobile data, 2 Mbps
- **4G/LTE (2009)**: 100+ Mbps, all-IP networks
- **5G (2019)**: 10+ Gbps, ultra-low latency, IoT support

#### Cloud Computing & Modern Technologies
- **Virtualization**: Multiple VMs on single hardware
- **Cloud services**: AWS (2006), Azure, Google Cloud
- **Software-Defined Networking (SDN)**: Programmable networks
- **Network Function Virtualization (NFV)**: Software-based network services

### Impact on Society

#### Communication
- Real-time global connectivity
- Video conferencing and remote collaboration
- Social media and instant messaging
- VoIP replacing traditional telephony

#### Business Transformation
- E-commerce and digital marketplaces
- Remote work and distributed teams
- Big data analytics and AI
- Supply chain optimization

#### Everyday Life
- Smart homes and IoT devices
- Streaming entertainment
- Mobile banking and payments
- Telemedicine and online education

### Comparison: Then vs. Now

| Aspect | Early Networks (1970s-1990s) | Modern Networks (2020s) |
|--------|------------------------------|-------------------------|
| **Speed** | 10 Mbps Ethernet | 100 Gbps+ fiber, 10 Gbps Wi-Fi 6E |
| **Reliability** | Frequent collisions, limited redundancy | 99.999% uptime, automatic failover |
| **Accessibility** | Expensive, institutional use | Ubiquitous, affordable consumer access |
| **Distance** | Limited by cable length | Global via satellite and submarine cables |
| **Security** | Minimal encryption | Advanced encryption, zero-trust models |

### Future Innovations & IT Careers
- **6G networks**: Terabit speeds, holographic communications
- **Quantum networking**: Unhackable communications
- **AI-driven network management**: Self-healing networks
- **Career paths**: Network engineer, security analyst, cloud architect, IoT specialist

---

## 2. OSI and TCP/IP Models

### OSI Model (Open Systems Interconnection)

The OSI model is a **conceptual framework** with 7 layers that standardizes network communication functions.

#### Layer 7: Application
- **Function**: User interface, network services to applications
- **Protocols**: HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS, DHCP, TFTP, Telnet, SSH
- **Data Unit**: Data
- **Devices**: Firewalls, application gateways
- **Example**: Web browser requesting a webpage

#### Layer 6: Presentation
- **Function**: Data translation, encryption, compression
- **Protocols**: SSL/TLS, JPEG, GIF, MPEG, ASCII, EBCDIC
- **Data Unit**: Data
- **Example**: Encrypting data before transmission

#### Layer 5: Session
- **Function**: Establishes, manages, terminates sessions
- **Protocols**: NetBIOS, RPC, PPTP, SAP
- **Data Unit**: Data
- **Example**: Maintaining a login session

#### Layer 4: Transport
- **Function**: End-to-end connections, reliability, flow control
- **Protocols**: TCP (connection-oriented), UDP (connectionless)
- **Data Unit**: Segment (TCP) / Datagram (UDP)
- **Port numbers**: Source and destination ports
- **Example**: TCP three-way handshake

#### Layer 3: Network
- **Function**: Logical addressing, routing, path determination
- **Protocols**: IP (IPv4/IPv6), ICMP, OSPF, EIGRP, BGP, ARP
- **Data Unit**: Packet
- **Devices**: Routers, Layer 3 switches
- **Addressing**: IP addresses
- **Example**: Router forwarding packet to next hop

#### Layer 2: Data Link
- **Function**: Physical addressing, error detection, frame formatting
- **Protocols**: Ethernet (802.3), Wi-Fi (802.11), PPP, HDLC
- **Data Unit**: Frame
- **Devices**: Switches, bridges, NICs
- **Addressing**: MAC addresses (48-bit)
- **Sublayers**: LLC (Logical Link Control), MAC (Media Access Control)
- **Example**: Switch forwarding frame based on MAC address table

#### Layer 1: Physical
- **Function**: Transmits raw bits over physical medium
- **Specifications**: Cables, voltages, frequencies, pin layouts
- **Data Unit**: Bits
- **Devices**: Hubs, repeaters, cables, connectors
- **Media**: Copper (UTP, STP), fiber optic, wireless
- **Example**: Electrical signal representing a binary 1 or 0

### TCP/IP Model (Internet Protocol Suite)

A **practical 4-layer model** that forms the foundation of the Internet.

#### Layer 4: Application
- **Corresponds to**: OSI Layers 5, 6, 7
- **Protocols**: HTTP, FTP, DNS, SMTP, SSH, Telnet
- **Function**: Combines application, presentation, and session functions

#### Layer 3: Transport
- **Corresponds to**: OSI Layer 4
- **Protocols**: TCP, UDP
- **TCP characteristics**: Connection-oriented, reliable, flow control, ordered delivery
- **UDP characteristics**: Connectionless, faster, no guarantees, used for streaming/gaming

#### Layer 2: Internet
- **Corresponds to**: OSI Layer 3
- **Protocols**: IP, ICMP, ARP, IGMP
- **Function**: Logical addressing and routing

#### Layer 1: Network Access (Link)
- **Corresponds to**: OSI Layers 1, 2
- **Function**: Combines physical and data link functions
- **Protocols**: Ethernet, Wi-Fi, PPP

### Data Flow Through the Layers

#### Encapsulation (Sending Data)
1. **Application Layer**: User data created
2. **Transport Layer**: Adds TCP/UDP header (source/destination ports) → Segment
3. **Network Layer**: Adds IP header (source/destination IP) → Packet
4. **Data Link Layer**: Adds Ethernet header and trailer (MAC addresses, FCS) → Frame
5. **Physical Layer**: Converts to bits and transmits

#### De-encapsulation (Receiving Data)
1. **Physical Layer**: Receives bits
2. **Data Link Layer**: Checks FCS, reads MAC address, strips header → Packet
3. **Network Layer**: Reads IP address, strips header → Segment
4. **Transport Layer**: Checks ports, strips header → Data
5. **Application Layer**: Presents data to application

### Protocol Matching Exercise

| Protocol | Layer (OSI) | Layer (TCP/IP) | Function |
|----------|-------------|----------------|----------|
| HTTP/HTTPS | 7 - Application | Application | Web traffic |
| FTP | 7 - Application | Application | File transfer |
| SMTP | 7 - Application | Application | Email sending |
| DNS | 7 - Application | Application | Name resolution |
| DHCP | 7 - Application | Application | IP address assignment |
| SSH | 7 - Application | Application | Secure remote access |
| Telnet | 7 - Application | Application | Unsecure remote access |
| TFTP | 7 - Application | Application | Trivial file transfer |
| SSL/TLS | 6 - Presentation | Application | Encryption |
| TCP | 4 - Transport | Transport | Reliable delivery |
| UDP | 4 - Transport | Transport | Fast, unreliable delivery |
| IP | 3 - Network | Internet | Logical addressing |
| ICMP | 3 - Network | Internet | Error reporting (ping) |
| OSPF | 3 - Network | Internet | Dynamic routing |
| EIGRP | 3 - Network | Internet | Dynamic routing (Cisco) |
| ARP | 3 - Network | Internet | IP to MAC resolution |
| Ethernet | 2 - Data Link | Network Access | LAN framing |
| Wi-Fi (802.11) | 2 - Data Link | Network Access | Wireless LAN |
| PPP | 2 - Data Link | Network Access | Point-to-point WAN |

---

## 3. IPv4 Addressing

### Definition and Purpose
- **IP address**: Unique logical identifier for devices on a network
- **32-bit address**: Written in dotted decimal notation (e.g., 192.168.1.1)
- **Two parts**: Network portion + Host portion
- **Subnet mask**: Distinguishes network from host bits

### IPv4 vs. IPv6 (Brief Contrast)

| Feature | IPv4 | IPv6 |
|---------|------|------|
| **Address size** | 32 bits | 128 bits |
| **Address format** | Decimal (192.168.1.1) | Hexadecimal (2001:db8::1) |
| **Total addresses** | ~4.3 billion | 340 undecillion |
| **Header** | Variable length | Fixed length |
| **Configuration** | Manual or DHCP | SLAAC, DHCPv6 |

### IPv4 Address Classes

#### Class A
- **Range**: 1.0.0.0 to 126.0.0.0
- **First bit**: 0
- **Default mask**: 255.0.0.0 (/8)
- **Networks**: 126 (0 and 127 reserved)
- **Hosts per network**: 16,777,214
- **Use**: Very large organizations, ISPs

#### Class B
- **Range**: 128.0.0.0 to 191.255.0.0
- **First bits**: 10
- **Default mask**: 255.255.0.0 (/16)
- **Networks**: 16,384
- **Hosts per network**: 65,534
- **Use**: Medium to large organizations

#### Class C
- **Range**: 192.0.0.0 to 223.255.255.0
- **First bits**: 110
- **Default mask**: 255.255.255.0 (/24)
- **Networks**: 2,097,152
- **Hosts per network**: 254
- **Use**: Small organizations, home networks

#### Class D (Multicast)
- **Range**: 224.0.0.0 to 239.255.255.255
- **First bits**: 1110
- **Use**: Multicast groups (one-to-many communication)
- **Not assigned to hosts**

#### Class E (Experimental)
- **Range**: 240.0.0.0 to 255.255.255.255
- **First bits**: 1111
- **Use**: Reserved for experimental purposes

### Private vs. Public Addresses

#### Private Address Ranges (RFC 1918)
- **Class A**: 10.0.0.0 to 10.255.255.255 (/8)
- **Class B**: 172.16.0.0 to 172.31.255.255 (/12)
- **Class C**: 192.168.0.0 to 192.168.255.255 (/16)
- **Usage**: Internal networks, not routable on Internet
- **NAT required**: To access Internet

#### Public Addresses
- All other addresses (except special ranges)
- Globally routable
- Must be unique on Internet
- Assigned by IANA/RIRs

### Special Addresses

| Address | Purpose |
|---------|---------|
| **0.0.0.0** | Default route, "this network" |
| **127.0.0.0 - 127.255.255.255** | Loopback (127.0.0.1 commonly used) |
| **169.254.0.0/16** | APIPA (Automatic Private IP Addressing) |
| **255.255.255.255** | Limited broadcast |
| **Network address** | First address in subnet (all host bits 0) |
| **Broadcast address** | Last address in subnet (all host bits 1) |

### Binary and Decimal Representation

#### Decimal to Binary Conversion
Each octet represents 8 bits with positional values:
```
128  64  32  16   8   4   2   1
```

**Example: Convert 192 to binary**
- 192 = 128 + 64
- Binary: 11000000

**Example: 168.192.5.10 in binary**
- 168 = 10101000
- 192 = 11000000
- 5 = 00000101
- 10 = 00001010
- **Result**: 10101000.11000000.00000101.00001010

#### Binary to Decimal Conversion
**Example: 11000000 to decimal**
- 1×128 + 1×64 + 0×32 + 0×16 + 0×8 + 0×4 + 0×2 + 0×1
- = 128 + 64 = **192**

### Subnet Masks

#### Common Subnet Masks
| CIDR | Decimal | Binary (last octet) | Hosts |
|------|---------|---------------------|-------|
| /8 | 255.0.0.0 | N/A | 16,777,214 |
| /16 | 255.255.0.0 | N/A | 65,534 |
| /24 | 255.255.255.0 | 11111111 | 254 |
| /25 | 255.255.255.128 | 10000000 | 126 |
| /26 | 255.255.255.192 | 11000000 | 62 |
| /27 | 255.255.255.224 | 11100000 | 30 |
| /28 | 255.255.255.240 | 11110000 | 14 |
| /29 | 255.255.255.248 | 11111000 | 6 |
| /30 | 255.255.255.252 | 11111100 | 2 |

#### Calculating Network and Host Portions
**Formula**: Usable hosts = 2^(host bits) - 2

**Example: 192.168.1.0/26**
- Subnet mask: 255.255.255.192
- Network bits: 26
- Host bits: 32 - 26 = 6
- Usable hosts: 2^6 - 2 = 62

### Subnetting

#### Fixed-Length Subnet Mask (FLSM)
All subnets use same size mask.

**Example: Subnet 192.168.1.0/24 into 4 subnets**
- Need 2 bits (2^2 = 4 subnets)
- New mask: /26 (255.255.255.192)
- Block size: 256 - 192 = 64

| Subnet # | Network Address | First Host | Last Host | Broadcast |
|----------|----------------|------------|-----------|-----------|
| 1 | 192.168.1.0 | 192.168.1.1 | 192.168.1.62 | 192.168.1.63 |
| 2 | 192.168.1.64 | 192.168.1.65 | 192.168.1.126 | 192.168.1.127 |
| 3 | 192.168.1.128 | 192.168.1.129 | 192.168.1.190 | 192.168.1.191 |
| 4 | 192.168.1.192 | 192.168.1.193 | 192.168.1.254 | 192.168.1.255 |

#### Variable-Length Subnet Mask (VLSM)
Subnets can use different size masks for efficiency.

**Example: Given 172.16.0.0/16, create subnets for:**
- Network A: 8000 hosts
- Network B: 4000 hosts
- Network C: 2000 hosts
- Network D: 1000 hosts

**Solution (largest to smallest):**

1. **Network A (8000 hosts)**
   - Need: 2^13 - 2 = 8190 hosts
   - Use: /19 (255.255.224.0)
   - Network: 172.16.0.0/19
   - Range: 172.16.0.1 - 172.16.31.254

2. **Network B (4000 hosts)**
   - Need: 2^12 - 2 = 4094 hosts
   - Use: /20 (255.255.240.0)
   - Network: 172.16.32.0/20
   - Range: 172.16.32.1 - 172.16.47.254

3. **Network C (2000 hosts)**
   - Need: 2^11 - 2 = 2046 hosts
   - Use: /21 (255.255.248.0)
   - Network: 172.16.48.0/21
   - Range: 172.16.48.1 - 172.16.55.254

4. **Network D (1000 hosts)**
   - Need: 2^10 - 2 = 1022 hosts
   - Use: /22 (255.255.252.0)
   - Network: 172.16.56.0/22
   - Range: 172.16.56.1 - 172.16.59.254

### Configuring IPv4 Addresses

#### Cisco Router Configuration
```
Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
```

#### Cisco Switch Configuration
```
Switch(config)# interface vlan 1
Switch(config-if)# ip address 192.168.1.2 255.255.255.0
Switch(config-if)# no shutdown
Switch(config-if)# exit
Switch(config)# ip default-gateway 192.168.1.1
```

#### Windows PC (Command Prompt)
```
netsh interface ip set address "Ethernet" static 192.168.1.10 255.255.255.0 192.168.1.1
```

#### Verification Commands
- **Cisco**: `show ip interface brief`, `show running-config`
- **Windows**: `ipconfig /all`
- **Linux**: `ip addr show` or `ifconfig`
- **Test connectivity**: `ping 192.168.1.1`

### Troubleshooting IPv4 Addressing

#### Common Issues

1. **Wrong Subnet Mask**
   - Symptom: Can't communicate with some devices
   - Solution: Verify all devices on subnet use same mask

2. **Duplicate IP Address**
   - Symptom: Intermittent connectivity, error messages
   - Solution: Use DHCP or maintain IP address documentation

3. **Incorrect Default Gateway**
   - Symptom: Can ping local devices but not remote networks
   - Solution: Verify gateway IP and that it's on same subnet

4. **Mismatched Network/Host Portions**
   - Symptom: Devices can't see each other
   - Solution: Ensure IP addresses are in same subnet

5. **APIPA Assignment (169.254.x.x)**
   - Symptom: No network connectivity
   - Cause: DHCP server unavailable
   - Solution: Check DHCP server, cables, switch ports

#### Structured Troubleshooting Approach

1. **Identify the problem**
   - Gather symptoms
   - Question users
   - Document issue

2. **Establish theory of probable cause**
   - Start with obvious (cables, power)
   - Check configuration
   - Review recent changes

3. **Test theory**
   - Use ping, traceroute, ipconfig
   - Check LED indicators
   - Verify physical connections

4. **Establish action plan**
   - Determine solution
   - Consider impact

5. **Implement solution**
   - Make changes methodically
   - Document changes

6. **Verify functionality**
   - Test connectivity
   - Ensure issue resolved

7. **Document findings**
   - Record problem and solution
   - Update network documentation

---

## 4. Building Small Networks

### Network Components

#### End Devices (Hosts)
- **Computers**: Workstations, laptops
- **Servers**: File, web, email, DHCP, DNS servers
- **Printers**: Network-connected printers
- **Mobile devices**: Smartphones, tablets
- **IoT devices**: IP cameras, sensors

#### Intermediary Devices
- **Routers**: Connect different networks, route traffic, operate at Layer 3
- **Switches**: Connect devices within a network, forward frames, operate at Layer 2
- **Wireless Access Points (APs)**: Provide wireless connectivity
- **Firewalls**: Security devices, filter traffic

#### Network Media
- **Copper cables**
  - UTP (Unshielded Twisted Pair): Cat5e, Cat6, Cat6a
  - STP (Shielded Twisted Pair): Better EMI protection
- **Fiber optic cables**
  - Single-mode: Long distances (100+ km)
  - Multi-mode: Shorter distances, cheaper
- **Wireless**: Radio frequencies (2.4 GHz, 5 GHz, 6 GHz)

### Cable Types and Standards

#### Ethernet Cables
- **Straight-through**: Router to switch, switch to PC
- **Crossover**: Switch to switch, PC to PC, router to router (older devices)
- **Rollover/Console**: Connecting to console port for configuration

#### Cable Standards
| Standard | Speed | Max Distance | Cable Type |
|----------|-------|--------------|------------|
| 10BASE-T | 10 Mbps | 100m | Cat3 UTP |
| 100BASE-TX | 100 Mbps | 100m | Cat5 UTP |
| 1000BASE-T | 1 Gbps | 100m | Cat5e/Cat6 |
| 10GBASE-T | 10 Gbps | 100m | Cat6a |

### Physical Setup of a LAN

#### Basic LAN Topology
```
Internet
   |
Router (Default Gateway)
   |
Switch (Central connecting device)
   |---- PC1
   |---- PC2
   |---- PC3
   |---- Server
   |---- Printer
```

#### Setup Steps
1. **Plan IP addressing scheme**
   - Choose network (e.g., 192.168.1.0/24)
   - Assign router: 192.168.1.1
   - Assign devices: 192.168.1.10-254

2. **Physical connections**
   - Connect router WAN port to ISP modem
   - Connect router LAN port to switch
   - Connect devices to switch ports
   - Connect power to all devices

3. **Verify LED indicators**
   - Link lights: Solid green = good connection
   - Activity lights: Blinking = traffic passing
   - Speed indicators: Different colors for 10/100/1000

### Basic Device Configuration

#### Router Basic Configuration
```
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)# enable secret cisco123
R1(config)# line console 0
R1(config-line)# password console123
R1(config-line)# login
R1(config-line)# exit
R1(config)# line vty 0 4
R1(config-line)# password telnet123
R1(config-line)# login
R1(config-line)# exit
R1(config)# service password-encryption
R1(config)# banner motd # Unauthorized access prohibited #
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# description Link to Switch
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# exit
R1# copy running-config startup-config
```

#### Switch Basic Configuration
```
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1
S1(config)# enable secret cisco123
S1(config)# line console 0
S1(config-line)# password console123
S1(config-line)# login
S1(config-line)# exit
S1(config)# line vty 0 15
S1(config-line)# password telnet123
S1(config-line)# login
S1(config-line)# exit
S1(config)# service password-encryption
S1(config)# banner motd # Authorized access only #
S1(config)# interface vlan 1
S1(config-if)# ip address 192.168.1.2 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# exit
S1(config)# ip default-gateway 192.168.1.1
S1(config)# exit
S1# copy running-config startup-config
```

### IP Address Assignment Methods

#### Static IP Configuration
- **Advantages**: Predictable, good for servers, network devices
- **Disadvantages**: Time-consuming, prone to errors
- **Best for**: Servers, routers, switches, printers

**Windows static configuration:**
```
Control Panel > Network and Sharing Center > Change adapter settings
Right-click adapter > Properties > IPv4 > Properties
Select "Use the following IP address"
IP address: 192.168.1.10
Subnet mask: 255.255.255.0
Default gateway: 192.168.1.1
DNS: 8.8.8.8
```

#### Dynamic IP Configuration (DHCP)
- **Advantages**: Automatic, reduces errors, easy to manage large networks
- **Disadvantages**: Addresses can change
- **Best for**: Workstations, mobile devices, guest devices

**DHCP Process (DORA)**:
1. **Discover**: Client broadcasts DHCP Discover message
2. **Offer**: DHCP server offers IP address
3. **Request**: Client requests offered address
4. **Acknowledge**: Server confirms assignment

**Router as DHCP Server:**
```
R1(config)# ip dhcp excluded-address 192.168.1.1 192.168.1.10
R1(config)# ip dhcp pool LAN-POOL
R1(dhcp-config)# network 192.168.1.0 255.255.255.0
R1(dhcp-config)# default-router 192.168.1.1
R1(dhcp-config)# dns-server 8.8.8.8
R1(dhcp-config)# exit
```

### Testing and Verification

#### Essential Commands

**Ping (ICMP Echo Request/Reply)**
- Tests connectivity to another device
- Shows round-trip time and packet loss
```
C:\> ping 192.168.1.1
C:\> ping google.com
```

**Ipconfig (Windows)**
```
ipconfig                    # Shows basic IP configuration
ipconfig /all              # Shows detailed configuration
ipconfig /release          # Releases DHCP lease
ipconfig /renew            # Requests new DHCP lease
ipconfig /flushdns         # Clears DNS cache
```

**Traceroute/Tracert**
- Shows path packets take to destination
```
C:\> tracert google.com
```

**Cisco IOS Commands**
```
show ip interface brief       # Shows all interfaces and IP addresses
show running-config           # Shows current configuration
show startup-config           # Shows saved configuration
show interfaces               # Detailed interface information
show ip route                 # Shows routing table
show mac address-table        # Shows MAC address table (switch)
```

### Troubleshooting Connectivity Issues

#### Systematic Approach

1. **Check physical layer**
   - Cables connected?
   - LED indicators working?
   - Power on?

2. **Verify IP configuration**
   - Correct IP address?
   - Correct subnet mask?
   - Correct default gateway?

3. **Test local connectivity**
   - Ping default gateway
   - Ping other local devices

4. **Test remote connectivity**
   - Ping Internet address
   - Check DNS resolution

#### Common Problems and Solutions

| Problem | Symptom | Solution |
|---------|---------|----------|
| No link light | Cable unplugged or bad | Check/replace cable |
| APIPA address | Can't reach DHCP server | Check DHCP server, cables |
| Can ping gateway, not Internet | Routing/DNS issue | Check gateway configuration |
| Can ping IP but not hostname | DNS issue | Check DNS server settings |
| Intermittent connectivity | Duplex mismatch, bad cable | Check duplex settings |

---

## 5. IP Routing Fundamentals

### Purpose of IP Routing
- **Routing**: Process of forwarding packets between networks
- **Routers**: Make forwarding decisions based on routing tables
- **Goal**: Find best path from source to destination across multiple networks

### How Routers Work

#### Routing Process
1. **Receive packet** on ingress interface
2. **Check destination IP** in packet header
3. **Consult routing table** for best match
4. **Forward packet** out egress interface to next hop
5. **Repeat** at each router until destination reached

#### Routing Table Components
- **Network destination**: Destination network address
- **Subnet mask**: Identifies network portion
- **Next hop**: IP address of next router OR exit interface
- **Metric**: Cost/distance to destination
- **Administrative distance**: Trustworthiness of route source
- **Exit interface**: Local interface to forward packet

### Types of Routes

#### 1. Directly Connected Routes
- **Source**: Interface configuration
- **Symbol**: C (Cisco)
- **Administrative Distance**: 0
- **Description**: Networks directly attached to router interfaces
- **Automatic**: Added when interface configured with IP and brought up

**Example:**
```
C    192.168.1.0/24 is directly connected, GigabitEthernet0/0
```

#### 2. Static Routes
- **Source**: Manual configuration by administrator
- **Symbol**: S (Cisco)
- **Administrative Distance**: 1
- **Advantages**: No routing protocol overhead, complete control, predictable
- **Disadvantages**: Not scalable, no automatic updates, manual maintenance

**Use cases:**
- Small networks
- Stub networks (only one exit point)
- Default routes
- Route summarization

#### 3. Dynamic Routes
- **Source**: Routing protocols (OSPF, EIGRP, RIP, BGP)
- **Symbol**: O (OSPF), D (EIGRP), R (RIP), B (BGP)
- **Advantages**: Automatic updates, scales well, adapts to topology changes
- **Disadvantages**: Uses bandwidth and CPU, more complex

### Administrative Distance (AD)

Determines which route source is most trustworthy when multiple routes to same destination exist.

| Route Source | AD Value |
|--------------|----------|
| Directly Connected | 0 |
| Static Route | 1 |
| EIGRP Summary | 5 |
| External BGP | 20 |
| Internal EIGRP | 90 |
| OSPF | 110 |
| IS-IS | 115 |
| RIP | 120 |
| External EIGRP | 170 |
| Internal BGP | 200 |

**Lower AD = More trusted**

### Configuring Static Routes

#### Standard Static Route
```
R1(config)# ip route <destination-network> <subnet-mask> <next-hop-ip>
```

**Example:**
```
R1(config)# ip route 172.16.0.0 255.255.0.0 10.1.1.2
```
*To reach 172.16.0.0/16, forward to next hop 10.1.1.2*

#### Using Exit Interface
```
R1(config)# ip route 172.16.0.0 255.255.0.0 GigabitEthernet0/1
```

#### Fully Specified Static Route (both next-hop and exit interface)
```
R1(config)# ip route 172.16.0.0 255.255.0.0 GigabitEthernet0/1 10.1.1.2
```
*Useful for point-to-point links*

#### Default Static Route (Gateway of Last Resort)
```
R1(config)# ip route 0.0.0.0 0.0.0.0 <next-hop-ip>
```

**Example:**
```
R1(config)# ip route 0.0.0.0 0.0.0.0 209.165.200.1
```
*Forward all unknown traffic toward the Internet*

#### Floating Static Route (Backup Route)
```
R1(config)# ip route 172.16.0.0 255.255.0.0 10.1.1.2 5
```
*The "5" is administrative distance - higher than default static (1), so only used if primary route fails*

### Routing Table Interpretation

**Example routing table:**
```
R1# show ip route

Codes: C - connected, S - static, O - OSPF, D - EIGRP

Gateway of last resort is 209.165.200.1 to network 0.0.0.0

S*   0.0.0.0/0 [1/0] via 209.165.200.1
     10.0.0.0/8 is variably subnetted, 2 subnets
C       10.1.1.0/30 is directly connected, GigabitEthernet0/0
C       10.1.1.4/30 is directly connected, GigabitEthernet0/1
S    172.16.0.0/16 [1/0] via 10.1.1.2
C    192.168.1.0/24 is directly connected, GigabitEthernet0/2
```

**Reading an entry:**
```
S    172.16.0.0/16 [1/0] via 10.1.1.2
|    |              | |   |
|    |              | |   Next hop IP
|    |              | Metric
|    |              Administrative Distance
|    Destination network
Route type (Static)
```

### Designing an Internetwork with Static Routes

#### Sample Topology
```
Internet (0.0.0.0/0)
        |
    [ISP Router]
        |
   209.165.200.1
        |
   [R1] - 10.1.1.1/30 --- 10.1.1.2/30 - [R2]
    |                                      |
192.168.1.0/24                      172.16.0.0/16
    |                                      |
  [LAN1]                                [LAN2]
```

#### Configuration for R1:
```
R1(config)# interface g0/0
R1(config-if)# ip address 10.1.1.1 255.255.252.252
R1(config-if)# no shutdown
R1(config-if)# exit

R1(config)# interface g0/2
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit

R1(config)# ip route 172.16.0.0 255.255.0.0 10.1.1.2
R1(config)# ip route 0.0.0.0 0.0.0.0 209.165.200.1
```

#### Configuration for R2:
```
R2(config)# interface g0/0
R2(config-if)# ip address 10.1.1.2 255.255.255.252
R2(config-if)# no shutdown
R2(config-if)# exit

R2(config)# interface g0/1
R2(config-if)# ip address 172.16.0.1 255.255.0.0
R2(config-if)# no shutdown
R2(config-if)# exit

R2(config)# ip route 192.168.1.0 255.255.255.0 10.1.1.1
R2(config)# ip route 0.0.0.0 0.0.0.0 10.1.1.1
```

### Verification Commands

```
show ip route                    # Display routing table
show ip route static             # Display only static routes
show ip interface brief          # Verify interface status
show running-config | include route    # Show route config lines
ping <destination-ip>            # Test end-to-end connectivity
traceroute <destination-ip>      # Show path packets take
```

### Analyzing Packet Flow

#### Example: PC1 (192.168.1.10) sends packet to PC2 (172.16.0.50)

1. **PC1 encapsulation:**
   - Source IP: 192.168.1.10
   - Destination IP: 172.16.0.50
   - PC1 recognizes destination on different network
   - Sends to default gateway (192.168.1.1)

2. **R1 receives packet:**
   - Checks routing table for 172.16.0.50
   - Finds route: 172.16.0.0/16 via 10.1.1.2
   - Forwards packet to R2 via G0/0

3. **R2 receives packet:**
   - Checks routing table for 172.16.0.50
   - Finds directly connected route: 172.16.0.0/16 on G0/1
   - Forwards directly to PC2

4. **Return traffic follows reverse path**

### Troubleshooting Routing Issues

#### Common Problems

1. **Missing Route**
   - Symptom: Destination unreachable
   - Check: `show ip route`
   - Solution: Add missing static route

2. **Incorrect Next-Hop IP**
   - Symptom: Packets forwarded to wrong location
   - Check: Verify next-hop in routing table
   - Solution: Correct static route configuration

3. **Incorrect Subnet Mask**
   - Symptom: Traffic not matching route
   - Check: Verify mask in `show ip route`
   - Solution: Reconfigure with correct mask

4. **Interface Down**
   - Symptom: Routes disappear from table
   - Check: `show ip interface brief`
   - Solution: `no shutdown`, check cables

5. **Mismatched Duplex/Speed**
   - Symptom: Intermittent connectivity, errors
   - Check: `show interfaces`
   - Solution: Configure matching duplex/speed or use auto

#### Systematic Troubleshooting Steps

1. **Verify physical connectivity**
   ```
   show ip interface brief
   show interfaces
   ```

2. **Check routing table**
   ```
   show ip route
   ```

3. **Test connectivity step-by-step**
   ```
   ping <next-hop>
   ping <destination>
   traceroute <destination>
   ```

4. **Verify configuration**
   ```
   show running-config
   ```

5. **Debug (use cautiously)**
   ```
   debug ip routing
   debug ip packet
   ```

### Documentation Best Practices

1. **Network diagrams**: Show topology, IP addresses, connections
2. **IP address spreadsheet**: Track assignments
3. **Configuration backups**: Save all device configs
4. **Change logs**: Document all changes with dates
5. **Troubleshooting notes**: Record problems and solutions

---

## 6. Network Applications and Protocols

### DNS (Domain Name System)

#### Purpose
- Translates human-readable domain names to IP addresses
- Hierarchical distributed database
- Makes Internet user-friendly

#### DNS Hierarchy
```
Root (.)
  |
Top-Level Domain (.com, .org, .net, .edu, .ca)
  |
Second-Level Domain (google.com, cisco.com)
  |
Subdomain (www.google.com, mail.google.com)
```

#### DNS Record Types
- **A Record**: Maps hostname to IPv4 address
- **AAAA Record**: Maps hostname to IPv6 address
- **CNAME**: Canonical name (alias)
- **MX**: Mail exchange server
- **NS**: Name server
- **PTR**: Reverse lookup (IP to name)
- **SOA**: Start of authority

#### DNS Query Process
1. User types "www.cisco.com" in browser
2. Computer checks local DNS cache
3. If not cached, queries configured DNS server (recursive query)
4. DNS server checks its cache
5. If not found, queries root server
6. Root directs to .com TLD server
7. TLD directs to cisco.com authoritative server
8. Authoritative server returns IP address
9. DNS server caches result and returns to client
10. Client caches result and connects to IP address

#### DNS Configuration

**Windows DNS Server Settings:**
```
Control Panel > Network > Adapter Properties > IPv4
Preferred DNS: 8.8.8.8 (Google)
Alternate DNS: 1.1.1.1 (Cloudflare)
```

**Cisco Router as DNS Client:**
```
R1(config)# ip domain-lookup
R1(config)# ip name-server 8.8.8.8
R1(config)# ip name-server 1.1.1.1
```

**Cisco Router as DNS Server:**
```
R1(config)# ip dns server
R1(config)# ip host server1 192.168.1.100
R1(config)# ip host www 192.168.1.200
```

#### DNS Troubleshooting

**Windows Commands:**
```
nslookup www.cisco.com          # Query DNS for domain
nslookup 192.168.1.100          # Reverse DNS lookup
ipconfig /displaydns            # Show DNS cache
ipconfig /flushdns              # Clear DNS cache
```

**Common DNS Issues:**
- Incorrect DNS server configuration
- DNS server unreachable
- Stale DNS cache
- Incorrect DNS records

### DHCP (Dynamic Host Configuration Protocol)

#### Purpose
- Automatically assigns IP addresses and network configuration
- Centralized management of IP addresses
- Prevents IP address conflicts

#### DHCP Process (DORA)

1. **Discover** (Client broadcast)
   - Client: "I need an IP address!" (255.255.255.255)
   - Source: 0.0.0.0, Destination: 255.255.255.255

2. **Offer** (Server unicast or broadcast)
   - Server: "I offer you 192.168.1.100"
   - Includes IP, subnet mask, gateway, DNS, lease time

3. **Request** (Client broadcast)
   - Client: "I accept 192.168.1.100 from Server1"
   - Broadcast so other DHCP servers know

4. **Acknowledge** (Server unicast)
   - Server: "192.168.1.100 is yours for 24 hours"
   - Client configures interface

#### DHCP Lease Process
- **Initial lease**: Full DORA process
- **Renewal (T1 timer - 50% of lease)**: Client tries to renew with same server
- **Rebinding (T2 timer - 87.5% of lease)**: Client broadcasts to any server
- **Lease expiration**: Client must stop using IP

#### DHCP Configuration

**Cisco Router as DHCP Server:**
```
R1(config)# ip dhcp excluded-address 192.168.1.1 192.168.1.10
R1(config)# ip dhcp excluded-address 192.168.1.254

R1(config)# ip dhcp pool LAN-1
R1(dhcp-config)# network 192.168.1.0 255.255.255.0
R1(dhcp-config)# default-router 192.168.1.1
R1(dhcp-config)# dns-server 8.8.8.8 8.8.4.4
R1(dhcp-config)# domain-name example.com
R1(dhcp-config)# lease 7
R1(dhcp-config)# exit
```

**DHCP Relay Agent (for remote DHCP server):**
```
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# ip helper-address 10.1.1.100
```
*Forwards DHCP broadcasts to server at 10.1.1.100*

**Verification Commands:**
```
show ip dhcp binding          # Shows assigned addresses
show ip dhcp pool             # Shows pool statistics
show ip dhcp server statistics
show ip dhcp conflict         # Shows address conflicts
```

#### DHCP Troubleshooting

**Windows Client:**
```
ipconfig /release             # Release current IP
ipconfig /renew               # Request new IP
ipconfig /all                 # Show DHCP server info
```

**Common DHCP Issues:**
- DHCP server unreachable
- Pool exhausted (no available addresses)
- Incorrect pool configuration
- Missing ip helper-address on router
- DHCP snooping blocking requests

### HTTP/HTTPS (Hypertext Transfer Protocol)

#### Purpose
- Application layer protocol for web communication
- Client-server model
- Request-response mechanism

#### HTTP vs HTTPS
| Feature | HTTP | HTTPS |
|---------|------|-------|
| **Port** | 80 | 443 |
| **Security** | Unencrypted | Encrypted (SSL/TLS) |
| **Speed** | Faster | Slightly slower (encryption overhead) |
| **Use case** | Non-sensitive data | Login, banking, e-commerce |

#### HTTP Methods
- **GET**: Request data from server
- **POST**: Submit data to server
- **PUT**: Update existing resource
- **DELETE**: Delete resource
- **HEAD**: Get headers only (no body)

#### HTTP Request Structure
```
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html
```

#### HTTP Response Structure
```
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1234

<html>...</html>
```

#### HTTP Status Codes
- **1xx**: Informational
- **2xx**: Success (200 OK, 201 Created)
- **3xx**: Redirection (301 Moved Permanently, 302 Found)
- **4xx**: Client error (400 Bad Request, 401 Unauthorized, 404 Not Found)
- **5xx**: Server error (500 Internal Server Error, 503 Service Unavailable)

#### HTTPS/TLS Handshake
1. Client sends "Client Hello" (supported encryption methods)
2. Server responds "Server Hello" (chosen encryption)
3. Server sends SSL certificate
4. Client verifies certificate
5. Client and server establish session keys
6. Encrypted communication begins

### Protocol Analysis with Wireshark

#### Wireshark Basics
- **Packet capture tool**: Intercepts and displays network traffic
- **Protocol decoder**: Understands hundreds of protocols
- **Filters**: Focus on specific traffic

#### Common Display Filters
```
http                          # HTTP traffic only
dns                           # DNS queries and responses
dhcp                          # DHCP traffic
ip.addr == 192.168.1.100     # Traffic to/from specific IP
tcp.port == 80                # Traffic on port 80
http.request.method == "GET"  # HTTP GET requests
dns.qry.name contains "cisco" # DNS queries containing "cisco"
```

#### Analyzing DNS in Wireshark
1. Capture traffic
2. Filter: `dns`
3. Identify:
   - Query packet (questions section)
   - Response packet (answers section)
   - Query type (A, AAAA, MX, etc.)
   - Response code (success, error)
   - IP address returned

#### Analyzing DHCP in Wireshark
1. Filter: `dhcp`
2. Identify DORA messages:
   - Discover: DHCP Discover (broadcast)
   - Offer: DHCP Offer
   - Request: DHCP Request (broadcast)
   - Acknowledge: DHCP ACK
3. Note offered IP, subnet, gateway, DNS, lease time

#### Analyzing HTTP in Wireshark
1. Filter: `http`
2. Examine request:
   - Method (GET, POST)
   - URI requested
   - Host header
3. Examine response:
   - Status code
   - Content-Type
   - Response body (Follow TCP Stream)

### Application Layer Security Concerns

#### DNS Security Issues
- **DNS Spoofing/Cache Poisoning**: Attacker provides false DNS records
- **DNS Tunneling**: Exfiltrating data via DNS queries
- **DDoS attacks**: Overwhelming DNS servers

**Mitigations:**
- DNSSEC (DNS Security Extensions)
- Use trusted DNS servers
- Monitor for unusual DNS traffic

#### DHCP Security Issues
- **Rogue DHCP Server**: Attacker provides malicious configuration
- **DHCP Starvation**: Exhausts IP address pool
- **DHCP Spoofing**: Impersonates legitimate server

**Mitigations:**
- DHCP Snooping on switches
- Port security
- Rate limiting

#### HTTP/HTTPS Security Issues
- **Man-in-the-Middle**: Intercepting HTTP traffic
- **Session Hijacking**: Stealing session cookies
- **Cross-Site Scripting (XSS)**: Injecting malicious scripts
- **SQL Injection**: Manipulating database queries

**Mitigations:**
- Use HTTPS everywhere
- Validate SSL certificates
- Input validation and sanitization
- Web application firewalls (WAF)

---

## 7. IPv6 Addressing

### Limitations of IPv4 and Need for IPv6

#### IPv4 Limitations
- **Address exhaustion**: 4.3 billion addresses insufficient
- **NAT complexity**: Breaks end-to-end connectivity
- **Manual configuration**: DHCP helps but adds complexity
- **Limited mobility support**: Difficult for mobile devices

#### Drivers for IPv6 Adoption
- **IoT explosion**: Billions of connected devices
- **Mobile growth**: Every device needs address
- **Cloud computing**: Massive scale requires more addresses
- **Better security**: IPsec mandatory in IPv6
- **Simplified header**: More efficient routing

### IPv6 Address Structure

#### Format
- **128 bits** (vs 32 bits for IPv4)
- Written as **8 groups of 4 hexadecimal digits**
- Separated by colons
- Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

#### Hexadecimal Notation
- Uses digits 0-9 and A-F
- Each hex digit represents 4 bits
- Each group (hextet) represents 16 bits

#### IPv6 Address Representation Rules

**Rule 1: Omit Leading Zeros**
```
2001:0db8:0000:0042:0000:8a2e:0070:7334
Can be written as:
2001:db8:0:42:0:8a2e:70:7334
```

**Rule 2: Double Colon (::) for Consecutive Zeros**
- Can only be used ONCE in an address
- Represents one or more groups of 16 zeros

```
2001:0db8:0000:0000:0000:0000:0000:0001
Can be written as:
2001:db8::1
```

```
2001:0db8:0000:0042:0000:0000:0000:0001
Can be written as:
2001:db8:0:42::1
```

**Invalid: Using :: twice**
```
2001::0042::0001  ❌ WRONG
```

#### Prefix Length Notation
- Similar to CIDR in IPv4
- /64 is standard for networks
- Format: `2001:db8:acad:1::/64`

### IPv6 Address Types

#### Global Unicast Address (GUA)
- **Range**: 2000::/3 (2000:: to 3FFF:...)
- **Purpose**: Public Internet addresses
- **Scope**: Globally routable
- **Similar to**: IPv4 public addresses
- **Structure**:
  ```
  | 48 bits        | 16 bits   | 64 bits      |
  | Global Prefix  | Subnet ID | Interface ID |
  ```

**Example:**
```
2001:db8:acad:1::10/64
- 2001:db8:acad: = Global prefix (assigned by ISP)
- 1 = Subnet ID
- ::10 = Interface ID
```

#### Link-Local Address (LLA)
- **Range**: FE80::/10 (FE80:: to FEBF::)
- **Purpose**: Communication on local link only
- **Scope**: Not routable beyond local network
- **Automatically configured**: On all IPv6-enabled interfaces
- **Required**: For IPv6 operation (neighbor discovery, routing protocols)
- **Format**: FE80::/64 + Interface ID

**Example:**
```
FE80::1
FE80::2:11FF:FE23:4567
```

#### Unique Local Address (ULA)
- **Range**: FC00::/7 (FC00:: to FDFF::)
- **Purpose**: Private addressing
- **Scope**: Not routable on Internet
- **Similar to**: IPv4 private addresses (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16)
- **Common practice**: Use FD00::/8

**Example:**
```
FD00:1234:5678:1::10/64
```

#### Multicast Address
- **Range**: FF00::/8
- **Purpose**: One-to-many communication
- **No broadcast in IPv6**: Replaced by multicast
- **Important multicast addresses**:
  - FF02::1 = All nodes on link
  - FF02::2 = All routers on link
  - FF02::1:FF00:0/104 = Solicited-node multicast

**Example:**
```
FF02::1  (ping all devices on local link)
```

#### Anycast Address
- **Assigned to multiple devices**
- **Packet delivered to nearest device** (lowest metric)
- **Same format as unicast**
- **Use case**: Load balancing, redundancy

#### Special Addresses
- **::/128** = Unspecified address (like 0.0.0.0)
- **::1/128** = Loopback (like 127.0.0.1)
- **::/0** = Default route
- **2001:db8::/32** = Documentation addresses

### IPv6 Address Configuration Methods

#### 1. Manual (Static) Configuration

**Cisco Router:**
```
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# ipv6 address FE80::1 link-local
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# ipv6 unicast-routing
```

**Windows PC:**
```
netsh interface ipv6 add address "Ethernet" 2001:db8:acad:1::10/64
```

#### 2. SLAAC (Stateless Address Autoconfiguration)

**How it works:**
1. Host generates link-local address
2. Host sends Router Solicitation (RS) to FF02::2
3. Router sends Router Advertisement (RA) with prefix
4. Host combines prefix + Interface ID = GUA
5. No server needed!

**Characteristics:**
- Automatic configuration
- No DHCP server required
- Uses Neighbor Discovery Protocol (NDP)
- Gateway address from RA

**Router Configuration:**
```
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# ipv6 unicast-routing
```

#### 3. Stateless DHCPv6

**Characteristics:**
- SLAAC for address
- DHCPv6 for DNS, domain name
- Router provides prefix
- DHCPv6 server provides additional info

**Router Configuration:**
```
R1(config-if)# ipv6 nd other-config-flag
```

**DHCPv6 Server:**
```
R1(config)# ipv6 dhcp pool IPV6-STATELESS
R1(config-dhcpv6)# dns-server 2001:4860:4860::8888
R1(config-dhcpv6)# domain-name example.com
R1(config-dhcpv6)# exit
R1(config)# interface g0/0
R1(config-if)# ipv6 dhcp server IPV6-STATELESS
```

#### 4. Stateful DHCPv6

**Characteristics:**
- DHCPv6 provides everything (address, DNS, gateway)
- Similar to IPv4 DHCP
- Centralized management

**Router Configuration:**
```
R1(config-if)# ipv6 nd managed-config-flag
R1(config-if)# ipv6 nd prefix default no-autoconfig
```

**DHCPv6 Server:**
```
R1(config)# ipv6 dhcp pool IPV6-STATEFUL
R1(config-dhcpv6)# address prefix 2001:db8:acad:1::/64
R1(config-dhcpv6)# dns-server 2001:4860:4860::8888
R1(config-dhcpv6)# domain-name example.com
R1(config-dhcpv6)# exit
R1(config)# interface g0/0
R1(config-if)# ipv6 dhcp server IPV6-STATEFUL
```

#### 5. EUI-64 (Extended Unique Identifier)

**Purpose**: Automatically generate Interface ID from MAC address

**Process:**
1. Take 48-bit MAC address: `00:1A:2B:3C:4D:5E`
2. Insert `FF:FE` in middle: `00:1A:2B:FF:FE:3C:4D:5E`
3. Flip 7th bit (universal/local bit): `02:1A:2B:FF:FE:3C:4D:5E`
4. Result: `021A:2BFF:FE3C:4D5E`

**Configuration:**
```
R1(config-if)# ipv6 address 2001:db8:acad:1::/64 eui-64
```

**Privacy concern**: MAC address visible in IPv6 address
**Solution**: Privacy extensions (randomized Interface IDs)

### Neighbor Discovery Protocol (NDP)

**Purpose**: Replaces ARP, ICMP, IGMP from IPv4

**Functions:**
1. **Router Discovery**: Find routers on link (RS/RA)
2. **Prefix Discovery**: Learn network prefixes
3. **Address Autoconfiguration**: SLAAC process
4. **Address Resolution**: Find MAC from IPv6 (like ARP)
5. **Next-hop Determination**: Find next router
6. **Duplicate Address Detection (DAD)**: Check address uniqueness
7. **Neighbor Unreachability Detection**: Verify neighbors still reachable

**ICMPv6 Messages:**
- **Router Solicitation (RS)**: "Any routers here?"
- **Router Advertisement (RA)**: "I'm a router, here's the prefix"
- **Neighbor Solicitation (NS)**: "Who has this IPv6?"
- **Neighbor Advertisement (NA)**: "I have this IPv6, here's my MAC"
- **Redirect**: "Use this router instead"

### IPv6 Subnetting

#### Standard /64 Subnets

**Given**: 2001:db8:acad::/48 (typical ISP allocation)

**Subnet field**: 16 bits (positions 49-64)
**Possible subnets**: 2^16 = 65,536 subnets

**Examples:**
```
2001:db8:acad:0000::/64  → Subnet 0
2001:db8:acad:0001::/64  → Subnet 1
2001:db8:acad:0002::/64  → Subnet 2
...
2001:db8:acad:FFFF::/64  → Reserved/future use
```

#### Subnetting Beyond /64

**Possible but not recommended for end-user networks**

**Example**: 2001:db8:acad:1::/64 divided into /68 subnets
- Each /68 provides 60 bits for hosts (still plenty!)
- Creates 16 smaller subnets

**When to use:**
- Point-to-point links (/127)
- Loopback interfaces (/128)

### IPv6 Routing

#### Enabling IPv6 Routing
```
Router(config)# ipv6 unicast-routing
```
*Without this command, router won't forward IPv6 packets*

#### Static IPv6 Routes
```
Router(config)# ipv6 route <destination-prefix/length> <next-hop-address | exit-interface>
```

**Examples:**
```
R1(config)# ipv6 route 2001:db8:acad:2::/64 2001:db8:acad:1::2
R1(config)# ipv6 route 2001:db8:acad:3::/64 gigabitEthernet0/1
R1(config)# ipv6 route ::/0 2001:db8:1::1  (default route)
```

#### Verification Commands
```
show ipv6 interface brief         # Interface status and addresses
show ipv6 interface g0/0          # Detailed interface info
show ipv6 route                   # IPv6 routing table
show ipv6 neighbors               # NDP neighbor table (like ARP)
ping 2001:db8:acad:1::10          # Test connectivity
traceroute 2001:db8:acad:2::50    # Trace path
show ipv6 routers                 # Show known routers
```

### Troubleshooting IPv6

#### Common Issues

1. **No IPv6 connectivity**
   - Check: `ipv6 unicast-routing` enabled on router
   - Check: Interface has IPv6 address and is up
   - Verify: `show ipv6 interface brief`

2. **Cannot reach remote networks**
   - Check: IPv6 routing table (`show ipv6 route`)
   - Verify: Static routes or routing protocol configured
   - Test: Ping next-hop router

3. **Link-local only**
   - Symptom: Only FE80:: address present
   - Cause: No RA received or SLAAC not working
   - Solution: Verify router configuration, check RA

4. **Duplicate address detection failure**
   - Symptom: Interface in tentative state
   - Cause: Another device has same address
   - Solution: Change IP or find conflicting device

5. **NDP issues**
   - Check: `show ipv6 neighbors`
   - Look for: REACH status (reachable)
   - Debug: `debug ipv6 nd`

#### Diagnostic Commands
```
ping ipv6 2001:db8:acad:1::1      # Test IPv6 connectivity
ping ff02::1                      # Ping all local devices
traceroute 2001:db8:acad:2::10    # Trace path
show ipv6 interface g0/0          # Detailed interface info
show ipv6 neighbors               # Neighbor cache
debug ipv6 packet                 # Debug IPv6 packets (use carefully!)
```

### IPv4/IPv6 Coexistence Strategies

#### 1. Dual Stack
- **Description**: Run both IPv4 and IPv6 simultaneously
- **Advantages**: Simple, maintains full IPv4 compatibility
- **Disadvantages**: Double configuration, more complexity
- **Use case**: Standard deployment method

**Configuration:**
```
R1(config)# interface g0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# no shutdown
```

#### 2. Tunneling
- **Description**: Encapsulate IPv6 packets inside IPv4
- **Types**:
  - **Manual tunnels**: Static configuration
  - **6to4**: Automatic tunnel using 2002::/16
  - **GRE**: Generic Routing Encapsulation
  - **ISATAP**: Intra-Site Automatic Tunnel Addressing Protocol

**Manual Tunnel Configuration:**
```
R1(config)# interface tunnel 0
R1(config-if)# ipv6 address 2001:db8:1:1::1/64
R1(config-if)# tunnel source 10.1.1.1
R1(config-if)# tunnel destination 10.2.2.2
R1(config-if)# tunnel mode ipv6ip
```

#### 3. Translation (NAT64)
- **Description**: Translate between IPv6 and IPv4
- **Use case**: IPv6-only client accessing IPv4 server
- **Requires**: DNS64 for address synthesis
- **Address format**: 64:FF9B::/96 + IPv4 address

---

## 8. Switching Concepts

### Ethernet Switching

#### MAC Address Table (CAM Table)
- **Purpose**: Maps MAC addresses to switch ports
- **Learning**: Switch learns by examining source MAC of incoming frames
- **Aging**: Entries removed after 5 minutes (default) of inactivity
- **Flooding**: Unknown unicast frames sent out all ports except incoming

**MAC Address Table Process:**
1. **Frame arrives** on port
2. **Learn**: Record source MAC → port mapping
3. **Forward decision**:
   - If destination MAC in table → forward to specific port
   - If destination MAC unknown → flood all ports except incoming
   - If destination MAC = broadcast → flood all ports

**View MAC table:**
```
Switch# show mac address-table
Switch# show mac address-table dynamic
Switch# show mac address-table address 0050.7966.6800
Switch# show mac address-table interface fa0/1
```

**Clear MAC table:**
```
Switch# clear mac address-table dynamic
Switch# clear mac address-table dynamic address 0050.7966.6800
```

#### Frame Switching Methods

**1. Store-and-Forward**
- Receives entire frame
- Performs error checking (CRC)
- Forwards if no errors
- **Advantage**: Error-free transmission
- **Disadvantage**: Higher latency

**2. Cut-Through**
- Forwards as soon as destination MAC read
- No error checking
- **Advantage**: Lowest latency
- **Disadvantage**: Propagates bad frames

**3. Fragment-Free**
- Reads first 64 bytes (collision fragment)
- Compromise between store-and-forward and cut-through

#### Switching Domains

**Collision Domain**
- Network segment where collisions can occur
- Hubs create large collision domains
- **Switches create separate collision domain per port**

**Broadcast Domain**
- Area where broadcasts are propagated
- Routers separate broadcast domains
- **Switches forward broadcasts to all ports in same VLAN**

### VLANs (Virtual Local Area Networks)

#### Purpose of VLANs
- **Segment networks logically**: Without physical separation
- **Improve security**: Isolate sensitive traffic
- **Reduce broadcast traffic**: Smaller broadcast domains
- **Organize by function**: Group users by department, not location
- **Cost savings**: No need for separate switches

#### VLAN Concepts

**Default VLANs:**
- **VLAN 1**: Default VLAN, cannot be deleted
- **VLAN 1002-1005**: Reserved for legacy technologies

**VLAN Types:**
- **Data VLAN**: User traffic
- **Voice VLAN**: VoIP phones
- **Management VLAN**: Switch management traffic
- **Native VLAN**: Untagged traffic on trunk (default VLAN 1)

#### VLAN Configuration

**Create VLANs:**
```
Switch(config)# vlan 10
Switch(config-vlan)# name SALES
Switch(config-vlan)# exit

Switch(config)# vlan 20
Switch(config-vlan)# name ENGINEERING
Switch(config-vlan)# exit

Switch(config)# vlan 99
Switch(config-vlan)# name MANAGEMENT
Switch(config-vlan)# exit
```

**Assign Ports to VLANs (Access Ports):**
```
Switch(config)# interface range fa0/1-10
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 10
Switch(config-if-range)# exit

Switch(config)# interface range fa0/11-20
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 20
Switch(config-if-range)# exit
```

**Verification:**
```
show vlan brief
show vlan id 10
show interfaces fa0/1 switchport
show interfaces trunk
```

#### Trunk Links

**Purpose**: Carry traffic for multiple VLANs between switches

**VLAN Tagging (802.1Q):**
- Adds 4-byte tag to Ethernet frame
- Tag includes VLAN ID (12 bits = 4094 VLANs)
- Native VLAN traffic untagged

**Configure Trunk:**
```
Switch(config)# interface gigabitEthernet 0/1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk native vlan 99
Switch(config-if)# switchport trunk allowed vlan 10,20,99
Switch(config-if)# exit
```

**Verification:**
```
show interfaces trunk
show interfaces g0/1 switchport
```

**Best Practices:**
- Change native VLAN from default (VLAN 1)
- Disable DTP (Dynamic Trunking Protocol)
- Specify allowed VLANs explicitly

```
Switch(config-if)# switchport nonegotiate
```

#### Inter-VLAN Routing

**Problem**: VLANs cannot communicate directly (different broadcast domains)

**Solutions:**

**1. Router-on-a-Stick (ROAS)**
- Single physical connection
- Multiple subinterfaces (one per VLAN)
- Router performs inter-VLAN routing

**Router Configuration:**
```
Router(config)# interface g0/0
Router(config-if)# no shutdown
Router(config-if)# exit

Router(config)# interface g0/0.10
Router(config-subif)# encapsulation dot1q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0
Router(config-subif)# exit

Router(config)# interface g0/0.20
Router(config-subif)# encapsulation dot1q 20
Router(config-subif)# ip address 192.168.20.1 255.255.255.0
Router(config-subif)# exit
```

**Switch Configuration:**
```
Switch(config)# interface g0/1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan 10,20
```

**2. Layer 3 Switch (SVI - Switched Virtual Interfaces)**
- Switch performs routing between VLANs
- Faster than ROAS
- More scalable

**Layer 3 Switch Configuration:**
```
Switch(config)# ip routing

Switch(config)# interface vlan 10
Switch(config-if)# ip address 192.168.10.1 255.255.255.0
Switch(config-if)# no shutdown
Switch(config-if)# exit

Switch(config)# interface vlan 20
Switch(config-if)# ip address 192.168.20.1 255.255.255.0
Switch(config-if)# no shutdown
Switch(config-if)# exit
```

### VTP (VLAN Trunking Protocol)

#### What is VTP?

**VTP (VLAN Trunking Protocol)** is a Cisco proprietary protocol that manages VLAN configuration across multiple switches.

**Purpose:**
- Centralized VLAN management
- Ensures consistency across switches
- Reduces configuration errors
- Easier to scale large networks

#### VTP Modes

**1. VTP Server Mode**
- Can create/modify/delete VLANs
- Propagates changes to other switches
- Stores VLAN config in NVRAM
- Default mode on Cisco switches

**2. VTP Client Mode**
- Cannot create/modify/delete VLANs
- Receives and forwards VTP advertisements
- Does NOT store VLAN config in NVRAM
- Gets configuration from server

**3. VTP Transparent Mode**
- Can create/modify/delete VLANs locally
- Forwards VTP advertisements but doesn't participate
- Stores VLAN config locally
- Changes not propagated to other switches

**4. VTP Off Mode**
- Doesn't forward VTP advertisements
- Completely isolated from VTP domain

#### VTP Configuration

**VTP Server:**
```
Switch(config)# vtp mode server
Switch(config)# vtp domain COMPANY
Switch(config)# vtp password SecurePass123
Switch(config)# vtp version 2
Switch(config)# vtp pruning
```

**VTP Client:**
```
Switch(config)# vtp mode client
Switch(config)# vtp domain COMPANY
Switch(config)# vtp password SecurePass123
```

**VTP Transparent:**
```
Switch(config)# vtp mode transparent
Switch(config)# vtp domain COMPANY
```

**Verification:**
```
show vtp status
show vtp counters
show vtp password
```

#### Important VTP Concepts

**Configuration Revision Number:**
- Tracks VLAN database changes
- Higher revision = more recent config
- **DANGER:** Switch with higher revision overwrites others

**Reset revision number (before adding switch to network):**
```
Switch(config)# vtp domain TEMP
Switch(config)# vtp domain COMPANY
```

**VTP Pruning:**
- Reduces unnecessary broadcast traffic
- Removes unneeded VLANs from trunk links
- Enable on VTP server only

#### Modern Best Practice
Many engineers now use **VTP transparent mode** on all switches:
- Prevents accidental VLAN deletion
- No risk from rogue switches
- More predictable and controllable
- Configure VLANs manually on each switch

### Switch Security

#### Port Security
- **Purpose**: Limit MAC addresses allowed on a port
- **Prevents**: MAC flooding, unauthorized access

**Configuration:**
```
Switch(config)# interface fa0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport port-security
Switch(config-if)# switchport port-security maximum 2
Switch(config-if)# switchport port-security mac-address sticky
Switch(config-if)# switchport port-security violation shutdown
Switch(config-if)# exit
```

**Violation Modes:**
- **Shutdown**: Err-disables port (default), requires manual recovery
- **Restrict**: Drops violating packets, logs, increments counter
- **Protect**: Drops violating packets silently

**Recover from err-disabled:**
```
Switch(config)# interface fa0/1
Switch(config-if)# shutdown
Switch(config-if)# no shutdown
```

**Verification:**
```
show port-security
show port-security interface fa0/1
show port-security address
```

#### DHCP Snooping
- **Purpose**: Prevent rogue DHCP servers
- **Creates**: Binding table (IP, MAC, port, VLAN)

**Configuration:**
```
Switch(config)# ip dhcp snooping
Switch(config)# ip dhcp snooping vlan 10,20
Switch(config)# interface g0/1
Switch(config-if)# ip dhcp snooping trust
Switch(config-if)# exit

Switch(config)# interface range fa0/1-24
Switch(config-if-range)# ip dhcp snooping limit rate 10
```

#### Dynamic ARP Inspection (DAI)
- **Purpose**: Prevent ARP spoofing
- **Uses**: DHCP snooping binding table

**Configuration:**
```
Switch(config)# ip arp inspection vlan 10,20
Switch(config)# interface g0/1
Switch(config-if)# ip arp inspection trust
```

### Spanning Tree Protocol (STP)

#### Purpose
- **Prevents**: Layer 2 loops
- **Creates**: Loop-free logical topology
- **Provides**: Redundancy with loop prevention

#### STP Operation

**Port Roles:**
- **Root Port (RP)**: Best path to root bridge
- **Designated Port (DP)**: Best path to segment
- **Alternate Port**: Backup to root port (blocked)
- **Backup Port**: Backup to designated port (blocked)

**Port States:**
1. **Blocking**: Receives BPDUs, drops data (20 sec)
2. **Listening**: Processes BPDUs (15 sec)
3. **Learning**: Learns MAC addresses (15 sec)
4. **Forwarding**: Forwards data
5. **Disabled**: Administratively down

**STP Convergence Time: ~50 seconds** (20 + 15 + 15)

#### Root Bridge Election
1. **Lowest Bridge ID wins**
2. Bridge ID = Priority (default 32768) + MAC address
3. All other switches find best path to root

**Configure Root Bridge:**
```
Switch(config)# spanning-tree vlan 1 root primary
```
*Sets priority to 24576*

Or manually:
```
Switch(config)# spanning-tree vlan 1 priority 4096
```
*Priority must be multiple of 4096*

#### PortFast and BPDU Guard

**PortFast**: Skips listening/learning states for access ports
```
Switch(config)# interface fa0/1
Switch(config-if)# spanning-tree portfast
```

**BPDU Guard**: Shuts down port if BPDU received (prevents loops)
```
Switch(config-if)# spanning-tree bpduguard enable
```

**Global configuration:**
```
Switch(config)# spanning-tree portfast default
Switch(config)# spanning-tree portfast bpduguard default
```

#### Rapid PVST+ (RPVST+)
- **Faster convergence**: Seconds instead of 50 seconds
- **Per-VLAN**: Separate instance for each VLAN
- **Cisco default**: On modern switches

```
Switch(config)# spanning-tree mode rapid-pvst
```

**Verification:**
```
show spanning-tree
show spanning-tree summary
show spanning-tree vlan 10
```

### EtherChannel

#### Purpose
- **Combines multiple physical links** into one logical link
- **Increases bandwidth**: Up to 8 links
- **Provides redundancy**: If one link fails, others continue

#### Protocols
- **PAgP (Port Aggregation Protocol)**: Cisco proprietary
- **LACP (Link Aggregation Control Protocol)**: IEEE 802.3ad, industry standard

#### Configuration

**LACP (Recommended):**
```
Switch(config)# interface range g0/1-2
Switch(config-if-range)# channel-group 1 mode active
Switch(config-if-range)# exit

Switch(config)# interface port-channel 1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan 10,20,99
```

**PAgP:**
```
Switch(config)# interface range g0/1-2
Switch(config-if-range)# channel-group 1 mode desirable
```

**Modes:**
- **LACP**:
  - `active`: Actively negotiates (recommended)
  - `passive`: Waits for negotiation
- **PAgP**:
  - `desirable`: Actively negotiates
  - `auto`: Waits for negotiation

**Verification:**
```
show etherchannel summary
show etherchannel port-channel
show interfaces port-channel 1
```

### EtherChannel

#### Purpose
- **Combines multiple physical links** into one logical link
- **Increases bandwidth**: Up to 8 links
- **Provides redundancy**: If one link fails, others continue

#### Protocols
- **PAgP (Port Aggregation Protocol)**: Cisco proprietary
- **LACP (Link Aggregation Control Protocol)**: IEEE 802.3ad, industry standard

#### Configuration

**LACP (Recommended):**
```
Switch(config)# interface range g0/1-2
Switch(config-if-range)# channel-group 1 mode active
Switch(config-if-range)# exit

Switch(config)# interface port-channel 1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan 10,20,99
```

**PAgP:**
```
Switch(config)# interface range g0/1-2
Switch(config-if-range)# channel-group 1 mode desirable
```

**Modes:**
- **LACP**:
  - `active`: Actively negotiates (recommended)
  - `passive`: Waits for negotiation
- **PAgP**:
  - `desirable`: Actively negotiates
  - `auto`: Waits for negotiation

**Verification:**
```
show etherchannel summary
show etherchannel port-channel
show interfaces port-channel 1
```

### HSRP, VRRP, and GLBP (First Hop Redundancy Protocols)

#### Purpose
Provide **default gateway redundancy** - if one router fails, another takes over seamlessly.

#### HSRP (Hot Standby Router Protocol)

**Cisco proprietary**

**How it works:**
- Multiple routers share a **virtual IP address**
- One router is **active**, others are **standby**
- Hosts use virtual IP as default gateway
- If active fails, standby becomes active (3-second switchover)

**Configuration:**
```
Router1(config)# interface g0/0
Router1(config-if)# ip address 192.168.1.2 255.255.255.0
Router1(config-if)# standby 1 ip 192.168.1.1
Router1(config-if)# standby 1 priority 110
Router1(config-if)# standby 1 preempt

Router2(config)# interface g0/0
Router2(config-if)# ip address 192.168.1.3 255.255.255.0
Router2(config-if)# standby 1 ip 192.168.1.1
Router2(config-if)# standby 1 priority 100
```

**Key concepts:**
- **Virtual IP**: 192.168.1.1 (shared)
- **Priority**: Higher priority = active router (default 100)
- **Preempt**: Higher priority router takes over when it comes back online
- **Group number**: Matches routers in same HSRP group

**Verification:**
```
show standby
show standby brief
```

#### VRRP (Virtual Router Redundancy Protocol)

**Industry standard** (RFC 5798)

**Similar to HSRP but:**
- Open standard (works with any vendor)
- Master/backup terminology (instead of active/standby)
- Virtual MAC uses format: 0000.5E00.01XX

**Configuration:**
```
Router1(config)# interface g0/0
Router1(config-if)# ip address 192.168.1.2 255.255.255.0
Router1(config-if)# vrrp 1 ip 192.168.1.1
Router1(config-if)# vrrp 1 priority 110
Router1(config-if)# vrrp 1 preempt
```

#### GLBP (Gateway Load Balancing Protocol)

**Cisco proprietary**

**Advantage over HSRP/VRRP:**
- **Load balancing** - all routers forward traffic simultaneously
- More efficient use of bandwidth
- One virtual IP, multiple virtual MACs

**Configuration:**
```
Router1(config)# interface g0/0
Router1(config-if)# ip address 192.168.1.2 255.255.255.0
Router1(config-if)# glbp 1 ip 192.168.1.1
Router1(config-if)# glbp 1 priority 110
Router1(config-if)# glbp 1 preempt
Router1(config-if)# glbp 1 load-balancing round-robin
```

**Load balancing methods:**
- Round-robin (default)
- Weighted
- Host-dependent

**Comparison:**

| Feature | HSRP | VRRP | GLBP |
|---------|------|------|------|
| **Vendor** | Cisco | Open standard | Cisco |
| **Load balancing** | No | No | Yes |
| **Active routers** | 1 | 1 | Multiple |
| **Preempt default** | Disabled | Enabled | Disabled |
| **Failover time** | ~3 seconds | ~3 seconds | ~3 seconds |

---

## 9. Wireless Networking

### Wireless LAN Components

#### Wireless Access Point (AP)
- Provides wireless connectivity
- Connects wireless clients to wired network
- Operates at Layer 2

**AP Modes:**
- **Autonomous AP**: Standalone, self-contained
- **Lightweight AP**: Managed by WLC (Wireless LAN Controller)
- **Home/SOHO AP**: Combined router/AP/switch

#### Wireless LAN Controller (WLC)
- Centrally manages multiple APs
- Scales to thousands of APs
- Provides roaming, security policies, RF management

#### Wireless Clients
- Devices with wireless NICs
- Laptops, smartphones, tablets, IoT devices

### Wireless Standards (802.11)

| Standard | Year | Frequency | Max Speed | Range |
|----------|------|-----------|-----------|-------|
| 802.11 | 1997 | 2.4 GHz | 2 Mbps | Short |
| 802.11b | 1999 | 2.4 GHz | 11 Mbps | Medium |
| 802.11a | 1999 | 5 GHz | 54 Mbps | Short |
| 802.11g | 2003 | 2.4 GHz | 54 Mbps | Medium |
| 802.11n (Wi-Fi 4) | 2009 | 2.4/5 GHz | 600 Mbps | Long |
| 802.11ac (Wi-Fi 5) | 2013 | 5 GHz | 6.9 Gbps | Long |
| 802.11ax (Wi-Fi 6) | 2019 | 2.4/5 GHz | 9.6 Gbps | Long |
| 802.11ax (Wi-Fi 6E) | 2020 | 6 GHz | 9.6 Gbps | Long |

### Wireless Frequency Bands

#### 2.4 GHz Band
- **Channels**: 1-11 (North America), 1-13 (Europe)
- **Non-overlapping channels**: 1, 6, 11
- **Advantages**: Better range, penetrates walls
- **Disadvantages**: Crowded, interference (Bluetooth, microwaves)

#### 5 GHz Band
- **More channels**: 24+ non-overlapping channels
- **Advantages**: Less interference, higher speeds
- **Disadvantages**: Shorter range, less wall penetration

#### 6 GHz Band (Wi-Fi 6E)
- **Latest addition**: Even more channels
- **Advantages**: No legacy devices, very clean spectrum
- **Disadvantages**: Requires new hardware

### Wireless Topologies

#### Ad Hoc (IBSS - Independent Basic Service Set)
- Peer-to-peer network
- No AP required
- Limited range and functionality

#### Infrastructure Mode (BSS - Basic Service Set)
- Clients connect to AP
- AP connects to wired network
- Most common topology

#### Extended Service Set (ESS)
- Multiple APs with same SSID
- Seamless roaming
- Enterprise deployments

### Wireless Security

#### Open Network
- No security
- Anyone can connect
- **Never use** except for public hotspots

#### WEP (Wired Equivalent Privacy)
- **Obsolete**: Easily cracked
- 64-bit or 128-bit keys
- **Never use**

#### WPA (Wi-Fi Protected Access)
- Replacement for WEP
- TKIP encryption
- Better but still vulnerable

#### WPA2 (802.11i)
- **Current standard**
- AES encryption (CCMP)
- Two modes:
  - **WPA2-Personal (PSK)**: Pre-shared key, home use
  - **WPA2-Enterprise**: 802.1X authentication, RADIUS server

#### WPA3
- **Latest standard** (2018)
- Stronger encryption (192-bit for Enterprise)
- Protection against offline dictionary attacks
- Forward secrecy
- Simplified device setup (Wi-Fi Easy Connect)

**Modes:**
- **WPA3-Personal**: SAE (Simultaneous Authentication of Equals)
- **WPA3-Enterprise**: 802.1X with 192-bit security

#### Authentication Methods

**Pre-Shared Key (PSK)**
- Password known by all users
- Same key for everyone
- Suitable for home/small office

**802.1X / EAP (Enterprise)**
- Individual user credentials
- RADIUS server authentication
- Certificate-based or username/password
- Accounting and logging

### Wireless Configuration

#### Basic AP Configuration (Cisco)
```
AP# configure terminal
AP(config)# hostname AP1
AP1(config)# interface gigabitEthernet 0
AP1(config-if)# ip address 192.168.1.2 255.255.255.0
AP1(config-if)# no shutdown
AP1(config-if)# exit

AP1(config)# dot11 ssid COMPANY-WIFI
AP1(config-ssid)# authentication open
AP1(config-ssid)# authentication key-management wpa version 2
AP1(config-ssid)# wpa-psk ascii MySecurePassword123
AP1(config-ssid)# exit

AP1(config)# interface dot11Radio 0
AP1(config-if)# ssid COMPANY-WIFI
AP1(config-if)# channel 6
AP1(config-if)# no shutdown
```

#### Router with Built-in Wireless (Home Router)
*Usually configured via web interface*
1. Connect to router (192.168.1.1 or 192.168.0.1)
2. Login (admin/admin or admin/password)
3. Navigate to Wireless Settings
4. Configure:
   - SSID name
   - Security mode (WPA2/WPA3)
   - Password
   - Channel (Auto or manual 1, 6, 11)

### Wireless Troubleshooting

#### Common Issues

**1. Cannot connect to wireless network**
- Check: SSID visible?
- Verify: Correct password
- Check: MAC filtering enabled?
- Solution: Verify security settings match

**2. Weak signal**
- Check: Distance from AP
- Check: Obstacles (walls, metal)
- Solution: Move closer, add APs, use repeaters

**3. Slow speeds**
- Check: Channel congestion (use Wi-Fi analyzer)
- Check: Too many clients on AP
- Solution: Change channel, add APs, upgrade to 5 GHz

**4. Intermittent connectivity**
- Check: Interference (microwaves, Bluetooth)
- Check: Roaming between APs
- Solution: Adjust channels, optimize AP placement

**5. Cannot get IP address**
- Check: DHCP server enabled on router
- Solution: Release/renew IP, restart router

#### Diagnostic Tools

**Windows Commands:**
```
netsh wlan show interfaces       # Show wireless info
netsh wlan show networks         # Show available networks
netsh wlan show profiles         # Show saved networks
ipconfig /all                    # Show IP configuration
```

**Site Survey Tools:**
- Ekahau HeatMapper
- NetSpot
- Wi-Fi Analyzer (Android)
- WiFi Explorer (Mac)

---

## 10. Dynamic Routing Protocols

### Routing Protocol Basics

#### Purpose
- Automatically learn routes
- Adapt to topology changes
- Share routing information with neighbors

#### Classification

**By Operation:**
- **Distance Vector**: Uses hop count or metric (RIP, EIGRP)
- **Link State**: Builds complete network map (OSPF, IS-IS)
- **Path Vector**: Uses path attributes (BGP)

**By Location:**
- **IGP (Interior Gateway Protocol)**: Within autonomous system (RIP, EIGRP, OSPF)
- **EGP (Exterior Gateway Protocol)**: Between autonomous systems (BGP)

**By Protocol:**
- **Classful**: No subnet mask in updates (RIPv1)
- **Classless**: Includes subnet mask (RIPv2, EIGRP, OSPF)

### RIP (Routing Information Protocol)

#### Characteristics
- **Distance vector protocol**
- **Metric**: Hop count (max 15 hops)
- **Updates**: Broadcast every 30 seconds
- **Administrative Distance**: 120
- **Versions**:
  - RIPv1: Classful, broadcast
  - RIPv2: Classless, multicast (224.0.0.9)

#### RIPv2 Configuration
```
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.1.0
Router(config-router)# network 10.0.0.0
Router(config-router)# no auto-summary
Router(config-router)# passive-interface gigabitEthernet 0/0
```

**Verification:**
```
show ip protocols
show ip rip database
show ip route rip
debug ip rip
```

**Advantages:**
- Simple configuration
- Works in small networks

**Disadvantages:**
- Slow convergence (3 minutes)
- 15-hop limit
- Inefficient (periodic updates)

### EIGRP (Enhanced Interior Gateway Routing Protocol)

#### Characteristics
- **Advanced distance vector** (or hybrid)
- **Cisco proprietary** (but has open standard version)
- **Metric**: Composite (bandwidth, delay, load, reliability, MTU)
- **Updates**: Partial, triggered (not periodic)
- **Protocol number**: 88
- **Multicast**: 224.0.0.10
- **Administrative Distance**: 90 (internal), 170 (external)

#### EIGRP Features
- **DUAL Algorithm**: Guarantees loop-free paths
- **Unequal cost load balancing**
- **Fast convergence**: Sub-second
- **Classless routing**: Supports VLSM and CIDR
- **Neighbor relationships**: Hello packets every 5 seconds

#### EIGRP Configuration
```
Router(config)# router eigrp 100
Router(config-router)# network 192.168.1.0 0.0.0.255
Router(config-router)# network 10.1.1.0 0.0.0.3
Router(config-router)# passive-interface gigabitEthernet 0/2
Router(config-router)# eigrp router-id 1.1.1.1
Router(config-router)# no auto-summary
```

**Wildcard mask**: Inverse of subnet mask
- Subnet mask 255.255.255.0 → Wildcard 0.0.0.255
- Subnet mask 255.255.255.252 → Wildcard 0.0.0.3

**Verification:**
```
show ip eigrp neighbors
show ip eigrp topology
show ip eigrp interfaces
show ip protocols
show ip route eigrp
```

#### EIGRP Terminology
- **Successor**: Best route to destination
- **Feasible Distance (FD)**: Metric of best path
- **Reported Distance (RD)**: Neighbor's metric to destination
- **Feasible Successor**: Backup route (RD < FD)

### OSPF (Open Shortest Path First)

#### Characteristics
- **Link-state protocol**
- **Open standard**: RFC 2328 (OSPFv2), RFC 5340 (OSPFv3)
- **Metric**: Cost (based on bandwidth)
- **Algorithm**: Dijkstra's SPF
- **Updates**: Triggered, not periodic
- **Protocol number**: 89
- **Multicast**: 224.0.0.5 (AllSPFRouters), 224.0.0.6 (AllDRRouters)
- **Administrative Distance**: 110

#### OSPF Operation
1. **Discover neighbors**: Hello packets every 10 seconds
2. **Exchange link-state database**: Flooding LSAs
3. **Calculate best paths**: SPF algorithm
4. **Update routing table**: Install best routes

#### OSPF Areas
- **Area 0 (Backbone)**: Must exist, all areas connect to it
- **Regular areas**: Connect to Area 0
- **Stub areas**: Don't receive external routes
- **Totally stubby areas**: Only default route
- **NSSA**: Allows limited external routes

#### OSPF Configuration (Single Area)
```
Router(config)# router ospf 1
Router(config-router)# router-id 1.1.1.1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 10.1.1.0 0.0.0.3 area 0
Router(config-router)# passive-interface gigabitEthernet 0/2
```

**Verification:**
```
show ip ospf neighbor
show ip ospf interface
show ip ospf database
show ip protocols
show ip route ospf
```

#### OSPF Router Types
- **Internal Router**: All interfaces in same area
- **Backbone Router**: At least one interface in Area 0
- **ABR (Area Border Router)**: Connects multiple areas
- **ASBR (Autonomous System Boundary Router)**: Connects to external networks

#### OSPF Network Types
- **Broadcast**: Ethernet (DR/BDR election)
- **Point-to-point**: Serial links (no DR/BDR)
- **Non-broadcast**: Frame Relay (manual neighbor config)

#### DR/BDR Election
- **DR (Designated Router)**: Reduces LSA flooding on multi-access networks
- **BDR (Backup Designated Router)**: Backup for DR
- **Election criteria**:
  1. Highest priority (default 1, range 0-255)
  2. Highest router ID
- **Priority 0**: Never becomes DR/BDR

```
Router(config-if)# ip ospf priority 100
```

### Protocol Comparison

| Feature | RIP | EIGRP | OSPF |
|---------|-----|-------|------|
| **Type** | Distance Vector | Advanced DV | Link State |
| **Standard** | Open | Cisco (open version exists) | Open |
| **Metric** | Hop count | Composite | Cost (bandwidth) |
| **Max Metric** | 15 hops | 4.2 billion | 65,535 |
| **Convergence** | Slow (minutes) | Fast (seconds) | Fast (seconds) |
| **Updates** | Periodic (30s) | Triggered | Triggered |
| **Scalability** | Small | Medium-Large | Large |
| **CPU/Memory** | Low | Medium | High |
| **Configuration** | Simple | Moderate | Complex |

### Route Redistribution

**Purpose**: Share routes between different routing protocols

**Example**: Redistribute EIGRP into OSPF
```
Router(config)# router ospf 1
Router(config-router)# redistribute eigrp 100 subnets
Router(config-router)# exit

Router(config)# router eigrp 100
Router(config-router)# redistribute ospf 1 metric 1544 20000 255 1 1500
```

**Caution**: Redistribution can cause routing loops and suboptimal routing

---

## 11. WAN Technologies

### WAN Overview

#### Purpose
- Connect geographically dispersed networks
- Span large distances (cities, countries, continents)
- Typically lower speeds than LANs

#### WAN Terminology
- **DTE (Data Terminal Equipment)**: Customer device (router)
- **DCE (Data Circuit-terminating Equipment)**: Service provider device (modem)
- **CPE (Customer Premises Equipment)**: Devices at customer location
- **Demarcation point**: Where customer responsibility ends
- **Local loop**: Connection from customer to service provider

### WAN Connection Types

#### Dedicated (Leased Lines)
- **Point-to-point permanent connection**
- **Guaranteed bandwidth**
- **Examples**: T1 (1.544 Mbps), T3 (44.736 Mbps), E1 (2.048 Mbps)

**Advantages:**
- Predictable performance
- High security
- No shared bandwidth

**Disadvantages:**
- Expensive
- Fixed bandwidth
- Long installation time

#### Circuit-Switched
- **Dial-up connection** when needed
- **Examples**: PSTN (telephone network), ISDN

**Advantages:**
- Pay per use
- Flexible

**Disadvantages:**
- Slow speeds
- Setup delay
- Largely obsolete

#### Packet-Switched
- **Shared infrastructure**
- **Examples**: Frame Relay (legacy), Metro Ethernet

**Advantages:**
- Cost-effective
- Flexible bandwidth

**Disadvantages:**
- Variable performance
- Shared medium

#### Internet-Based
- **Uses public Internet**
- **Examples**: VPN, broadband

**Types:**
- DSL (Digital Subscriber Line)
- Cable
- Fiber
- Wireless (4G/5G, satellite)

### PPP (Point-to-Point Protocol)

#### Characteristics
- **Layer 2 protocol** for point-to-point links
- **Successor to HDLC**
- **Supports**: Authentication, compression, multilink
- **Authentication methods**: PAP, CHAP

#### PPP Configuration

**Basic PPP:**
```
Router(config)# interface serial 0/0/0
Router(config-if)# encapsulation ppp
Router(config-if)# ip address 10.1.1.1 255.255.255.252
Router(config-if)# no shutdown
```

**PPP with CHAP Authentication:**
```
Router(config)# username RemoteRouter password cisco123

Router(config)# interface serial 0/0/0
Router(config-if)# encapsulation ppp
Router(config-if)# ppp authentication chap
Router(config-if)# ip address 10.1.1.1 255.255.255.252
Router(config-if)# no shutdown
```

**Verification:**
```
show interfaces serial 0/0/0
show ppp all
debug ppp authentication
```

### VPN (Virtual Private Network)

#### Purpose
- **Secure connection over public network**
- **Encrypts traffic**
- **Cost-effective alternative to dedicated WAN**

#### VPN Types

**Site-to-Site VPN**
- Connects entire networks
- Always-on connection
- Transparent to users

**Remote Access VPN**
- Connects individual users
- On-demand connection
- Client software required

#### IPsec (Internet Protocol Security)

**Components:**
- **AH (Authentication Header)**: Authentication and integrity
- **ESP (Encapsulating Security Payload)**: Encryption, authentication, integrity
- **IKE (Internet Key Exchange)**: Key negotiation

**Modes:**
- **Transport mode**: Encrypts payload only (host-to-host)
- **Tunnel mode**: Encrypts entire packet (site-to-site)

**Basic Site-to-Site VPN Configuration:**
```
Router(config)# crypto isakmp policy 10
Router(config-isakmp)# encryption aes 256
Router(config-isakmp)# hash sha
Router(config-isakmp)# authentication pre-share
Router(config-isakmp)# group 2
Router(config-isakmp)# exit

Router(config)# crypto isakmp key MySecretKey address 203.0.113.2

Router(config)# crypto ipsec transform-set MYSET esp-aes 256 esp-sha-hmac

Router(config)# access-list 100 permit ip 192.168.1.0 0.0.0.255 192.168.2.0 0.0.0.255

Router(config)# crypto map MYMAP 10 ipsec-isakmp
Router(config-crypto-map)# set peer 203.0.113.2
Router(config-crypto-map)# set transform-set MYSET
Router(config-crypto-map)# match address 100
Router(config-crypto-map)# exit

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# crypto map MYMAP
```

### GRE (Generic Routing Encapsulation)

#### Purpose
- **Tunneling protocol**
- **Encapsulates wide variety of protocols**
- **Not encrypted by default** (use with IPsec for security)

#### Use Cases
- Connect non-contiguous networks
- Pass routing protocols over Internet
- Multicast traffic over Internet

**GRE Tunnel Configuration:**
```
Router(config)# interface tunnel 0
Router(config-if)# ip address 172.16.1.1 255.255.255.252
Router(config-if)# tunnel source gigabitEthernet 0/0
Router(config-if)# tunnel destination 203.0.113.2
Router(config-if)# tunnel mode gre ip
Router(config-if)# exit
```

---

## 12. Network Management

### Network Documentation

#### Essential Documents
- **Network topology diagrams**: Physical and logical
- **IP addressing scheme**: Spreadsheet or IPAM tool
- **Device inventory**: Make, model, serial numbers
- **Configuration files**: Backups of all devices
- **Change logs**: Who, what, when, why
- **Maintenance schedules**: Firmware updates, backups
- **Troubleshooting procedures**: Common issues and solutions
- **Contact information**: Vendors, ISPs, support

### SNMP (Simple Network Management Protocol)

#### Purpose
- **Monitor and manage network devices**
- **Collect statistics** (bandwidth, errors, uptime)
- **Receive alerts** (link down, high CPU)

#### SNMP Components
- **Manager**: Monitoring system (NMS - Network Management System)
- **Agent**: Software on network device
- **MIB (Management Information Base)**: Database of variables
- **OID (Object Identifier)**: Unique identifier for MIB variable

#### SNMP Versions
- **SNMPv1**: Original, insecure (community strings in clear text)
- **SNMPv2c**: Improved performance, still uses community strings
- **SNMPv3**: Secure (authentication and encryption)

#### SNMP Operations
- **GET**: Manager requests information
- **SET**: Manager modifies configuration
- **TRAP**: Agent sends unsolicited alert
- **INFORM**: Like trap, but requires acknowledgment

**SNMP Configuration:**
```
Router(config)# snmp-server community public RO
Router(config)# snmp-server community private RW
Router(config)# snmp-server location "Building A, Floor 3"
Router(config)# snmp-server contact "admin@example.com"
Router(config)# snmp-server host 192.168.1.100 version 2c public
Router(config)# snmp-server enable traps
```

### Syslog

#### Purpose
- **Centralized logging**
- **Records system events**
- **Troubleshooting and auditing**

#### Syslog Severity Levels
| Level | Name | Description |
|-------|------|-------------|
| 0 | Emergency | System unusable |
| 1 | Alert | Immediate action needed |
| 2 | Critical | Critical condition |
| 3 | Error | Error condition |
| 4 | Warning | Warning condition |
| 5 | Notification | Normal but significant |
| 6 | Informational | Informational message |
| 7 | Debugging | Debug messages |

**Syslog Configuration:**
```
Router(config)# logging 192.168.1.100
Router(config)# logging trap informational
Router(config)# logging source-interface gigabitEthernet 0/0
```

**View local logs:**
```
show logging
```

### NTP (Network Time Protocol)

#### Purpose
- **Synchronize clocks** across network
- **Critical for**: Logging, authentication, scheduled tasks

**NTP Configuration:**
```
Router(config)# ntp server 129.6.15.28
Router(config)# ntp server time.nist.gov
```

**Verification:**
```
show ntp status
show ntp associations
show clock
```

### CDP and LLDP (Discovery Protocols)

#### CDP (Cisco Discovery Protocol)
- **Cisco proprietary**
- **Layer 2 protocol**
- **Discovers directly connected Cisco devices**

**Commands:**
```
show cdp neighbors
show cdp neighbors detail
show cdp interface
cdp run (enable globally)
cdp enable (enable on interface)
```

**Disable for security:**
```
Router(config)# no cdp run
Router(config-if)# no cdp enable
```

#### LLDP (Link Layer Discovery Protocol)
- **Industry standard** (IEEE 802.1AB)
- **Similar to CDP** but vendor-neutral

**Commands:**
```
Router(config)# lldp run
show lldp neighbors
show lldp neighbors detail
```

### Device Management Best Practices

#### Access Security
```
Router(config)# enable secret Str0ngP@ssw0rd
Router(config)# service password-encryption
Router(config)# security passwords min-length 10

Router(config)# line console 0
Router(config-line)# password ConsolePass123
Router(config-line)# login
Router(config-line)# exec-timeout 5 0
Router(config-line)# logging synchronous
Router(config-line)# exit

Router(config)# line vty 0 4
Router(config-line)# password VtyPass123
Router(config-line)# login local
Router(config-line)# transport input ssh
Router(config-line)# exec-timeout 10 0
Router(config-line)# exit

Router(config)# username admin privilege 15 secret AdminPass123
```

#### SSH Configuration
```
Router(config)# hostname R1
R1(config)# ip domain-name example.com
R1(config)# crypto key generate rsa modulus 2048
R1(config)# ip ssh version 2
R1(config)# line vty 0 4
R1(config-line)# transport input ssh
R1(config-line)# login local
```

#### Banner Messages
```
Router(config)# banner motd #
******************************************
*  UNAUTHORIZED ACCESS PROHIBITED       *
*  All access is logged and monitored   *
******************************************
#
```

#### Configuration Management

**Save Configuration:**
```
Router# copy running-config startup-config
Router# write memory
Router# wr
```

**Backup to TFTP:**
```
Router# copy running-config tftp:
Address: 192.168.1.100
Filename: R1-config-backup-2025-01-15
```

**Restore from TFTP:**
```
Router# copy tftp: running-config
Address: 192.168.1.100
Filename: R1-config-backup-2025-01-15
```

**Erase Configuration:**
```
Router# write erase
Router# erase startup-config
Router# reload
```

---

## 13. Network Security Fundamentals

### Security Threats

#### Types of Attacks
- **Reconnaissance**: Information gathering (port scans, ping sweeps)
- **Access attacks**: Unauthorized access (password attacks, phishing)
- **Denial of Service (DoS)**: Overwhelm resources
- **Data exfiltration**: Stealing sensitive information
- **Man-in-the-Middle**: Intercepting communications
- **Malware**: Viruses, worms, trojans, ransomware

### Defense in Depth

**Layered security approach:**
1. **Physical security**: Lock server rooms, badge access
2. **Perimeter security**: Firewalls, IPS
3. **Network security**: ACLs, VLANs, port security
4. **Endpoint security**: Antivirus, host firewalls
5. **Application security**: Input validation, updates
6. **Data security**: Encryption, backups
7. **User security**: Training, strong passwords, MFA

### Access Control Lists (ACLs)

#### Purpose
- **Packet filtering** based on criteria
- **Control traffic flow**
- **Improve security**

#### ACL Types

**Standard ACL**
- **Filters by source IP only**
- **Number range**: 1-99, 1300-1999
- **Place close to destination**

**Extended ACL**
- **Filters by source/dest IP, protocol, port**
- **Number range**: 100-199, 2000-2699
- **Place close to source**

**Named ACL**
- **Descriptive name instead of number**
- **Easier to manage**

#### Standard ACL Configuration

**Deny specific host:**
```
Router(config)# access-list 10 deny host 192.168.1.50
Router(config)# access-list 10 permit any

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip access-group 10 out
```

**Permit specific network:**
```
Router(config)# access-list 20 permit 192.168.10.0 0.0.0.255
Router(config)# access-list 20 deny any

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip access-group 20 in
```

#### Extended ACL Configuration

**Block telnet from specific network:**
```
Router(config)# access-list 100 deny tcp 192.168.1.0 0.0.0.255 any eq 23
Router(config)# access-list 100 permit ip any any

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip access-group 100 in
```

**Allow only HTTP/HTTPS to web server:**
```
Router(config)# access-list 110 permit tcp any host 192.168.1.100 eq 80
Router(config)# access-list 110 permit tcp any host 192.168.1.100 eq 443
Router(config)# access-list 110 deny ip any host 192.168.1.100
Router(config)# access-list 110 permit ip any any

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip access-group 110 in
```

#### Named ACL Configuration

```
Router(config)# ip access-list extended BLOCK-TELNET
Router(config-ext-nacl)# deny tcp any any eq 23
Router(config-ext-nacl)# permit ip any any
Router(config-ext-nacl)# exit

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip access-group BLOCK-TELNET in
```

**Advantages of named ACLs:**
- Delete specific entries
- Insert entries at specific positions
- More readable

**Edit named ACL:**
```
Router(config)# ip access-list extended BLOCK-TELNET
Router(config-ext-nacl)# no 10
Router(config-ext-nacl)# 10 deny tcp 192.168.1.0 0.0.0.255 any eq 23
```

#### ACL Best Practices
- **Implicit deny**: Invisible "deny any" at end
- **Order matters**: First match wins
- **One ACL per interface/direction/protocol**
- **Minimize processing**: Place most common rules first
- **Test carefully**: Can block legitimate traffic
- **Document**: Comment each rule's purpose

**Verification:**
```
show access-lists
show access-lists 10
show ip interface gigabitEthernet 0/0
show running-config | include access-list
```

### NAT (Network Address Translation)

#### Purpose
- **Conserve IPv4 addresses**
- **Hide internal addressing**
- **Provide security layer**

#### NAT Types

**Static NAT**
- **One-to-one mapping**
- **Permanent**
- **Use for servers**

```
Router(config)# ip nat inside source static 192.168.1.100 209.165.200.225

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip nat inside
Router(config-if)# exit

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip nat outside
```

**Dynamic NAT**
- **Pool of public addresses**
- **Temporary mappings**

```
Router(config)# ip nat pool PUBLIC-POOL 209.165.200.225 209.165.200.254 netmask 255.255.255.224
Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
Router(config)# ip nat inside source list 1 pool PUBLIC-POOL

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip nat inside
Router(config-if)# exit

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip nat outside
```

**PAT (Port Address Translation) / NAT Overload**
- **Many private IPs to one public IP**
- **Uses port numbers**
- **Most common in home/small office**

```
Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
Router(config)# ip nat inside source list 1 interface gigabitEthernet 0/1 overload

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip nat inside
Router(config-if)# exit

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip nat outside
```

**Verification:**
```
show ip nat translations
show ip nat statistics
clear ip nat translation *
debug ip nat
```

### Firewalls

#### Types

**Packet-Filtering Firewall**
- Examines packet headers
- Similar to ACLs
- Stateless (each packet independently)

**Stateful Firewall**
- Tracks connection state
- Allows return traffic automatically
- More intelligent

**Application-Layer Firewall**
- Inspects application data
- Can block specific content
- Deep packet inspection (DPI)

**Next-Generation Firewall (NGFW)**
- Application awareness
- Intrusion prevention
- Advanced threat protection
- User identity awareness

#### Zone-Based Firewall (Cisco)

**Concept**: Group interfaces into zones, define policies between zones

```
Router(config)# zone security INSIDE
Router(config)# zone security OUTSIDE

Router(config)# interface gigabitEthernet 0/0
Router(config-if)# zone-member security INSIDE
Router(config-if)# exit

Router(config)# interface gigabitEthernet 0/1
Router(config-if)# zone-member security OUTSIDE
Router(config-if)# exit

Router(config)# class-map type inspect match-all INSIDE-TO-OUTSIDE
Router(config-cmap)# match protocol http
Router(config-cmap)# match protocol https
Router(config-cmap)# exit

Router(config)# policy-map type inspect INSIDE-TO-OUTSIDE-POLICY
Router(config-pmap)# class type inspect INSIDE-TO-OUTSIDE
Router(config-pmap-c)# inspect
Router(config-pmap-c)# exit
Router(config-pmap)# exit

Router(config)# zone-pair security IN-TO-OUT source INSIDE destination OUTSIDE
Router(config-sec-zone-pair)# service-policy type inspect INSIDE-TO-OUTSIDE-POLICY
```

### Security Best Practices Summary

1. **Password security**: Strong, unique, regularly changed
2. **Encryption**: Use SSH, HTTPS, IPsec
3. **Minimize services**: Disable unused ports/protocols
4. **ACLs**: Filter unnecessary traffic
5. **Regular updates**: Firmware, IOS, security patches
6. **Monitoring**: Logs, SNMP, IPS alerts
7. **Backup**: Regular configuration and data backups
8. **Physical security**: Lock equipment, badge access
9. **User training**: Security awareness
10. **Incident response plan**: Document procedures

---

## 14. Additional CCNA Topics

### Network Automation

#### Benefits
- **Consistency**: Eliminate human error
- **Speed**: Deploy changes rapidly
- **Scalability**: Manage thousands of devices
- **Documentation**: Configurations stored as code

#### Tools
- **Ansible**: Agentless automation, uses SSH
- **Python**: Scripting with netmiko, paramiko libraries
- **REST APIs**: Programmable interfaces (RESTCONF, NETCONF)
- **Puppet/Chef**: Configuration management

#### Basic Python Example
```python
from netmiko import ConnectHandler

device = {
    'device_type': 'cisco_ios',
    'host': '192.168.1.1',
    'username': 'admin',
    'password': 'password',
}

connection = ConnectHandler(**device)
output = connection.send_command('show ip interface brief')
print(output)
connection.disconnect()
```

### Quality of Service (QoS)

#### Purpose
- **Prioritize traffic**
- **Guarantee bandwidth** for critical applications
- **Reduce latency/jitter** for voice/video

#### QoS Mechanisms
- **Classification**: Identify traffic (by port, IP, DSCP)
- **Marking**: Label packets (CoS, DSCP, IP Precedence)
- **Policing**: Enforce rate limits
- **Shaping**: Smooth traffic to rate
- **Queuing**: Prioritize transmission
- **Congestion avoidance**: Prevent drops

#### QoS Models
- **Best Effort**: No QoS (default Internet)
- **IntServ**: Per-flow reservations (RSVP)
- **DiffServ**: Traffic classes (most common)

### Cloud Computing

#### Service Models
- **IaaS**: Infrastructure (VMs, storage) - AWS EC2, Azure VMs
- **PaaS**: Platform (runtime environment) - Heroku, Google App Engine
- **SaaS**: Software (applications) - Office 365, Salesforce

#### Deployment Models
- **Public cloud**: Shared infrastructure (AWS, Azure, GCP)
- **Private cloud**: Dedicated infrastructure
- **Hybrid cloud**: Mix of public and private
- **Multi-cloud**: Multiple public cloud providers

### SDN (Software-Defined Networking)

#### Concepts
- **Control plane**: Makes forwarding decisions (software)
- **Data plane**: Forwards traffic (hardware)
- **Separation**: Control centralized, data distributed

#### Controllers
- **Cisco ACI**: Application Centric Infrastructure
- **Cisco DNA Center**: Intent-based networking
- **OpenDaylight**: Open source controller

### Network Troubleshooting Methodology

#### Cisco's Structured Approach

1. **Define the problem**
   - Gather symptoms
   - Question users and devices
   - Narrow scope

2. **Gather information**
   - Check logs
   - Run diagnostic commands
   - Review documentation
   - Check recent changes

3. **Analyze information**
   - Identify symptoms
   - Determine problem scope
   - Form hypothesis

4. **Eliminate possible causes**
   - Question obvious
   - Use layered approach (OSI model)
   - Top-down, bottom-up, or divide-and-conquer

5. **Propose hypothesis**
   - Based on evidence
   - Consider multiple possibilities

6. **Test hypothesis**
   - Implement temporary fix
   - Observe results
   - Use known-good components

7. **Solve problem and document**
   - Implement permanent solution
   - Verify full functionality
   - Document solution
   - Update procedures

#### Troubleshooting Tools

**Physical Layer:**
- Cable tester
- Multimeter
- OTDR (fiber)
- Visual inspection

**Data Link Layer:**
- show interfaces
- show mac address-table
- show spanning-tree
- show etherchannel

**Network Layer:**
- ping
- traceroute
- show ip route
- show ip protocols

**Transport/Application:**
- telnet (test port connectivity)
- nslookup/dig (DNS)
- netstat (connections)
- Wireshark (packet capture)

### Final Exam Tips

#### Command Summary - Most Important

**General:**
- `enable` - Enter privileged EXEC mode
- `configure terminal` - Enter global config mode
- `hostname <name>` - Set device hostname
- `no shutdown` - Enable interface
- `exit` / `end` - Move up/exit config mode
- `copy running-config startup-config` - Save config
- `show running-config` - View active configuration
- `show startup-config` - View saved configuration

**Interface Configuration:**
- `interface <type> <number>` - Enter interface config
- `ip address <ip> <mask>` - Set IPv4 address
- `ipv6 address <ipv6/prefix>` - Set IPv6 address
- `description <text>` - Add interface description

**Show Commands:**
- `show ip interface brief` - Interface status summary
- `show interfaces` - Detailed interface info
- `show ip route` - Routing table
- `show mac address-table` - MAC table
- `show vlan brief` - VLAN summary
- `show running-config` - Current configuration

**Troubleshooting:**
- `ping <ip>` - Test connectivity
- `traceroute <ip>` - Trace packet path
- `show cdp neighbors` - View connected devices
- `show version` - IOS version and hardware info

#### Study Strategy
1. **Hands-on practice**: Use Packet Tracer extensively
2. **Understand concepts**: Don't just memorize commands
3. **Layer approach**: Think in terms of OSI model
4. **Practice subnetting**: Until it's automatic
5. **Know troubleshooting**: Use systematic methodology
6. **Review wrong answers**: Learn from mistakes
7. **Time management**: Don't spend too long on one question
8. **Read carefully**: Questions may have tricky wording

---

## Summary

These notes cover the core topics for CCNA certification:

✅ Network fundamentals and history  
✅ OSI and TCP/IP models  
✅ IPv4 addressing and subnetting  
✅ IPv6 addressing and configuration  
✅ Network applications (DNS, DHCP, HTTP)  
✅ Routing (static and dynamic)  
✅ Switching and VLANs  
✅ Wireless networking  
✅ WAN technologies  
✅ Network management  
✅ Security fundamentals  
✅ Automation and cloud concepts  

```

**Simplified notation:**
```
2001:db8:acad:1::/64
2001:db8:acad:2::/64
2001:db8:acad:10::/64
2001:db8:acad:A5::/64
```

#### Enterprise Subnet Planning

**Scenario**: Company receives 2001:db8:acad::/48

**Allocation example:**
```
2001:db8:acad:0001::/64  → Building 1, Floor 1
2001:db8:acad:0002::/64  → Building 1, Floor 2
2001:db8:acad:0100::/64  → Building 2, Floor 1
2001:db8:acad:0200::/64  → Building 3, Floor 1
2001:db8:acad:1000::/64  → Data center
2001:db8:acad:2000::/64  → Guest network
2001:db8:acad:FFFF::/64

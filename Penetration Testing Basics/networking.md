# Networking Cheat Sheet

## TCP/IP

### Layers:
1. **Application Layer**: Interfaces with applications to provide network services.
   - **Protocols**: HTTP, FTP, SMTP, DNS
2. **Transport Layer**: Ensures complete data transfer.
   - **Protocols**: TCP, UDP
   - **TCP**: Reliable, connection-oriented
   - **UDP**: Unreliable, connectionless
3. **Internet Layer**: Routes packets across networks.
   - **Protocols**: IP (IPv4, IPv6), ICMP
   - **IP**: Assigns addresses, routes data
   - **ICMP**: Error messages, diagnostics (e.g., ping)
4. **Network Interface Layer**: Manages hardware addressing and defines protocols for physical media.
   - **Examples**: Ethernet, Wi-Fi

### Key Concepts:
- **IP Address**: Unique identifier for devices on a network.
  - **IPv4**: `192.168.1.1` (32-bit address)
  - **IPv6**: `2001:0db8:85a3:0000:0000:8a2e:0370:7334` (128-bit address)
- **Subnet Mask**: Divides IP address into network and host parts.
  - Example: `255.255.255.0` (defines the network portion for IPv4)
- **Default Gateway**: Router IP address for forwarding data to external networks.
  - Example: `192.168.1.1`
- **NAT (Network Address Translation)**: Converts private IP addresses to a public IP address for internet access.
  - **Purpose**: Conserves public IP addresses, enhances security.

### TCP vs. UDP:
- **TCP (Transmission Control Protocol)**:
  - Connection-oriented: Establishes a connection before data transfer.
  - Reliable: Guarantees delivery, order, and error-checking.
  - Use Cases: Web browsing (HTTP/HTTPS), file transfer (FTP), email (SMTP).
- **UDP (User Datagram Protocol)**:
  - Connectionless: Sends data without establishing a connection.
  - Faster but less reliable: No guarantee of delivery or order.
  - Use Cases: Streaming media, online gaming, DNS queries.

## DNS (Domain Name System)

### Purpose:
- Translates human-readable domain names (e.g., `example.com`) to machine-readable IP addresses (e.g., `93.184.216.34`).

### Key Components:
- **Domain Names**: Readable addresses (e.g., `example.com`).
- **IP Addresses**: Numeric addresses assigned to devices (e.g., `93.184.216.34` for IPv4).
- **DNS Resolver**: Client-side component that queries DNS servers to resolve domain names.
- **Root Servers**: The top of the DNS hierarchy, direct queries to appropriate TLD servers.
- **TLD (Top-Level Domain) Servers**: Manage specific domain extensions (e.g., `.com`, `.net`).
- **Authoritative Servers**: Provide definitive answers for DNS queries about specific domains.

### Record Types:
- **A (Address) Record**: Maps a domain name to an IPv4 address.
- **AAAA (Quad-A) Record**: Maps a domain name to an IPv6 address.
- **CNAME (Canonical Name) Record**: Alias of one domain name to another.
- **MX (Mail Exchange) Record**: Specifies mail servers for email routing.
- **TXT (Text) Record**: Stores text information, often used for verification and security.

## VPN (Virtual Private Network)

### Purpose:
- Securely connects remote users or sites to a private network over the internet.

### Key Concepts:
- **Encryption**: Secures data by converting it into an unreadable format during transmission.
- **Tunneling**: Encapsulates network traffic within a secure, encrypted connection.
- **VPN Protocols**: Methods used to establish and maintain VPN connections.
  - **PPTP (Point-to-Point Tunneling Protocol)**: Simple, less secure, older protocol.
  - **L2TP/IPsec (Layer 2 Tunneling Protocol with IPsec)**: Combines L2TP's tunneling with IPsec's security.
  - **OpenVPN**: Open-source, highly secure, supports multiple encryption standards.
  - **IKEv2/IPsec (Internet Key Exchange version 2)**: Fast, secure, resilient to network changes, ideal for mobile users.

### Types of VPNs:
- **Remote Access VPN**: Allows individual users to connect to a private network from remote locations.
  - Example: Employees accessing company resources from home.
- **Site-to-Site VPN**: Connects entire networks (e.g., branch offices) to each other securely over the internet.
  - Example: Connecting the network of a company's headquarters with its branch office.

### Common Uses:
- **Privacy**: Hides user's IP address and encrypts online activity, preventing tracking and monitoring.
- **Security**: Protects data from eavesdropping, especially on public Wi-Fi networks.
- **Access Control**: Provides secure access to restricted or region-locked resources.

# Networking

#### what is TCP IP protocol
TCP/IP (Transmission Control Protocol/Internet Protocol) is a set of communication protocols used to connect network devices on the internet. It defines how data should be transmitted, routed, and received across networks . TCP (Transmission Control Protocol): Ensures reliable, ordered delivery of data between applications.
IP (Internet Protocol): Handles addressing and routing of data packets to ensure they reach the correct destination.


 
 
#### Explain OSI model
OSI (Open Systems Interconnection)
the OSI model helps us understand the different parts involved in sending and receiving data over a network, from the physical wires to the software applications

Each layer serves a specific purpose and interacts with adjacent layers to facilitate communication between devices
 
 
#### What is IP ADDRESS ?
  An IP (Internet Protocol) address is a unique string of numbers separated by periods (for IPv4) or colons (for IPv6) that identifies each computer using the Internet Protocol to communicate over a network. IP addresses are essential for routing data between devices on a network or across the internet.
 
#### What is the difference between  public key and  private key?
Public Key: Used for encryption and verification. Shared openly.
Private Key: Used for decryption and signing. Kept secret by the owner
 
#### Protocols and Port numbers
- FTP --- File Transfer Protocol --- 21
- SMTP --- Simple Mail Transfer Protocol --- 25
- TELNET --- Terminal  Network  ---  21
  -  DNS --- Domain Name Systems --- 53
- HTTP --- Hypertext Transfer Protocol --- 80
- HTTPS  --- Hypertext Transfer Protocol Secure --- 443 / 8443
- RDP ---  Remote Desktop Protocol  --- 3389
- SSH  ---  Secure Shell --- 22
- RDS for MYSQL   ---   3306
- RDS for  DB2   ---   50000


 
#### Explain Network topology
- Network topology refers to the layout or structure of a computer network, defining how devices are interconnected and how data flows between them. It describes both the physical and logical arrangement of devices, cables, and other components that make up the network.
- Star: Devices connect to a central hub or switch.
- Bus: Devices connect along a single cable.
- Ring: Devices connect in a closed loop.
- Mesh: Devices connect with multiple paths.
- Tree: Hierarchical structure of interconnected star networks.
- Hybrid: Combination of different topologies for flexibility.

#### 7.  What do you mean by Look back address ?
The term "loopback address" typically refers to a special IP address used to send network traffic back to the same device. In IPv4, the loopback address is 127.0.0.1, while in IPv6, it's represented as "::1".
This loopback address allows a device to communicate with itself, useful for testing network applications or troubleshooting connectivity issues. When a device sends data to the loopback address, it's routed internally within the device without being transmitted over the network.


#### 8.  Explain Reverse proxy concept
A reverse proxy sits between clients and backend servers, forwarding client requests to the appropriate backend server and returning the response to the client. It improves performance, security, and reliability by load balancing, caching, SSL termination, and URL rewriting.



What are the differences between HTTP and HTTPS?
HTTP (HyperText Transfer Protocol): A protocol used for transmitting data over the web. It is not encrypted, making it vulnerable to interception.
HTTPS (HyperText Transfer Protocol Secure): An extension of HTTP that uses encryption (SSL/TLS) to secure data transmitted between the client and server, providing confidentiality and integrity.

How do you handle and resolve CPU-related tickets?
To handle CPU-related tickets, you would:
Analyze resource usage and identify processes consuming high CPU.
Check for resource limits and requests in Kubernetes or other environments.
Optimize application performance, adjust configurations, or scale resources as needed.
Implement monitoring and alerts to proactively manage CPU utilization.

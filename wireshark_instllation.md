
# Lab 0: Basic wireshark operation and capture
- [Lab 0: Basic wireshark operation and capture](#lab-0-basic-wireshark-operation-and-capture)
  - [1.Wireshark Installation Guide (Windows)](#1wireshark-installation-guide-windows)
  - [2. Capture packets: access the NTUST homepage (https://www.ntust.edu.tw/home.php)](#2-capture-packets-access-the-ntust-homepage-httpswwwntustedutwhomephp)
    - [2.1 Q: What is the IP address and port of the NTUST homepage (https://www.ntust.edu.tw/home.php)?](#21-q-what-is-the-ip-address-and-port-of-the-ntust-homepage-httpswwwntustedutwhomephp)
    - [2.2 Q: What is the IP address and port of your PC when initially accessing the page?](#22-q-what-is-the-ip-address-and-port-of-your-pc-when-initially-accessing-the-page)
    - [2.3 What is the process of the TCP three-way handshake?](#23-what-is-the-process-of-the-tcp-three-way-handshake)
  - [3. Use the filter dns to find a DNS packet](#3-use-the-filter-dns-to-find-a-dns-packet)
    - [3.1 What is the IP address and port of the DNS server?](#31-what-is-the-ip-address-and-port-of-the-dns-server)
    - [3.2 What is the domain name in this query?](#32-what-is-the-domain-name-in-this-query)
    - [3.3 Which protocol(s) does this DNS packet use? (List the protocols from Layer 2 — Link Layer — up to Layer 5 — Application Layer in the TCP/IP five-layer model.)](#33-which-protocols-does-this-dns-packet-use-list-the-protocols-from-layer-2--link-layer--up-to-layer-5--application-layer-in-the-tcpip-five-layer-model)

## 1.Wireshark Installation Guide (Windows)
Go to [wireshark website](https://www.wireshark.org/download.html) and choose version to download 

Choose Components you want to install\
![alt text](image/image-3.png)

Creat the icon in desktop\
![alt text](image/image-4.png)

Install Npcap (In this PC is already have)\
![alt text](image/image-8.png)

Install USBPcap and wireshark\
![alt text](image/image-9.png)

Reboot PC\
![alt text](image/image-10.png)

## 2. Capture packets: access the NTUST homepage (https://www.ntust.edu.tw/home.php)


![alt text](image/image-12.png)

### 2.1 Q: What is the IP address and port of the NTUST homepage (https://www.ntust.edu.tw/home.php)?

- A: IP adress is `140.118.31.124` ,port is `443` (from Dst Port).

### 2.2 Q: What is the IP address and port of your PC when initially accessing the page?

- A: IP adress is `192.168.1.105`, port is `63410` (from Src Port).

### 2.3 What is the process of the TCP three-way handshake?
- SYN: Client sends SYN to server.\
![alt text](image/image-13.png)

- SYN-ACK: Server replies with SYN-ACK.\
![alt text](image/image-14.png)

- ACK: Client sends ACK. Connection established.\
![alt text](image/image-15.png)


## 3. Use the filter dns to find a DNS packet

![alt text](image/image-16.png)

### 3.1 What is the IP address and port of the DNS server?
- IP adress is `192.168.1.1` ,port is `53` (from Dst Port).

### 3.2 What is the domain name in this query?

- The domain name in the query is [www.ntust.edu.tw](https://www.ntust.edu.tw/)

### 3.3 Which protocol(s) does this DNS packet use? (List the protocols from Layer 2 — Link Layer — up to Layer 5 — Application Layer in the TCP/IP five-layer model.)

![alt text](image/image-17.png)

- Layer 2 (Link Layer): Ethernet II
- Layer 3 (Network Layer): Internet Protocol Version 4 (IPv4)
- Layer 4 (Transport Layer): User Datagram Protocol (UDP)
- Layer 5 (Application Layer): Domain Name System (DNS)


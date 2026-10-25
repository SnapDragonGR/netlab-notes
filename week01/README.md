# Week 1

Done when: captured a TCP handshake, DNS lookup and ARP exchange, annotated.

## What I did
### OSI Model & TCP / IP model  

| OSI | TCP/IP |
|---|---|
| 7 Application | 4 Application |
| 6 Presentation | 4 Application |
| 5 Session | 4 Application |
| 4 Transport | 3 Transport |
| 3 Network | 2 Internet |
| 2 Data Link | 1 Link |
| 1 Physical | 1 Link |

Conceptual model made by ISO to standardazie the different functions in a network.  
Layer Summary:  
7 - closest to the end user. HTTP / HTTPS. Interacts with Software Apps. Identifies communication partners and synchronizes communication.  
6 - Translates between application and network formats. Encryption / decryption of data. Translated between Application - Layer formats.  
5 - controls sessions between hosts. Manages connections btw local app and remote app (browser - YouTube).  

7, 6, 5 - mostly app devs work with them.  

4 - breaks large pieces of data into smaller segments for easier sending. Process-to-process communication.  
3 - connectivity btw end hosts on different networks  (outside LAN). IP addresses. Path selection. Routers are here.
2 - node-to-node connectivity and data transfer (ex. PC to Switch). Formatting for transmission over a physical medium. Detects and corrects layer 1 errors. Separate addressing from Layer 3. Switches are here.  
1 - physical characteristics: voltages, distances, physical connectors, cables. Digital bits converted into electrical or radio signals.

TCP/IP:
Actually used in modern networks. OSI is still important.  
4 - Layers 7, 6, 5 OSI = TCP/IP Layer 4.  
4 OSI = 3 TCP IP.  
3 OSI = 2 Internet TCP IP.  
2 + 1 OSI = 1 TCP IP.


  
Encapsulation:  
### Encapsulation

1. **Application (7, 6, 5):** data is prepared
2. **Transport (4):** add L4 header → **Segment**
3. **Network (3):** add L3 header → **Packet**
4. **Data Link (2):** add L2 header and L2 trailer → **Frame**
5. **Physical (1):** the frame is sent over the cable as **Bits**

Final frame layout: `L2 header | L3 header | L4 header | Data | L2 trailer`

De-encapsulation:
Same is encapsulation but reversed order - remove tailer and header as we go up the model.  
Get Data at the end - 7, 6, 5.

![Data Flow and Network Topology Diagram](data-flow.png)

## What broke
...

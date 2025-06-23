# Project 3: Network Traffic Analysis with Wireshark

## Objective

The objective of this project was to use Wireshark on an Ubuntu machine to capture and analyze real-time network traffic. The goal was to observe, interpret, and understand common network protocols, monitor live traffic, and practice filtering and analyzing packets in a structured lab setup.

### Skills Learned

- Understanding how to capture live traffic using Wireshark.
- Familiarity with interpreting common protocols like ICMP, DNS, HTTP, and TCP handshakes.
- Proficiency in applying display filters to isolate specific communication.
- Ability to detect common anomalies or misconfigurations in traffic.
- Competence in exporting and analyzing .pcap files.

### Tools Used

Wireshark – for live packet capture and inspection.
Ubuntu – as the analysis system and traffic source.

Built-in Ubuntu tools:

ping – to generate ICMP traffic.
curl – to initiate HTTP requests.
dig – to perform DNS lookups.

## Steps
Ref 1: Launching Wireshark and Selecting Network Interface
Wireshark was opened on Ubuntu. The active Ethernet interface (usually eth0 or ens33) was selected to begin live capture.
![image](https://github.com/user-attachments/assets/873b493f-5849-46f3-99a4-7d4f30c60c68)

Ref 2: Capturing ICMP Packets Using Ping
A terminal window was used to ping Google's DNS server:Wireshark captured the ICMP Echo Request and Reply packets. These were examined for TTL, packet size, and response time
![image](https://github.com/user-attachments/assets/ada9337b-928e-4b17-a4d7-fb4dec67bec6)

Ref 3: Applying Filters and Exporting .pcap File
Display filters like ip.addr == 192.168.31.131 and tcp.port == 80 were used to narrow down relevant traffic. The capture was saved as a .pcap file for further offline analysis and documentation.
![image](https://github.com/user-attachments/assets/a0c6f379-c980-477e-82cd-2f01da8124bb)
![image](https://github.com/user-attachments/assets/c1b23cbc-0105-4660-82b0-5c1098efc556)
![image](https://github.com/user-attachments/assets/c8e4d84a-0407-4174-9d88-b800d7bbfe60)
![image](https://github.com/user-attachments/assets/78dab3bd-d9dd-403a-b47e-6ee2f95e6db1)

Ref 4 : Follow TCP/UDP Stream
![image](https://github.com/user-attachments/assets/d1b417f0-e466-4a09-95e1-9deb53133c3b)

Ref 5 : Inspect Packet Content
Expand the packet content to inspect the header and the payload of each layer
![image](https://github.com/user-attachments/assets/4990e9ef-3b5a-416e-bed0-523f1b6b1bd6)

Ref 6 : Use Built-in Tool Analysis
Explored the statistics menu to find tools like 
a)protocol Hierarchy : View breakdowns of protocols used in this capture
![image](https://github.com/user-attachments/assets/7a04bc00-9f02-43f4-ac0c-2703ebd8729f)

b)Conversations : See communication pairs and their traffic statistics
![image](https://github.com/user-attachments/assets/765e2cb1-4ed0-4ec7-9d1e-90a017674182)

c)Endpoints : View traffic statistics for individual endpoints
![image](https://github.com/user-attachments/assets/3deaad21-f982-42be-b1ad-bd6fec5c644c)

Outcome
Using only the Ubuntu system, Wireshark was successfully used to capture and analyze real-time network communication. This provided valuable insights into protocol behavior and foundational experience for later deep-packet inspection, threat hunting, or forensic analysis.



















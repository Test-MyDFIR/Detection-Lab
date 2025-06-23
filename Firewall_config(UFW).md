# Project 2: Build and Configure a Firewall Using UFW

## Objective


The objective of this project was to understand and implement basic firewall configurations using UFW (Uncomplicated Firewall) on a Linux system. The project involved setting default policies, allowing and denying specific ports/services, and testing the firewall's effectiveness. This hands-on experience helps reinforce fundamental concepts in network security and host-based protection.

### Skills Learned


- Understanding of host-based firewalls and their role in layered security.
- Proficiency in using UFW to control inbound and outbound traffic.
- Ability to configure secure defaults and write rules based on security needs.
- Skills in verifying and troubleshooting firewall configurations.
- Increased awareness of network services and their associated ports.

### Tools Used


- UFW (Uncomplicated Firewall) – to manage firewall rules.
- Linux (Ubuntu) – as the host operating system.
- Netcat / Nmap – for testing open and closed ports.
- SSH – for remote access configuration and testing.

## Steps
Ref 1: Enable UFW and Set Default Policies
This screenshot shows UFW being enabled and the default policies being set to deny all incoming and allow all outgoing connections — a secure starting point
![image](https://github.com/user-attachments/assets/0effd782-e831-4dc2-a9dc-84d15735808b)


Ref 2: Allow Specific Services (e.g., SSH and HTTP)
This screenshot demonstrates allowing SSH for remote login and HTTP for web services. Specific ports were opened to maintain functionality while minimizing exposure.
![image](https://github.com/user-attachments/assets/044bde85-00ed-47ee-8f11-52987a759ab1)

Ref 3: Deny Specific IPs or Ports (e.g., block ping or a malicious IP)
In this screenshot, a known malicious IP is blocked and ICMP requests are denied to prevent ping-based reconnaissance.
![image](https://github.com/user-attachments/assets/63c0610c-32ba-4640-99df-f5951741d880)

Ref 4: Checking UFW Status and Active Rules
This screenshot shows all active firewall rules with numbers assigned, making it easy to track or remove rules later.
![image](https://github.com/user-attachments/assets/9062116a-2b4f-44bd-a442-4242f29ae6d3)

Ref 5: Testing with Nmap and Netcat
Testing screenshots demonstrate how nmap was used from another system to scan for open ports and netcat to verify rule enforcement.
![image](https://github.com/user-attachments/assets/51b0a673-96fc-42aa-8d44-371c8498c1e6)


Outcome
By the end of this project, a secure host-based firewall was configured using UFW. It restricted unnecessary access while allowing only essential services. Testing confirmed that the firewall effectively blocked or allowed traffic as configured.




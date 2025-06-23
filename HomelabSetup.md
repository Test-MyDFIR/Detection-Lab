#  Set Up a Home Lab for Attack Simulation and Defense Analysis

## Objective


The objective of this project was to create a controlled lab environment with Ubuntu and Kali Linux virtual machines. This setup was used to simulate cyber attacks, analyze network traffic using Wireshark, and observe logs and security events in real-time, enhancing practical cybersecurity skills

### Skills Learned


- Practical configuration of virtual machines and virtual networks.
- Attack simulation techniques using Kali Linux tools.
- Network traffic inspection and filtering with Wireshark.
- Identification of suspicious patterns and behavior.
- Understanding of basic IDS/IPS and firewall reactions to attacks.

### Tools Used


- VirtualBox – For creating and managing virtual machines.
- Ubuntu – Used as the target system in the simulated network.
- Kali Linux – Used as the attacker machine with pre-installed penetration testing tools.
- Wireshark – For capturing and analyzing network traffic.
- nmap – Network scanning tool to perform reconnaissance from Kali.
- ufw (Uncomplicated Firewall) – Basic firewall configuration on Ubuntu.
- Metasploit Framework – For simulating advanced exploits and payloads.

## Steps
Step 1: Install VirtualBox
1. Download VirtualBox

Visit the official site: https://www.virtualbox.org/wiki/Downloads
Choose the installer for your OS (Windows/macOS/Linux).

2. Install VirtualBox

Windows: Run the .exe file and follow setup prompts.
macOS: Open the .dmg file and move the VirtualBox icon to Applications.

3. Install VirtualBox Extension Pack

Download it from the same downloads page.
Go to File → Preferences → Extensions, then click Add New Package and install the extension.

Step 2: Set Up Virtual Machines
1. Download OS Images
Ubuntu: https://ubuntu.com/download/desktop
Kali Linux: https://www.kali.org/downloads/


2.Create VMs in VirtualBox
Launch VirtualBox → Click New.
Name your VM (e.g., Ubuntu, Kali).
Allocate RAM (2-4 GB recommended per VM).
Attach the downloaded ISO to install the OS.

Step 3: Simulate a Network Attack
1. Configure Network Settings

Set both VMs (Ubuntu & Kali) to use Internal Network or Host-Only Adapter to simulate isolated traffic.
Ensure both machines can ping each other to confirm connectivity.

2. Launch Kali Linux (Attacker VM)

Open terminal and use tools like nmap to simulate scans or exploit attempts against ubuntu VM
![image](https://github.com/user-attachments/assets/c03349e3-a7a5-4e5c-842a-272a97e144cb)

3. Launch Ubuntu (Target VM)

- Ensure ufw (firewall) is active:

sudo ufw enable

- Monitor incoming traffic using Wireshark:

Start capture on the relevant network interface.
Filter by protocol (e.g., tcp, icmp, http).

Step 4: Analyze Network Traffic Using Wireshark
1. Install Wireshark on Ubuntu

sudo apt update && sudo apt install wireshark

2. Capture Traffic

Open Wireshark and start capturing.
Analyze suspicious packets (e.g., SYN floods, ICMP echo requests).

Sample Screenshot & Explanation
Ref 1: VirtualBox Configuration

This screenshot shows VirtualBox with Ubuntu and Kali Linux VMs configured. Both are set to use an internal network to isolate traffic within the lab.

Ref 2: Wireshark Packet Capture

Captured ICMP ping requests and port scans from Kali to Ubuntu. Highlighted packets indicate reconnaissance activity, forming the basis of further analysis and defensive logging.
![image](https://github.com/user-attachments/assets/e7328830-3a4b-40f3-9bab-e5456926b419)


Ref 3 : Network Diagram
![image](https://github.com/user-attachments/assets/7954fcff-095c-4e8b-a3cc-ffd85c71ec6e)


# Elevate-labs

# Task 1 – Scan Your Local Network for Open Ports using Nmap

## Objective

The goal of this task is to perform a **TCP SYN scan** using `nmap` to discover active devices and open ports within a local network. This helps understand **network exposure**, assess **potential risks**, and develop basic **network reconnaissance skills**.

---

## Tools & Technologies

- **Nmap**: Open-source network scanning tool
- **Operating Systems**:
  - Ubuntu (Linux Terminal)
  - Kali Linux (Security Testing Environment)
- Wireshark for packet analysis(here, i used only for kali)

---

## Method 1: Ubuntu (Linux Terminal)

### Step 1: Install Nmap

I used these commands to install:

- sudo apt update
- sudo apt install nmap
  
<img src="https://github.com/user-attachments/assets/d6dccd07-2280-4107-a2fc-c70d1328ab95" width="600"/>
  
### Step 2: Finding local IP range

I used the command - ip a
It shows the Network Info as
- Scanned Range: `172.21.96.0/20`
- Local Machine IP: `172.21.108.213`

<img src="https://github.com/user-attachments/assets/a2df784b-03c9-4995-bfd6-efbcd1b29a9a" width="600"/>

### Step 3: To perform TCP-SYN-scan and saving results as a text file

used this command - sudo nmap -sS 172.21.96.0/20 -oN TCP-SYN-scan-results.txt

<img src="https://github.com/user-attachments/assets/b7abf6e7-6a3d-4aa0-86e4-dcf3ed3a566e" width="600"/>

Here, in this we can see that all ports are filtered, it means the host is reachable, but a firewall is blocking or dropping all port responses. so, trying with kali the same thing to see any open ports.

### Step 6: Research Common Services
In this scan, no open ports were found on the active devices. One host (172.21.96.1) had all ports filtered, which likely means a firewall is blocking scan attempts. The other host (172.21.108.213) had all ports closed, meaning no services are currently listening.

### Step 7: Identify Potential Security Risks
Since no ports were open, there were no immediate exposed services found on the scanned hosts. The filtered status on one device is a good sign of firewall protection, and closed ports indicate that the device isn’t running unnecessary services. Overall, the network appears to be secure with minimal exposure.


---


## Method 2: kali version

### Step 1 and 2: Install Nmap and finding ip

I followed the step 1 and step2 same to find the local ip range using "ip a" command

The Network Info
- Scanned Range: `192.168.236.0/24`
- Local IP: `192.168.236.15`
the result is as follows for this kali version:

<img src="https://github.com/user-attachments/assets/2f9edd4f-52f0-4518-a616-afe12673e769" width="600"/>

### Step 3:To perform TCP-SYN-scan and saving results as a text file(kali version)

<img src="https://github.com/user-attachments/assets/02133e7a-b592-4627-97fd-d796f762ebf4" width="600"/>

- Verification: for this, i used cat kali-scan-results.txt command to verify the text file content

### Step 4: Note IP Addresses and Open Ports
After running the scan, I reviewed the results from step 3 figure, to identify which IP addresses were active and whether any ports were open. Out of the scanned range, three devices were found to be active. Among them, only one device had an open port (53/tcp), while the others had all ports either closed or filtered. This helps in understanding which devices are visible on the network and what services they might be exposing.

### Step 5: Wireshark analysis(kali)

Here, in kali, followed same procedure as ubuntu till the third step then, open Wireshark and started packet capturing while running nmap command in the terminal and filtered the TCP SYN  responses in real time using filter "tcp.flags.syn==1 && tcp.flags.ack==0" and saved the pcap file.

<img src="https://github.com/user-attachments/assets/3398644e-1bb0-49b8-8033-e6bdea6c06d6" width="600"/>

### Step 6: Research Common Services
The scan found only one open port: 53/tcp, which is used for DNS (Domain Name System). This service is usually found on routers or servers to resolve domain names. In this case, it was found on 192.168.236.138, which may be a router or a device running DNS. If it's not meant to run DNS, this could be a misconfiguration.

### Step 7: Identify Potential Security Risks
An open DNS port on a normal device can be risky if not needed — it may allow misuse like DNS tunneling. The other devices had all ports closed or filtered, which is good because it means no unnecessary services are exposed and firewalls may be protecting them.





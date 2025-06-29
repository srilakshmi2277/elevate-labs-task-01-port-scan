# Elevate-labs

## Task 1: Scan Your Local Network for Open Ports using Nmap(June 23, 2025)

Here, in this task, I used **Nmap** to perform TCP SYN scans on local networks in both **Ubuntu** and **Kali Linux** environments. The goal was to detect active devices, identify open ports, and understand potential exposure within the local network.

- On **Ubuntu**, I scanned the range `172.21.96.0/20` and found two hosts — one with all ports filtered (likely behind a firewall), and another with all ports closed. No open ports were found in this environment in my system. so, next i tried in kali environment. 
- In **Kali**, I scanned `192.168.236.0/24` and identified three active devices. One of them had **port 53/tcp** which is a DNS service open, while the others had closed or filtered ports. I also used **Wireshark** in Kali to analyze TCP SYN packets in real-time.

**Full PDF Report:**   [Task 1 – Scan Your Local Network for Open Ports using Nmap](Daily_Task_Documents/Elevate_Labs_Task_1.pdf)


---


## Task 2: Analyze a Phishing Email Sample(June 24,2025)

- Here, In this task, I created and analyzed a fake phishing email to understand how phishing works. I made an email that looked like it was from Samsung, offering a free Galaxy S25 Ultra, and sent it from a ProtonMail account. I checked the sender’s email, the link, the message style, and other signs like mismatched URLs. In detail, all the steps are explained in my report below:

**Full PDF Report:** [Task 2 – Analyze a Phishing Email Sample](Daily_Task_Documents/Elevate_Labs_Task_2.pdf)


---

## Task 3: Perform a Basic Vulnerability Scan on Your PC(June 26,2025)

- Tools Used: Nessus Essentials.
- Performed a basic vulnerability assessment on my PC using Nessus Essentials as part of a security task. Initially tried scanning with my local IP, but switched to 127.0.0.1 as the target due to host detection issues. Completed the scan successfully and documented the process in my report below:

**Full PDF Report:** [Task 3 – Basic Vulnerability Scan on Your PC](Daily_Task_Documents/Elevate_Labs_Task_3.pdf)

---

## Task 4: Setup and Use a Firewall on Windows/Linux(June 27,2025)

- Tools Used: Windows Firewall
- Here, Using the built-in firewall tool, I configured and tested basic firewall rules on Windows. I blocked and tested Telnet (port 23), allowed SSH (port 22), and learned how firewalls use rules to filter and protect network traffic.
  
**Full PDF Report:** [Task 4 – Setup and Use a Firewall on Windows](Daily_Task_Documents/Elevate_Labs_Task_4.pdf)


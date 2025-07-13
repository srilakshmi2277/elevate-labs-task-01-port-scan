# Elevate-labs

## Task 1: Scan Your Local Network for Open Ports using Nmap(June 23, 2025)

Here, in this task, I used **Nmap** to perform TCP SYN scans on local networks in both **Ubuntu** and **Kali Linux** environments. The goal was to detect active devices, identify open ports, and understand potential exposure within the local network.

- On **Ubuntu**, I scanned the range `172.21.96.0/20` and found two hosts — one with all ports filtered (likely behind a firewall), and another with all ports closed. No open ports were found in this environment in my system. so, next i tried in kali environment. 
- In **Kali**, I scanned `192.168.236.0/24` and identified three active devices. One of them had **port 53/tcp** which is a DNS service open, while the others had closed or filtered ports. I also used **Wireshark** in Kali to analyze TCP SYN packets in real-time.

**Full PDF Report:**   [Task 1 – Scan Your Local Network for Open Ports using Nmap](https://drive.google.com/file/d/1h5wdvuC0LHkDTtCtPq6SNmOMwi7hfAGj/view?usp=drive_link)



## Task 2: Analyze a Phishing Email Sample(June 24,2025)

- Here, In this task, I created and analyzed a fake phishing email to understand how phishing works. I made an email that looked like it was from Samsung, offering a free Galaxy S25 Ultra, and sent it from a ProtonMail account. I checked the sender’s email, the link, the message style, and other signs like mismatched URLs. In detail, all the steps are explained in my report below:

**Full PDF Report:** [Task 2 – Analyze a Phishing Email Sample](Daily_Task_Documents/Elevate_Labs_Task_2.pdf)



## Task 3: Perform a Basic Vulnerability Scan on Your PC(June 26,2025)

- Tools Used: Nessus Essentials.
- Performed a basic vulnerability assessment on my PC using Nessus Essentials as part of a security task. Initially tried scanning with my local IP, but switched to 127.0.0.1 as the target due to host detection issues. Completed the scan successfully and documented the process in my report below:

**Full PDF Report:** [Task 3 – Basic Vulnerability Scan on Your PC](Daily_Task_Documents/Elevate_Labs_Task_3.pdf)



## Task 4: Setup and Use a Firewall on Windows/Linux(June 27,2025)

- Tools Used: Windows Firewall
- Here, Using the built-in firewall tool, I configured and tested basic firewall rules on Windows. I blocked and tested Telnet (port 23), allowed SSH (port 22), and learned how firewalls use rules to filter and protect network traffic.
  
**Full PDF Report:** [Task 4 – Setup and Use a Firewall on Windows](Daily_Task_Documents/Elevate_Labs_Task_4.pdf)



## Task 5: Capture and Analyze Network Traffic Using Wireshark(June 30,2025)

- Tools Used: Wireshark, Ubuntu
- Here, I used Wireshark on Linux with eth0 interface to capture live network traffic. I filtered and checked each protocol, then saved the capture as a .pcap file. Documented the process and steps in my report below:
  
**Full PDF Report:** [Task 5 - Capture and Analyze Network Traffic Using Wireshark](Daily_Task_Documents/Elevate_Labs_Task_5.pdf)



## Task 6: Create a Strong Password and Evaluate Its Strength(July 1,2025)

- Tools Used: The Password Meter(online free version)
- Here, I created and tested six passwords with different strengths using a password checker and noted their scores and learned what makes a strong password. Documented my observations in the report below:
  
**Full PDF Report:** [Task 6 - Create a Strong Password and Evaluate Its Strength.](Daily_Task_Documents/Elevate_Labs_Task_6.pdf)


## Task 7 :Identify and Remove Suspicious Browser Extensions(July 3,2025) 

- Tools Used: Chrome web browser
- Here in this task, I reviewed all Chrome extensions, checked their permissions, identified unused or risky ones, and removed Volume Booster due to unnecessary access to all website data.
  
**Full PDF Report:** [Task 7 - Identify and Remove Suspicious Browser Extensions .](Daily_Task_Documents/Elevate_Labs_Task_6.pdf)




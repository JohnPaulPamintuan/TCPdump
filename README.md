<h1>Network traffic Analysis and using TCPdump and Wireshark</h1> 

<h2>Network Traffic Analysis (NTA)</h2>
Network Traffic Analysis (NTA) refers to the process of monitoring and analyzing network traffic to detect anomalies, performance issues, or security threats. NTA helps organizations understand what is happening within their network by providing visibility into network communications in real time or through historical logs. It is essential for improving security posture, optimizing performance, and troubleshooting network-related problems.<br />


<h2>Everyday use cases of NTA includes:</h2>

- <b>Collecting</b>  real-time traffic within the network to analyze upcoming threats.
- <b>Setting</b> a baseline for day-to-day network communications.
- <b>Identifying</b> and analyzing traffic from non-standard ports, suspicious hosts, and issues with networking protocols such as HTTP errors, problems with TCP, or other networking misconfigurations.
- <b>Detecting</b> malware on the wire, such as ransomware, exploits, and non-standard interactions.




<h2>Description</h2>
Project consists of the basics of security features in Windows Operating System using Windows Defender Antivirus. The process of configuring and managing Windows Defender Antivirus is a crucial component in protecting computer systems from unauthorized access and threats.<br />



<h2>Learning Ojectives</h2>

- <b>Locate Microsoft Windows Security Virus and Threat Protection</b> 
- <b>Review Microsoft Windows Security Virus and Threat Protection and Update Threat Definitions</b>
- <b>Run Microsoft Windows Defender Antivirus Quick Scan and Review Threat History</b> 
- <b>Configure Firewall Rules using Microsoft Windows Defender Firewall with and without Advanced Security</b>


<h2>Understanding Windows Defender Antivirus</h2>
Windows Defender Antivirus, also known as Microsoft Defender Antivirus, is a robust security solution integrated into the Windows operating system. It provides real-time protection against various types of malware, including viruses, worms, and spyware. This reading focuses on understanding the functionalities, configuration, and management of Windows Defender Antivirus.

Some important functions of Windows Defender Antivirus are listed below-
1. Real-Time Protection: Windows Defender Antivirus offers several types of scans to ensure comprehensive protection, which includes *<b>Quick Scan, Full Scan, Custom Scan, Offline Scan and Schedule Scan*.</b>

<img src="https://i.imgur.com/Bx7wsNQ.jpeg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />

- <b>Quick Scan</b>  Allows the user to scan the areas of the system that are most likely to be targeted by malware. This scan is faster but less comprehensive. Here's what it typically involves:

  - <ins>Memory Scan</ins>:Checks for active malware in your computer's memory.
  - <ins>System Files</ins>: Scans all files and running programs on your hard disk. This scan is more thorough and can take several hours to complete, depending on the size of your drive and the number of files.
  -  <ins>Registry Entries</ins>: Examines Windows Registry entries that are commonly used by malware to execute upon startup.
  - <ins>Common Malware Locations</ins>: Scans common locations where malware is known to reside, such as the Windows directory and temporary files.
- <b>Full scan</b>:This option thoroughly scans the entire system for threats.
- <b>Custom Scan</b>:This option allows the user to select specific files and folders to scan. This is useful if you suspect a particular area of your computer is infected.
- <b>Offline Scan</b>:This option allows users to scan the system before the operating system loads to detect and remove persistent threats.
- <b>Schedule Scan</b>:This can be set up using the Task Scheduler to run regular scans at specified date and time to maintain system health.<br />

2. <b>Exclusions</b>:
This option allows users to specify files, folders, and processes to be excluded from scans. After a scan is completed, Windows Defender Antivirus provides detailed results, which can be accessed through the Windows Security Center. Actions based on scan results include:
- <b>Quarantine</b>: Isolating detected threats to prevent them from harming the system.
- <b>Remove</b>: Deleting detected threats from the system.
- <b>Allow</b>: Permitting certain detected items if they are known to be safe (adding to exclusions)
<img src="https://i.imgur.com/xnu3LG7.jpeg" height="60%" width="50%" alt="Disk Sanitization Steps"/>

3. <b>Temper Protection</b>: 
Tamper Protection is a feature in Windows Security that helps prevent malicious apps from changing important security settings, including real-time protection and cloud-delivered protection.

<img src="https://i.imgur.com/xnu3LG7.jpeg" height="60%" width="50%" alt="Disk Sanitization Steps"/>


4. <b>Automatic Sample Submission</b>: 
Automatic Sample Submission is a feature in Windows Defender that helps protect your computer by automatically sending samples of suspicious files to Microsoft for analysis.

<img src="https://i.imgur.com/XzAuGOD.jpeg" height="60%" width="50%" alt="Disk Sanitization Steps"/>

5. <b>Regular Updates</b>: 
Automatic Sample Submission is a feature in Windows Defender that helps protect your computer by automatically sending samples of suspicious files to Microsoft for analysis.




<h2>Understanding Windows Firewall </h2>
A firewall is one of the most effective methods for securing your network from external threats. In a non-technical setting, a firewall is a physical, fire-resistant wall that is designed to keep a fire from spreading from one area to the next. Similarly, a computer security firewall is a software program or a hardware device that is designed to keep malicious threats from spreading from the public network to a private network or device. Firewalls provide defense against spyware, virus attacks, and hacking. They can also help to ensure that sensitive information is kept private. 

- <b>Functions of Firewalls</b>
  - <ins>Threat Mitigation</ins>: Firewalls help prevent unauthorized access and cyber-attacks by blocking malicious traffic.
  - <ins>Traffic Control</ins>: They regulate network traffic, allowing only legitimate communication.
  - <ins>Enhanced Security</ins>: By setting rules, firewalls protect sensitive data and ensure compliance with security
 
- <b>Types of Firewalls</b>
  - <ins>Software</ins> – or host-based firewalls are programs that are installed on a computer. Most modern operating systems have built-in firewall software. Microsoft, for example, provides Windows Defender Firewall. These built-in firewalls help to monitor port traffic and traffic between applications.
  - <ins>Hardware</ins> – or network-based firewalls are deployed between a network and an internet gateway. In-home or small business settings, a router often has built-in firewall protection to stop unwanted traffic from the outside. Larger organizations use separate firewall devices to protect their network.


- <b>Types of Firewalls</b>
The network profiles help tailor the firewall’s behavior based on the network’s trust level and security requirements.

  - <ins>Domain Network</ins>:This is a network where the computer is connected to a domain of the company and is typically used in enterprise environments. This allows to apply settings for computers that are part of a corporate or organizational network, allowing for centralized management.
  - <ins>Private Network</ins>:This is a network, such as a home or small office network, where the one or more computers can be trusted. Here, a more relaxed security settings can be applied, allowing devices within the same network to communicate more freely.
  - <ins>Public Network</ins>:This is a network where the computer is connected in a public place, like a café or airport. This needs a restrictive settings to prevent unauthorized access and ensure maximum security in untrusted environments.


<h2>How Firewalls Work </h2>
A firewall works by monitoring all incoming and outgoing network traffic. The firewall decides whether to permit or deny the traffic based on a predefined set of rules.  Firewalls can monitor and filter traffic using several different methods. 

- <b>Packets</b> are small pieces of data that travel across a network. A firewall that uses packet filtering reviews each packet that tries to access a network or device. Any packets that match known threats or that have been explicitly denied are removed and all other packets are sent through to their destination.
- <b>Stateful inspection</b>, also known as dynamic filtering, monitors the state of active network connections.  It relies on patterns to analyze and monitor traffic for potential threats.
- <b>A proxy firewall</b> serves as a go-between for the requesting system and the internet. Information is first sent to the proxy service before it is forwarded to its destination.


<b><ins> Filters - Controlling Network Traffic</b></ins>

Firewalls can be configured to meet the specific need of an individual or organization. The Inbound and outbound rules in Windows Firewall control the traffic allowed into and out of your computer, respectively. Traffic can be approved or denied based on IP addresses, ports, domain names, and even specific words and phrases. These ensure that only authorized traffic is allowed while unauthorized or potentially harmful traffic is blocked.

  Before you configure your firewall, it is important to create a plan. In many cases it’s best to deny all traffic except what is allowed. Rules that are too strict can limit important user functionality. However, rules that are too loose can put your network at risk, so it’s usually easier to add approved access than it is to recover from a breach that happened because of loose firewall rules. The more rules there are, the longer the firewall takes to review the traffic, so you’ll want to try to keep a lean, but efficient set of rules.


  - <b>Inbound Rules</b>
Inbound rules control the incoming network traffic to your computer. These rules help protect your system from unauthorized access and attacks by specifying which types of incoming connections are allowed or blocked.


  - <b>Outbound Rules</b>
Outbound rules control the outgoing network traffic from your computer. These rules help manage what data leaves your computer and ensure that only authorized applications and services can send information.

<img src="https://www.online-tech-tips.com/wp-content/uploads/2012/07/advanced-firewall-settings.png" height="60%" width="50%" alt="Disk Sanitization Steps"/>

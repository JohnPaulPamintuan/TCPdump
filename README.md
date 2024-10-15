<h1>Capturing and Analyzing TCP Traffic with TCPdump</h1> 

<h2>Project Description:</h2>
In this project, we use TCPdump to capture TCP traffic from a network interface and analyze it to understand the flow of communication between hosts. We’ll examine TCP flags and connection behaviors, such as the TCP three-way handshake.<br/>

<h2>Tools Used:</h2>

- <b>TCPdump</b>: Command-line packet analyzer for capturing network traffic.
- <b>Wireshark (Optional)</b>: For more detailed inspection and visualization of the captured traffic (you may focus solely on TCPdump for the core project).

<h1>Step-by-Step Implementation</h1>

<h2><ins>1. Setting Up the Environment</ins></h2>

- Install TCPdump on your machine (Linux-based or virtual machine).
- Ensure that you have administrative privileges to capture network traffic.

  <img src="https://i.imgur.com/Q99f0YI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2><ins>2. Capturing TCP Traffic</ins></h2>

- Use TCPdump to capture only TCP traffic from a specified network interface (e.g., eth0). You can use filters to focus on traffic from a specific source or destination IP, or port.
   <img src="https://i.imgur.com/n4wsxXD.png" height="120%" width="85%" alt="Disk Sanitization Steps"/>

- Example command to capture all TCP traffic and save it to a file:
   <img src="https://i.imgur.com/1dxjZDH.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>

- <b>Other examples of Tcpdump Packet Filtering:</b>

	- host will filter visible traffic to show anything involving the designated host. Bi-directional.

       <img src="https://i.imgur.com/oJHHKxN.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>


  - src and dest are modifiers. We can use them to designate a source or destination host or port and Utilizing Source With Port as a Filter.

     <img src="https://i.imgur.com/RNkMYk3.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
     <img src="https://i.imgur.com/Q4cBh2I.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>

   -  proto will filter for a specific protocol type. (ether, TCP, UDP, and ICMP as examples).
   -  port is bi-directional. It will show any traffic with the specified port as the source or destination.

       <img src="https://i.imgur.com/BnS36fc.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
       <img src="https://i.imgur.com/thajDeo.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
       <img src="https://i.imgur.com/7jrsoKr.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
       
       

   - less and greater can be used to look for a packet or protocol option of a specific size.

     <img src="https://i.imgur.com/IKaTf8g.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
     <img src="https://i.imgur.com/HYcVD9Y.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
     
     

   - and && can be used to concatenate two different filters together. for example, src host AND port.
   - or allows for a match on either of two conditions. It does not have to meet both. It can be tricky.
   - not is a modifier saying anything but x. For example, not UDP.

     <img src="https://i.imgur.com/JcgsKpC.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
     <img src="https://i.imgur.com/m6fMmrg.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>
     <img src="https://i.imgur.com/WBrtF35.png" height="130%" width="80%" alt="Disk Sanitization Steps"/>

  
<h2><ins>3. Basic Analysis with TCPdump</ins></h2>

- After capturing the traffic, use TCPdump to analyze specific packets directly from the terminal.
- View the contents of the <b>.pcap</b> file:
  
   <img src="https://i.imgur.com/D5P15oy.png" height="120%" width="85%" alt="Disk Sanitization Steps"/>
- To filter for TCP packets with the SYN flag set (indicating new connection attempts):
   <img src="https://i.imgur.com/ixoWbwR.png" height="120%" width="85%" alt="Disk Sanitization Steps"/>
- To see all packets with the FIN flag (indicating connection terminations):
   <img src="https://i.imgur.com/yfg94fA.png" height="120%" width="85%" alt="Disk Sanitization Steps"/>

<h2><ins>4. Inspecting TCP Three-Way Handshake</ins></h2>

- Identify the TCP three-way handshake in the captured data by filtering for packets with the SYN, SYN-ACK, and ACK flags.
- The three-step process looks like:
  - SYN from the client to initiate a connection.
  - SYN-ACK from the server to acknowledge the request.
  - ACK from the client to establish the connection.
 
- Example filter to capture this sequence:

 <img src="https://i.imgur.com/jhwYuR9.png" height="120%" width="85%" alt="Disk Sanitization Steps"/>

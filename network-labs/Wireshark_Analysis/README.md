#### **Wireshark Traffic Analysis *(Cybersecurity Project)***





###### *Objective*

To capture and analyze network packets to identify suspicious or abnormal traffic behavior.





###### *Tools \& Environment*

\- Wireshark

\- Linux Ubuntu VM

\- Sample pcap files





###### *Steps Taken*

1\. Captured live network traffic on eth0.

2\. Applied filters for HTTP, DNS, and ICMP.

3\. Identified abnormal packets (e.g., repeated SYN requests).

4\. Analyzed possible reconnaissance or DoS patterns.





###### *Sample Filters*

http

dns

tcp.flags.syn==1 and tcp.flags.ack==0





###### *Findings*

\- Detected multiple SYN packets without ACK → Possible SYN flood attempt

\- DNS requests from unknown sources → Potential spoofing

\- Clear-text passwords in HTTP packets → Unsecured transmission





What I Know:

\- How to interpret packet flows

\- Basics of network forensics and packet filtering

\- Importance of encryption in preventing credential leaks


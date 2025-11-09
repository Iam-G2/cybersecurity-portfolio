# **VLAN Configuration Project**



* ###### ***Objective***

To segment a network using VLANs and improve performance, security, and traffic management.



* ###### ***Tools \& Environment***

\- Cisco Packet Tracer

\- Cisco 2960 Switches

\- Windows



* ###### ***Configuration Steps***

1\. Created VLANs (10, 20, 30) for different departments.

2\. Assigned ports to VLANs.

3\. Configured trunking between switches.

4\. Verified VLAN communication using ping tests.



###### **Sample Commands**

>enable

Switch> Config T

Switch(config)#hostname S1

S1(config)#vlan 10

S1(config-vlan)#name HR

S1(config-vlan)#exit

S1(config)#int g0/1-4

S1(config-if-range)#switchport mode access

S1(config-if-range)#switchport access vlan 10









VERIFICATION...

use *show vlan* brief and *ping* to confirm isolation between VLANs





What I Know:



* How VLANs segment networks logically
* How trunking works to carry multiple VLANs between Switches
* Troubleshooting VLAN connectivity issues




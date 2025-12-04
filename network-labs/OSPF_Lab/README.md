# OSPF Routing Lab



##### Objective

To configure dynamic routing using OSPF for IPv4 and IPv6 networks.



###### *Tools \& Environment*

\- Cisco Packet Tracer

\- Routers: 2911 Series



###### *Configuration Steps*

1\. Assigned IP addresses on router interfaces.

2\. Enabled OSPF and set router IDs.

3\. Advertised networks using wildcard masks.

4\. Verified routing tables and neighbor relationships.



###### *Sample Commands*

Router(config)# router ospf 1

Router(config-router)# router-id 1.1.1.1

Router(config-router)# network 192.168.1.0 0.0.0.255 area 0

Router(config-router)# ipv6 router ospf 10

Router(config-rtr)# router-id 2.2.2.2

Router(config-rtr)# interface g0/0

Router(config-if)# ipv6 ospf 10 area 0



###### *Verification*

    \- Checked adjacency using show ip ospf neighbor

    \- Verified routes with show ip route ospf



What I Know:

\- OSPF basics and LSA types

\- The difference between single and multi-area OSPF

\- Configuring OSPF for IPv6






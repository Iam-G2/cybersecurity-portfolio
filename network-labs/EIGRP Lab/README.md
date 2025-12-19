# EIGRP Routing Lab (CCNA / CCNP Aligned)
# Overview

This lab demonstrates the configuration and verification of Enhanced Interior Gateway Routing Protocol (EIGRP) in a multi-router IPv4 environment.
The objective is to validate neighbor adjacency, route exchange, and metric-based path selection using Cisco best practices aligned with CCNA and CCNP Enterprise standards.

# Objective

Configure EIGRP using a common autonomous system (AS)

Establish neighbor relationships between routers

Advertise and learn IPv4 networks dynamically

Verify routing behavior and end-to-end connectivity

# Tools & Environment

Cisco Packet Tracer

Cisco 2911 Series Routers

Routing Protocol: EIGRP (IPv4)

Autonomous System: AS 100

# Lab Topology
[ PC-A ] ---- R1 ---- R2 ---- R3 ---- [ PC-B ]

Topology Description

Three routers connected in a linear topology

Each router services a unique LAN subnet

Inter-router links use Gigabit Ethernet or Serial interfaces

End devices validate full end-to-end communication

Example IP Addressing Scheme
Device	Interface	IP Address
R1	G0/0	192.168.1.1/24
R1	G0/1	10.0.12.1/24
R2	G0/0	10.0.12.2/24
R2	G0/1	10.0.23.1/24
R3	G0/0	10.0.23.2/24
R3	G0/1	192.168.3.1/24
# Configuration Steps

Assign IPv4 addresses to all router interfaces

Enable EIGRP using a shared AS number

Advertise all directly connected networks

Disable automatic summarization

Verify EIGRP neighbor adjacency

Confirm learned routes and connectivity

# Sample Configuration Commands
Router(config)# router eigrp 100
Router(config-router)# network 192.168.1.0 0.0.0.255
Router(config-router)# network 10.0.12.0 0.0.0.255
Router(config-router)# no auto-summary

Router(config)# interface g0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown

# Verification & Validation
show ip eigrp neighbors


✔ Confirms neighbor adjacency and hold timers

show ip route eigrp


✔ Verifies EIGRP-learned routes in the routing table

show ip eigrp topology


✔ Displays successor and feasible successor routes

ping
traceroute


✔ Validates end-to-end connectivity

# What This Lab Demonstrates
CCNA-Level Skills

Dynamic routing fundamentals

EIGRP neighbor discovery and routing table validation

Basic troubleshooting and verification commands

CCNP-Level Understanding

DUAL algorithm and loop-free path selection

Successor vs Feasible Successor concepts

Metric calculation (Bandwidth & Delay)

Impact of auto-summary in modern networks

Common EIGRP adjacency failure causes:

AS mismatch

K-value mismatch

Passive interfaces

# Key Takeaways

EIGRP provides fast convergence and efficient route selection

Proper verification ensures stable and loop-free routing

Understanding EIGRP internals is essential for enterprise networks

📂 Portfolio Note

This lab highlights hands-on enterprise routing experience and aligns with real-world scenarios covered in CCNA and CCNP Enterprise certifications.

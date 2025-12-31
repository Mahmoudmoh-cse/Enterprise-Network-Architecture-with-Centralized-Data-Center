# Enterprise-Network-Architecture-with-Centralized-Data-Center
A data center–centric enterprise network designed to support corporate services and research environments using real-world design principles. Network Design Data Center as the central backbone and service core Independent domains (Corporate &amp; Labs) connected via BGP Spine–leaf topology for high availability and low latency
# Routing Protocols
BGP: Inter-domain connectivity
EIGRP: Corporate Campus
OSPF: Research & Cyber Labs
RIP: Internal Data Center routing
# Core Data Center Architecture
Spine–Leaf Topology:
Two-tier design ensures scalability and efficient east–west traffic, ideal for AI and HPC workloads.
High Availability:
Redundant paths between Spine and Leaf switches eliminate bottlenecks and improve reliability.
Segmentation:
Room 1 (Standard): Web & application servers for DevOps and cloud testing
Room 2 (High-Performance): HPC clusters, GPU farms, and AI research servers
Routing & Connectivity
RIP: Simple internal routing inside the Data Center
BGP: Policy-based routing to Corporate Campus and Research Labs
Data Center Subnetting (11.0.0.0/8)
Subnetting Strategy: Borrowed 4 bits to support multiple networks
Subnet Mask: /12 (255.240.0.0)
Examples:
11.0.0.0 – 11.15.255.255 → General services
11.80.0.0 – 11.95.255.255 → High-compute clusters
11.112.0.0 – 11.127.255.255 → HPC server segments

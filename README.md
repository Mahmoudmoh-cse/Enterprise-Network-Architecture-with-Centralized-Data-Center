# Enterprise Network Architecture with Centralized Data Center

A data-center-centric enterprise network designed around real-world routing, segmentation, redundancy, and scalability concepts.

## Network Design

- Centralized data center as the service backbone
- Independent Corporate and Research/Lab domains
- BGP for inter-domain connectivity
- Spine-leaf topology for high availability and low-latency east-west traffic

## Routing Protocols

- **BGP:** Inter-domain connectivity
- **EIGRP:** Corporate campus
- **OSPF:** Research and cyber labs
- **RIP:** Internal data-center routing

## Data Center Architecture

### Spine-Leaf

A two-tier topology designed to improve scalability and reduce bottlenecks for workloads such as AI and HPC.

### High Availability

Redundant paths between spine and leaf switches provide alternate routes and reduce single points of failure.

### Segmentation

- **Room 1:** Web and application servers for general services, DevOps, and cloud testing
- **Room 2:** HPC clusters, GPU farms, and AI research servers

## Addressing

Data-center address space: `11.0.0.0/8`

Example /12 segments:

- `11.0.0.0 – 11.15.255.255` — general services
- `11.80.0.0 – 11.95.255.255` — high-compute clusters
- `11.112.0.0 – 11.127.255.255` — HPC server segments

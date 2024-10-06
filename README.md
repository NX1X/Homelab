# My Home Lab

## Overview

This repository contains documentation and configuration files for my personal home lab environment. The lab is designed to provide a robust platform for learning, experimentation, and hosting various services.

**Note: This project is still in progress. More details will be coming soon.**

## Infrastructure

# 🏠 Homelab Infrastructure

| Category | Description | Tool |
|----------|-------------|------|
| **On-premise** | 8 physical Dell/Lenovo servers (second-hand) | [Proxmox](https://www.proxmox.com/en/) (7-node cluster) |
| **Firewall** | Network security and traffic management | [pfSense](https://www.pfsense.org/) |
| **Container Orchestration** | Kubernetes cluster for microservices | [Rancher](https://www.rancher.com/) |
| **Security** | XDR & SIEM for monitoring and threat detection | [Wazuh](https://wazuh.com/) |
| **Storage** | Network-attached storage | [TrueNAS Scale](https://www.truenas.com/truenas-scale/) |
| **Networking** | High-performance switch (second-hand) | [Cisco Catalyst 4948E-F](https://www.cisco.com/c/en/us/products/switches/catalyst-4948e-ethernet-switch/index.html) |

> **Notes**: 
> - One physical server is dedicated as the firewall, while the other 7 form the Proxmox cluster.
> - All servers and the Cisco switch were purchased second-hand, demonstrating cost-effective infrastructure building.

## Structure

The repository is organized as follows:

```
├── proxmox/
├── firewall/
├── kubernetes/
├── xdr-siem/
├── storage/
├── network/
└── docs/
```

Each directory contains relevant configuration files, scripts, and documentation for the respective component.

## Getting Started

(Instructions on how to set up or use the lab will be added here)

## Future Plans

(Outline of planned improvements or additions to the lab)

## Contributing

As this is a personal project, contributions are not currently being accepted. However, feel free to fork the repository and adapt it for your own use.

## License

MIT License
Copyright (c) [2024] [NX1X]

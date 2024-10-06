# My Home Lab

## Overview

This repository contains documentation and configuration files for my personal home lab environment. The lab is designed to provide a robust platform for learning, experimentation, and hosting various services.

**Note: This project is still in progress. More details will be coming soon.**

## Infrastructure

The home lab consists of the following key components:

1. **8 Physical Servers**: Running Proxmox for virtualization and container management. Tool: **[Proxmox](https://www.proxmox.com/en/)**
2. **Firewall**: Ensuring network security and managing traffic. Tool: **[pfSense](https://www.pfsense.org/)**
3. 4. **Kubernetes Cluster**: For container orchestration and microservices deployment. Tool: **[Rancher](https://www.rancher.com/)**
4. **XDR & SIEM**: For comprehensive security monitoring and threat detection. Tool: **[Wazuh](https://wazuh.com/)**
5. **Storage**: Providing network-attached storage capabilities. Tool: **[TrueNAS Scale](https://www.truenas.com/truenas-scale/)**
6. **Cisco Managed Switch**: 4948EF model for high-performance networking. Model: **[Cisco Catalyst 4948E-F](https://www.cisco.com/c/en/us/products/switches/catalyst-4948e-ethernet-switch/index.html)**

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

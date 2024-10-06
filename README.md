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
6. **Cisco Managed Switch**: 4948EF model for high-performance networking. Model: **[Cisco Catalyst 4948E-F](https://www.cisco.com/c/en/us/products/collateral/switches/catalyst-4948e-ethernet-switch/data_sheet_c78-598933.html)**

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
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

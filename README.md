# Enterprise Network Design and Configuration Using EVE-NG

## Project Overview

Hi everyone! This project was originally part of my apprenticeship academic work. After completing and revising the concepts, I wanted to evaluate my practical networking knowledge and understand how confidently I could configure a complete network independently.

To achieve this, I designed and implemented an enterprise network project entirely from scratch using **EVE-NG**. I analyzed the requirements, designed the complete network topology independently, planned the IP addressing scheme, and configured the network devices step by step.

Although EVE-NG did not support wireless radio functionality in my lab environment, I completed the project by using floor routers to represent the intended connectivity.

## Technologies and Configurations Implemented

- **Network Topology Design:** Designed the complete topology independently based on the project requirements.
- **IP Addressing:** Planned and assigned IP addresses to network devices and interfaces.
- **VLANs and Trunking:** Created VLANs, configured trunk links, and assigned switch access ports to the appropriate VLANs.
- **Inter-VLAN Routing:** Enabled communication between different VLANs.
- **DHCP:** Configured centralized DHCP services for dynamic IP address allocation.
- **OSPF:** Implemented OSPF dynamic routing to enable route exchange between network devices.
- **Port Security:** Configured switch port security to control device access.
- **SSH:** Configured secure remote management of network devices.
- **ACLs:** Implemented Access Control Lists to control traffic and manage access permissions.
- **NAT/PAT:** Configured Port Address Translation to provide internet connectivity for internal networks.

## Key Learnings and Troubleshooting

During the implementation, I encountered several configuration challenges. Troubleshooting and resolving them helped me understand the behavior of network protocols and configurations more deeply.

### 1. OSPF Default Route Advertisement

I learned the importance of the `default-information originate` command in OSPF when advertising a default route to other OSPF routers. This helped me understand how internal networks can learn a route toward an external network through the appropriate gateway.

### 2. PAT and Cisco Express Forwarding (CEF)

While troubleshooting PAT, I encountered an issue related to my NAT/PAT configuration and the lab environment. I investigated the network configuration and disabled Cisco Express Forwarding (CEF) using `no ip cef` during troubleshooting. This helped me explore the relationship between packet forwarding and NAT/PAT behavior in the lab.

### 3. ACL Sequence Numbers and SSH Access

I encountered an issue with SSH access due to the sequence and ordering of ACL entries. By reviewing and adjusting the ACL sequence, I learned how rule ordering and traffic-matching conditions affect whether management traffic is permitted or denied.

I also learned the importance of understanding where traffic originates, how it travels through the network, and where an ACL should be applied.

### 4. ACL Direction: Inbound and Outbound

I gained additional practical knowledge of ACL placement and direction, including the differences between inbound and outbound filtering. I learned to consider the traffic source, destination, direction, and interface when determining the correct ACL configuration.

### 5. Adapting the Topology to EVE-NG Limitations

Since wireless radio functionality was unavailable in my EVE-NG environment, I adapted the topology by using floor routers to represent the required network connectivity. This allowed me to continue implementing and testing the other networking requirements despite the lab limitation.

## Overall Learning Outcomes

This project helped me move beyond theoretical networking concepts and apply them in a practical environment. Designing the topology independently, configuring the devices, troubleshooting connectivity issues, and resolving routing, NAT/PAT, ACL, and SSH problems improved my understanding of enterprise networking.

Most importantly, I learned that successful network implementation requires more than entering configuration commands. It requires understanding the requirements, planning the topology, analyzing traffic flow, identifying configuration mistakes, and validating the results.

**This project represents my hands-on learning journey in enterprise network design, implementation, and troubleshooting using EVE-NG.**

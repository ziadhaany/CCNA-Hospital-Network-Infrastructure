Hospital Network Infrastructure
A secure, highly available hospital network designed and simulated in Cisco Packet Tracer,
connecting departments such as Emergency, Administration, Clinics, and Laboratories.

1. VLANs & Inter-VLAN Routing
- Created 4 VLANs (10, 20, 40, 50) to separate hospital departments.
- Configured access ports and 802.1Q trunks between floor switches.
- Set up inter-VLAN routing using SVIs on the multilayer switches.

2. Routing
- Configured OSPF (Area 0) across the core, distribution, and edge devices.
- Assigned IP addressing for VLANs and the point-to-point links.

3.High Availability
- Configured HSRP (priority 150 + preempt) with virtual gateway IPs for each VLAN.
- Built LACP EtherChannel bundles between switches for redundancy and bandwidth.
- Set STP root primary/secondary using Rapid-PVST+.

4.Network Services
- Configured a central DHCP server with `ip helper-address` relay.
- Set up DNS, HTTP, and FTP servers in a dedicated server subnet.
- Added a wireless access point for mobile devices.

5. NAT
- Configured PAT on the edge router so internal hosts share one public IP.

6. Security
- Enabled SSH v2, encrypted passwords, login banner, and login block-for.
- Applied port security (sticky MAC), PortFast, and BPDU Guard on access ports.
- Shut down unused ports.
- Created an extended ACL to protect the server subnet.
- Added an anti-spoofing ACL on the edge routers.

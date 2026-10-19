Packet Tracer Troubleshooting Lab — Nothing Pings
Overview
This lab investigates and fixes connectivity failures in a small Cisco Packet Tracer network. Troubleshooting focused on router interfaces, VLAN membership, trunk configuration, and end-device IP settings.

Issues Identified and Fixes
1. Router R1 Interface
Issue: GigabitEthernet0/1 was administratively down.

Fix: Enabled the interface with no shutdown.

2. Switch VLAN Assignment
Issue: FastEthernet0/2 was assigned to VLAN 10 instead of VLAN 20.

Fix: Assigned Fa0/2 to VLAN 20.

3. Trunk Allowed VLANs
Issue: The trunk on GigabitEthernet0/1 allowed only VLAN 10.

Fix: Configured the trunk to allow VLANs 10 and 20.

4. PC1 Default Gateway
Issue: PC1 used the incorrect default gateway 192.168.10.254.

Fix: Changed the default gateway to 192.168.10.1.

5. PC2 IP Address
Issue: PC2 was configured with 192.168.2.10, outside the intended Admin subnet.

Fix: Changed the IP address to 192.168.20.10 with subnet mask 255.255.255.0.

Troubleshooting and Verification
The fault log records the use of:

tracert to investigate the path between devices.

show ip interface brief to inspect router interface status and addressing.

show vlan brief to check switch VLAN membership.

show interfaces trunk to inspect trunk status and allowed VLANs.

ping to test connectivity.

Conclusion
The recorded faults involved a disabled router interface, an incorrect switch VLAN assignment, a trunk VLAN restriction, and incorrect end-device IP settings. The lab report states that after these corrections, communication between the Sales VLAN, Admin VLAN, and server network was restored.

Files
Lab_fixed_Emmanuel_Amoasi.pkt — Cisco Packet Tracer lab file.

Packet_Tracer_Troubleshooting_Fault_Log.pdf — troubleshooting notes and fault log.

VLAN and Addressing Summary
Network component	Configuration noted in the lab
Sales VLAN	VLAN 10
Admin VLAN	VLAN 20
R1 VLAN 10 gateway	192.168.10.1
R1 VLAN 20 gateway	192.168.20.1
PC2 address after correction	192.168.20.10/24
PC1 gateway after correction	192.168.10.1
How to Open
Open Cisco Packet Tracer.

Select File → Open.

Open Lab_fixed_Emmanuel_Amoasi.pkt.

Review the topology and test connectivity with ping as appropriate.

Project: Packet Tracer Troubleshooting Lab — Nothing Pings
Author: Emmanuel Amoasi


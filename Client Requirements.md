1.Client Requirements
Mmala Courier Services, based in Rustenburg, requires a reliable and secure network to support daily courier operations across multiple departments. The design must ensure efficient communication while keeping sensitive resources separated.
•	Departmental segmentation: VLANs must isolate traffic between courier operations, administration, and support teams.
•	Printer sharing: Printers must be accessible across departments, regardless of VLAN boundaries.
•	File sharing: File access must remain restricted within each department to protect confidential information.
•	CCTV integration: Four cameras must be added on a dedicated VLAN to prevent video traffic from interfering with courier operations.
•	IP addressing: The block 172.30.22.0/23 will be used to allocate IP addresses across all VLANs
•	Inter VLAN routing: A Layer 3 switch with SVI will be used to allow controlled communication between VLANs.

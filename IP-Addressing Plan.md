# IP Addressing Plan – Mmala Courier Services (CLI-045)

Assigned block: **172.30.22.0/23** (172.30.22.0 – 172.30.23.255, 512 addresses)

## VLAN subnets

| VLAN | Name | Subnet | Mask | Usable range | Broadcast | Gateway (SVI on CORE-L3) |
|---|---|---|---|---|---|---|
| 10 | COURIER_OPS | 172.30.22.0/25 | 255.255.255.128 | .1 – .126 | 172.30.22.127 | 172.30.22.1 |
| 20 | ADMIN | 172.30.22.128/26 | 255.255.255.192 | .129 – .190 | 172.30.22.191 | 172.30.22.129 |
| 30 | SUPPORT | 172.30.22.192/26 | 255.255.255.192 | .193 – .254 | 172.30.22.255 | 172.30.22.193 |
| 40 | PRINTER | 172.30.23.0/27 | 255.255.255.224 | .1 – .30 | 172.30.23.31 | 172.30.23.1 |
| 50 | CCTV | 172.30.23.32/28 | 255.255.255.240 | .33 – .46 | 172.30.23.47 | 172.30.23.33 |

Unallocated (reserved for growth): 172.30.23.48 – 172.30.23.255.

## End devices

| Device | VLAN | IP address | Mask | Gateway |
|---|---|---|---|---|
| PC-OPS1, PC-OPS2 | 10 | 172.30.22.10, .11 | 255.255.255.128 | 172.30.22.1 |
| PC-ADMIN1, PC-ADMIN2 | 20 | 172.30.22.130, .131 | 255.255.255.192 | 172.30.22.129 |
| PC-SUP1, PC-SUP2 | 30 | 172.30.22.194, .195 | 255.255.255.192 | 172.30.22.193 |
| PRN-01 (printer) | 40 | 172.30.23.10 | 255.255.255.224 | 172.30.23.1 |
| CCTV-01 to CCTV-04 | 50 | 172.30.23.34 – .37 | 255.255.255.240 | 172.30.23.33 |

## Correction to Milestone 1

The Milestone 1 plan listed the Printer VLAN as 172.30.22.256/27 and the CCTV VLAN as 172.30.22.288/28. Those addresses are invalid because an octet cannot exceed 255. Since the /23 continues into 172.30.23.0, the two subnets were moved to 172.30.23.0/27 and 172.30.23.32/28. The first three subnets were already correct.

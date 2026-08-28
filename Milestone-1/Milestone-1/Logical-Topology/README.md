# Logical Topology

The proposed logical topology uses four VLANs and router-on-a-stick inter-VLAN routing.

| VLAN | Name |
|---:|---|
| 10 | ENGINEERING |
| 20 | ADMINISTRATION |
| 30 | SHARED-PRINTER |
| 40 | SERVERS |

VLANs 10 and 20 will use DHCP.

VLANs 30 and 40 will contain statically addressed shared resources.

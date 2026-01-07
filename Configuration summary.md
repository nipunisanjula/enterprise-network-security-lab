: ![Image Alt](https://github.com/nipunisanjula/enterprise-network-security-lab/blob/4f49fbfbad45cf0306ee903c09145613388bc759/Image/1.1.png)
# **Network device specifications and virtual images used in EVE-NG lab**

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| Device | Real OS | Node name | RAM | CPU |
| Router | IOSv | Cisco vIOS router<br><br>(Lightweight than Cisco CSR1000v which requires 4GB RAM per instance) | 1GB | 1 core |
| Layer 2 Switch | vIOSL2 | Cisco vLOS switch | 768 MB | 1 core |
| Firewall | FortiGate | Fortinet FGT.v6 | 2GB | 1 core |
| Servers | Ubuntu desktop | Linux | 1GB | 1 core |
| Virtual PC | vPCS | vPCs | \-  | \-  |
| PC  | Windows 10 | Windows | 2 GB | 1 core |

# **Configuration details of switches**

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| device | interfaces | Port(Trunk/Access) | Vlan | port security and port status | EtherChannel |
| Switch_1 | Gi0/0 | Trunk |     | Sticky -up | Port channel 3 |
| Gi0/1 |
| Gi0/2 | Access | Vlan 10 | Sticky -up |     |
| Gi0/3 |
| Gi1/0 | Access | Vlan 20 | Sticky -up |     |
| Gi1/1 | Sticky -up |     |
| Gi1/2 | Sticky- down |     |
| Gi1/3 | Sticky- down |     |
| Gi2/0 | Access | Vlan 30 | Sticky -up |     |
| Gi2/1 | Sticky- down |     |
| Gi2/2 | Sticky- down |     |
| Gi2/3 | Sticky- down |     |
| Switch_2 | Gi0/0 | Trunk |     | Sticky -up | Port channel 2 |
| Gi0/1 |
| Gi0/2 | Access | Vlan 10 | Sticky -up |     |
| Gi0/3 | Access | Vlan 20 | Sticky -up |     |
| Gi1/0 | Access | Vlan 30 | Sticky -up |     |
| Gi1/1 | Access | Vlan 70 | Sticky- down |     |
| Gi1/2 |
| Gi1/3 |
| DMZ_Switch | Gi0/0 | Trunk |     | Sticky -up |     |
| Gi0/1 | Access | Vlan 50 | Sticky -up |     |
| Gi0/2 |
| Gi0/3 |
| L3_Switch_2 | Gi0/0 | Trunk |     | Sticky -up | Port channel 1 |
| Gi0/1 |
| Gi0/2 | Trunk |     | Sticky -up | Port channel 2 |
| Gi0/3 |
| Gi1/0 | Trunk |     | Sticky -up | Port channel 3 |
| Gi1/1 |
| Gi1/2 | Access | Vlan 20 | Sticky -up |     |
| Gi1/3 | Access | Vlan 30 | Sticky -up |     |
| L3_Switch_1 | Gi0/0 | Trunk |     | Sticky -up |     |
| Gi0/1 | Trunk |     | Sticky -up | Port channel 1 |
| Gi0/2 |
| Gi0/3 | Access | Vlan 80 | Sticky -up |     |
| Gi1/0 |
| Gi1/1 |
| Gi1/2 | Access | Vlan 70 | Sticky -down |     |
| Gi1/3 |
| Branch_Switch | Gi0/0 | Trunk |     | Sticky -up |     |
| Gi0/1 | Access | DHCP | Sticky -up |     |
| Gi0/2 |
| Gi0/3 |

# **Configuration details of routers**

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| device name | password | interface | Ip address |     |     |
| Ip address | sub net | Wildcard mask |
| ISP_NAT | console, aux, telnet - int123<br><br>Enable secret- int456 | Gi0/0 | 192.168.100.1/24 | 255.255.255.0 | 0.0.0.255 |
| Gi0/2 | 192.168.200.1/24 | 255.255.255.0 | 0.0.0.255 |
| ISP_1 | console, aux, telnet, enable secret - isp123 | Gi0/0 | 40.1.1.2 /26 | 255.255.255.192 | 0.0.0.63 |
| Gi0/1 | 20.1.1.1 /24 | 255.255.255.0 | 0.0.0.255 |
| Gi0/2 | 192.168.100.2/24 | 255.255.255.0 | 0.0.0.255 |
| ISP_2 | console, aux, telnet, enable secret - isp456 | Gi0/0 | 40.1.1.66 /26 | 255.255.255.192 | 0.0.0.63 |
| Gi0/1 | 30.1.1.1 /24 | 255.255.255.0 | 0.0.0.255 |
| Gi0/2 | 192.168.200.2/24 | 255.255.255.0 | 0.0.0.255 |
| Router_Office | console, aux- Cs@1!2Ax<br><br>telnet- Tl@1!2vbn<br><br>enable secret- Es@1!2vbn | Gi0/0 | 192.168.1.1 /24 | 255.255.255.0 | 0.0.0.255 |
| Gi0/1 | 20.1.1.2 /24 | 255.255.255.0 | 0.0.0.255 |
| Gi0/2 | 30.1.1.2 /24 | 255.255.255.0 | 0.0.0.255 |
| Router_Branch | console, aux, telnet-Rb123<br><br>Enable secret- Rb456 | Gi0/0 | 40.1.1.1 /26 | 255.255.255.192 | 0.0.0.63 |
| Gi0/1 | 40.1.1.65 /26 | 255.255.255.192 | 0.0.0.63 |
| Gi0/2 | 192.168.40.1/24 | 255.255.255.0 | 0.0.0.255 |

# **Configuration details of Office_Firewall**

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| pasword | interface | ip address | role | Sub Interfaces | default gatway |
| username: admin<br><br>password: 123 | port1 | 192.168.3.1/24 | lan-ping,http,https,ssh,fgfm | vlan10 | 192.168.10.1/24 |
| vlan20 | 192.168.20.1/24 |
| vlan30 | 192.168.30.1/24 |
| vlan70 | 192.168.70.1/24 |
| vlan80 | 192.168.80.1/24 |
| port2 | 192.168.1.2/24 | wan-ping,https |     | 192.168.1.1/24 |
| port3 | 192.168.2.1/24 | dmz-ping,http,https | vlan50 | 192.168.50.1/24 |

# **Configuration details of end devices**

|     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
|     | VPC/Linux/Windows | Interface | Device name | ip address | VLAN | default gatway |
| Switch_1 | VPC | Gi 0/2 | IT_1 | 192.168.10.2 | VLAN 10 | 192.168.10.1 |
| Windows 10 | Gi 0/3 | IT_2<br><br>(monitoring) | 192.168.10.3 | VLAN 10 | 192.168.10.1 |
| VPC | Gi 1/0 | HR_1 | 192.168.20.2 | VLAN 20 | 192.168.20.1 |
| VPC | Gi 1/1 | HR_2 | 192.168.20.3 | VLAN 10 | 192.168.20.1 |
| VPC | Gi 2/0 | Sales_1 | 192.168.30.2 | VLAN 30 | 192.168.30.1 |
| Switch_2 | VPC | Gi 0/2 | IT_3 | 192.168.10.4 | VLAN 10 | 192.168.10.1 |
| VPC | Gi 0/3 | HR_3 | 192.168.20.4 | VLAN 10 | 192.168.20.1 |
| VPC | Gi 1/0 | Sales_2 | 192.168.30.3 | VLAN 30 | 192.168.30.1 |
| L3_Switch_2 | VPC | Gi 1/2 | HR_4 | 192.168.20.5 | VLAN 10 | 192.168.20.1 |
| VPC | Gi 1/3 | Sales_3 | 192.168.30.4 | VLAN 30 | 192.168.30.1 |
| L3_Switch_1 | Linux Server | Gi 0/3 | AAA Server | 192.168.80.12 | VLAN 80 | 192.168.80.1 |
| Linux Server | Gi 1/0 | Cacti Server | 192.168.80.13 | VLAN 80 | 192.168.80.1 |
| Linux | Gi 1/1 | Linux16 | 192.168.80.14 | VLAN 80 | 192.168.80.1 |
| DMZ_Switch | Linux Server | Gi 0/1 | Proxy Server | 192.168.50.2 | VLAN 50 | 192.168.50.1 |
| Linux Server | Gi 0/2 | FTP Server | 192.168.50.3 | VLAN 50 | 192.168.50.1 |
| Branch_Switch | Linux | Gi 0/1 | Branch_PC_1 | DHCP |     | 192.168.40.1 |
| Windows 10 | Gi 0/2 | Branch_PC_2 | DHCP |     | 192.168.40.1 |

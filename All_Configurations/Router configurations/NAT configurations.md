# **Network Address Translation (NAT) configurations on ISP_NAT**

ISP_NAT(config)# ip nat pool WAN 192.168.174.139 192.168.174.140 prefix-length 24

**Create an Access List:**

ISP_NAT(config)#ip access-list standard WANacl

ISP_NAT(config-std-nacl)#permit 192.168.100.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.200.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.10.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.20.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.30.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.40.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.50.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.70.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.80.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.2.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.3.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 192.168.1.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 20.1.1.0 0.0.0.255

ISP_NAT(config-std-nacl)#permit 30.1.1.0 0.0.0.25

ISP_NAT(config-std-nacl)#permit 40.1.1.0 0.0.0.63

ISP_NAT(config-std-nacl)#permit 40.1.1.64 0.0.0.63

ISP_NAT(config-std-nacl)#exit

**Link Access List to Pool:**

ISP_NAT(config)#ip nat inside source list WANacl pool WAN overload

**Apply:**

ISP_NAT(config)#int gi0/1

ISP_NAT(config-if)#ip nat outside

ISP_NAT(config-if)#exit

ISP_NAT(config)#int gi0/0

ISP_NAT(config-if)#ip nat inside

ISP_NAT(config-if)#exit

ISP_NAT(config)#int gi0/2

ISP_NAT(config-if)#ip nat inside

ISP_NAT(config-if)#exit

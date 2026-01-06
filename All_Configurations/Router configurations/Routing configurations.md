Dynamic routing configurations on ISP_NAT

ISP_NAT(config)#int gi 0/2

ISP_NAT(config-if)#ip ospf cost 5

ISP_NAT(config-if)#exit

ISP_NAT(config)#router ospf 1

ISP_NAT(config-router)# router-id 7.7.7.7

ISP_NAT(config-router)#network 192.168.100.0 0.0.0.255 area 0

ISP_NAT(config-router)#network 192.168.200.0 0.0.0.255 area 0

Static and dynamic routing configurations on ISP_1

ISP_1(config)# router ospf 1

ISP_1(config-router)# router-id 6.6.6.6

ISP_1(config-router)#network 192.168.100.0 0.0.0.255 area 0

ISP_1(config-router)#network 20.1.1.0 0.0.0.255 area 0

ISP_1(config-router)#network 40.1.1.0 0.0.0.63 area 0

ISP_1(config)#ip route 0.0.0.0 0.0.0.0 192.168.100.1

ISP_1(config)#ip name-server 8.8.8.8

Static and dynamic routing configurations on Router_Office

Office(config)#int gi 0/2

Office(config-if)#ip ospf cost 5

Office(config-if)#exit

Office(config)#router ospf 1

Office(config-router)# router-id 1.1.1.1

Office(config-router)#network 192.168.1.0 0.0.0.255 area 0

Office(config-router)#network 20.2.2.0 0.0.0.255 area 0

Office(config-router)#network 30.1.1.0 0.0.0.255 area 0

Office(config)#ip route 0.0.0.0 0.0.0.0 192.168.100.1

Office(config)#ip route 0.0.0.0 0.0.0.0 192.168.200.1 20

Office (config)#ip name-server 8.8.8.8

Static and dynamic routing configurations on ISP_2

ISP_2 (config)#int range gi 0/0-2

ISP_2 (config-if)#ip ospf cost 5

ISP_2 (config-if)#exit

ISP_2(config)# router ospf 1

ISP_2(config-router)# router-id 5.5.5.5

ISP_2(config-router)#network 192.168.200.0 0.0.0.255 area 0

ISP_2(config-router)#network 30.1.1.0 0.0.0.255 area 0

ISP_2(config-router)#network 40.1.1.64 0.0.0.63 area 0

ISP_2(config)#ip route 0.0.0.0 0.0.0.0 192.168.200.1

ISP_2(config)#ip name-server 8.8.8.8

Static and dynamic routing configurations on ROUTER_BRANCH

Router_Branch (config)#int gi 0/1

Router_Branch (config-if)#ip ospf cost 5

Router_Branch (config-if)#exit

Router_Branch (config)#router ospf 1

Router_Branch (config-router)# router-id 4.4.4.4

Router_Branch (config-router)#network 192.168.40.0 0.0.0.255 area 0

Router_Branch (config-router)#network 40.1.1.0 0.0.0.63 area 0

Router_Branch (config-router)#network 40.1.1.64 0.0.0.63 area 0

Router_Branch (config)#ip route 0.0.0.0 0.0.0.0 192.168.100.1

Router_Branch (config)#ip route 0.0.0.0 0.0.0.0 192.168.200.1 20

Router_Branch(config)#ip name-server 8.8.8.8
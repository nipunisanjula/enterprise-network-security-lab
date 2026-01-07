# **Dynamic routing with OSPF on FortiGate**

Office_Firewall # config router ospf

Office_Firewall (ospf) # set router-id 2.2.2.2

Office_Firewall (ospf) # config area

Office_Firewall (area) # edit 0.0.0.0

Office_Firewall (0.0.0.0) # next

Office_Firewall (area) # end

Office_Firewall (ospf) # config network

Office_Firewall (network) # edit 1

Office_Firewall (1) # set prefix 192.168.1.0 255.255.255.0

Office_Firewall (1) # set area 0.0.0.0

Office_Firewall (1) # next

Office_Firewall (network) # edit 2

Office_Firewall (2) # set prefix 192.168.2.0 255.255.255.0

Office_Firewall (2) # set area 0.0.0.0

Office_Firewall (2) # next

Office_Firewall (network) # edit 3

Office_Firewall (3) # set prefix 192.168.3.0 255.255.255.0

Office_Firewall (3) # set area 0.0.0.0

Office_Firewall (3) # next

Office_Firewall (network) # edit 10

Office_Firewall (10) # set prefix 192.168.10.0 255.255.255.0

Office_Firewall (10) # set area 0.0.0.0

Office_Firewall (10) # next

Office_Firewall (network) # edit 20

Office_Firewall (20) # set prefix 192.168.20.0 255.255.255.0

Office_Firewall (20) # set area 0.0.0.0

Office_Firewall (20) # next

Office_Firewall (network) # edit 30

Office_Firewall (30) # set prefix 192.168.30.0 255.255.255.0

Office_Firewall (30) # set area 0.0.0.0

Office_Firewall (30) # next

Office_Firewall (network) # edit 50

Office_Firewall (50) # set prefix 192.168.50.0 255.255.255.0

Office_Firewall (50) # set area 0.0.0.0

Office_Firewall (50) # next

Office_Firewall (network) # edit 70

Office_Firewall (70) # set prefix 192.168.70.0 255.255.255.0

Office_Firewall (70) # set area 0.0.0.0

Office_Firewall (70) # next

Office_Firewall (network) # edit 80

Office_Firewall (80) # set prefix 192.168.80.0 255.255.255.0

Office_Firewall (80) # set area 0.0.0.0

Office_Firewall (80) # next

Office_Firewall (network) # end

Office_Firewall (ospf) # config ospf-interface

Office_Firewall (ospf-interface) # edit FGT_to_Router

Office_Firewall (FGT_to_Router) # set interface port2

Office_Firewall (FGT_to_Router) # next

Office_Firewall (ospf-interface) # edit 10_passive

Office_Firewall (10_passive) # set interface vlan10

Office_Firewall (10_passive) # next

Office_Firewall (ospf-interface) # edit 20_passive

Office_Firewall (20_passive) # set interface vlan20

Office_Firewall (20_passive) # next

Office_Firewall (ospf-interface) # edit 30_passive

Office_Firewall (30_passive) # set interface vlan30

Office_Firewall (30_passive) # next

Office_Firewall (ospf-interface) # edit 50_passive

Office_Firewall (50_passive) # set interface vlan50

Office_Firewall (50_passive) # next

Office_Firewall (ospf-interface) # edit 70_passive

Office_Firewall (70_passive) # set interface vlan70

Office_Firewall (70_passive) # next

Office_Firewall (ospf-interface) # edit 80_pasive

Office_Firewall (80_pasive) # set interface vlan80

Office_Firewall (80_pasive) # next

Office_Firewall (ospf-interface) # end

Office_Firewall (ospf) # end

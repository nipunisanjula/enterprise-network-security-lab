Spanning Tree PortFast Configurations on DMZ_Switch

DMZ_Switch(config)#interface range gigabitEthernet 0/1 - 2

DMZ_Switch(config-if-range)#spanning-tree portfast

STP Root primary configurations on L3_Switch_2

L3_Switch_2(config)#spanning-tree vlan 1 root primary

STP Root secondary configurations on Switch_1

Switch_1(config)#spanning-tree vlan 1 root secondary
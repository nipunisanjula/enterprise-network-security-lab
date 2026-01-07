# **VLAN configurations on Switch_1**

Switch_1(config)#vlan 10

Switch_1(config-vlan)#name IT

Switch_1(config-vlan)#exit

Switch_1(config)#vlan 20

Switch_1(config-vlan)#name HR

Switch_1(config-vlan)#exit

Switch_1(config)#vlan 30

Switch_1(config-vlan)#name Sales

Switch_1(config-vlan)#

Switch_1(config)#int rang gi0/2 - 3

Switch_1(config-if)#switchport mode access

Switch_1(config-if)#switchport access vlan 10

Switch_1(config-if)#exit

Switch_1(config)#int range gi1/0 - 3

Switch_1(config-if-range)#switchport mode access

Switch_1(config-if-range)#switchport access vlan 20

Switch_1(config-if-range)#exit

Switch_1(config)#int range gi2/0 - 3

Switch_1(config-if-range)#switchport mode access

Switch_1(config-if-range)#switchport access vlan 30

Switch_1(config-if-range)#exit

Switch_1(config)#int range gi0/0 - 1

Switch_1(config-if-range)#switchport trunk encapsulation dot1q

Switch_1(config-if-range)#switchport mode trunk

Switch_1(config-if-range)#exit

Switch_1(config)#do show interfaces trunk

# **VLAN configurations on Switch_2**

Switch_2(config)#vlan 10

Switch_2(config-vlan)#name IT

Switch_2(config-vlan)#exit

Switch_2(config)#vlan 20

Switch_2(config-vlan)#name HR

Switch_2(config-vlan)#exit

Switch_2(config)#vlan 30

Switch_2(config-vlan)#name Sales

Switch_2(config-vlan)#exit

Switch_2(config)#vlan 70

Switch_2(config-vlan)#name StandBy

Switch_2(config-vlan)#exit

Switch_2(config)#int gi0/2

Switch_2(config-if)#switchport mode access

Switch_2(config-if)#switchport access vlan 10

Switch_2(config-if)#exit

Switch_2(config)#int gi0/3

Switch_2(config-if)#switchport mode access

Switch_2(config-if)#switchport access vlan 20

Switch_2(config-if)#exit

Switch_2(config)#int gi1/0

Switch_2(config-if)#switchport mode access

Switch_2(config-if)#switchport access vlan 30

Switch_2(config-if)#exit

Switch_2(config)#int range gi1/1 - 3

Switch_2(config-if-range)#switchport mode access

Switch_2(config-if-range)#switchport access vlan 70

Switch_2(config-if-range)#exit

Switch_2(config)#int range gi0/0 - 1

Switch_2(config-if-range)#switchport trunk encapsulation dot1q

Switch_2(config-if-range)#switchport mode trunk

Switch_2(config-if-range)#exit

# **VLAN configurations on L3_Switch_1**

L3_Switch_1(config)#vlan 80

L3_Switch_1(config-vlan)#name servers

L3_Switch_1(config-vlan)#exit

L3_Switch_1(config)#vlan 70

L3_Switch_1(config-vlan)#name StandBy

L3_Switch_1(config-vlan)#exit

L3_Switch_1(config)#vlan 10

L3_Switch_1(config-vlan)#name IT

L3_Switch_1(config-vlan)#exit

L3_Switch_1(config)#vlan 20

L3_Switch_1(config-vlan)#name HR

L3_Switch_1(config-vlan)#exit

L3_Switch_1(config)#vlan 30

L3_Switch_1(config-vlan)#name Sales

L3_Switch_1(config-vlan)#exit

L3_Switch_1(config)#int gi0/3

L3_Switch_1(config-if)#switchport mode access

L3_Switch_1(config-if)#switchport access vlan 80

L3_Switch_1(config-if)#exit

L3_Switch_1(config)#int range gi1/0 - 1

L3_Switch_1(config-if-range)#switchport mode access

L3_Switch_1(config-if-range)#switchport access vlan 80

L3_Switch_1(config-if-range)#exit

L3_Switch_1(config)#int range gi1/2 - 3

L3_Switch_1(config-if-range)#switchport mode access

L3_Switch_1(config-if-range)#switchport access vlan 70

L3_Switch_1(config-if-range)#exit

L3_Switch_1(config)#int range gi0/0 - 2

L3_Switch_1(config-if-range)#switchport trunk encapsulation dot1q

L3_Switch_1(config-if-range)#switchport mode trunk

L3_Switch_1(config-if-range)#exit

VLAN Configurations on L3_Switch_2

L3_Switch_2(config)#vlan 20

L3_Switch_2(config-vlan)#name HR

L3_Switch_2(config-vlan)#exit

L3_Switch_2(config)#vlan 30

L3_Switch_2(config-vlan)#name Sales

L3_Switch_2(config-vlan)#exit

L3_Switch_2(config)#vlan 10

L3_Switch_2(config-vlan)#name IT

L3_Switch_2(config-vlan)#exit

L3_Switch_2(config)#vlan 70

L3_Switch_2(config-vlan)#name StandBy

L3_Switch_2(config-vlan)#exit

L3_Switch_2(config)#int gi1/2

L3_Switch_2(config-if)#switchport mode access

L3_Switch_2(config-if)#switchport access vlan 20

L3_Switch_2(config-if)#exit

L3_Switch_2(config)#int gi1/3

L3_Switch_2(config-if)#switchport mode access

L3_Switch_2(config-if)#switchport access vlan 30

L3_Switch_2(config-if)#exit

L3_Switch_2(config)#int range gi0/0 – 3

L3_Switch_2(config-if-range)#switchport trunk encapsulation dot1q

L3_Switch_2(config-if-range)#switchport mode trunk

L3_Switch_2(config-if-range)#exit

L3_Switch_2(config)#int range gi1/0 - 1

L3_Switch_2(config-if-range)#switchport trunk encapsulation dot1q

L3_Switch_2(config-if-range)#switchport mode trunk

L3_Switch_2(config-if-range)#exit

# **VLAN configurations on DMZ_Switch**

DMZ_Switch(config)#vlan 50

DMZ_Switch(config-vlan)#name DMZ

DMZ_Switch(config-vlan)#exit

DMZ_Switch(config)#int rang gi0/1 - 3

DMZ_Switch(config-if-range)#switchport mode access

DMZ_Switch(config-if-range)#switchport access vlan 50

DMZ_Switch(config-if-range)#exit

DMZ_Switch(config)#int gi0/0

DMZ_Switch(config-if)#switchport trunk encapsulation dot1q

DMZ_Switch(config-if)#switchport mode trunk

DMZ_Switch(config-if)#exit

# **Port security configurations on Switch_1**

Switch_1(config)#interface range gi0/2 - 3

Switch_1 (config-if-range)#switchport mode access

Switch_1 (config-if-range)#switchport port-security

Switch_1 (config-if-range)#switchport port-security mac-address sticky

Switch_1 (config-if-range)#switchport port-security maximum 1

Switch_1 (config-if-range)#switchport port-security violation shutdown

Switch_1 (config-if-range)#exit

Switch_1 (config)#interface range gi1/0 - 3

Switch_1 (config-if-range)#switchport mode access

Switch_1 (config-if-range)#switchport port-security

Switch_1 (config-if-range)#switchport port-security mac-address sticky

Switch_1 (config-if-range)#switchport port-security maximum 1

Switch_1 (config-if-range)#switchport port-security violation shutdown

Switch_1 (config-if-range)#exit

Switch_1 (config)#interface range gi2/0 - 3

Switch_1 (config-if-range)#switchport mode access

Switch_1 (config-if-range)#switchport port-security

Switch_1 (config-if-range)#switchport port-security mac-address sticky

Switch_1 (config-if-range)#switchport port-security maximum 1

Switch_1 (config-if-range)#switchport port-security violation shutdown

Switch_1 (config-if-range)#exit

Switch_1(config)#interface range gi1/2 - 3

Switch_1(config-if-range)#shutdown

Switch_1(config-if-range)#exit

Switch_1(config)#interface range gi2/1 - 3

Switch_1(config-if-range)#shutdown

Switch_1(config-if-range)#exit

# **Port security configurations on Switch_2**

Switch_2(config)#interface range gi0/2 - 3

Switch_2(config-if-range)#switchport mode access

Switch_2(config-if-range)#switchport port-security

Switch_2(config-if-range)#switchport port-security mac-address sticky

Switch_2(config-if-range)#switchport port-security maximum 1

Switch_2(config-if-range)#switchport port-security violation shutdown

Switch_2(config-if-range)#exit

Switch_2(config)#interface range gi1/0 - 3

Switch_2(config-if-range)#switchport mode access

Switch_2(config-if-range)#switchport port-security

Switch_2(config-if-range)#switchport port-security mac-address sticky

Switch_2(config-if-range)#switchport port-security maximum 1

Switch_2(config-if-range)#switchport port-security violation shutdown

Switch_2(config-if-range)#exit

Switch_2(config)#interface range gi1/1 - 3

Switch_2(config-if-range)#shutdown

# **Port security configurations on DMZ_Switch**

DMZ_Switch (config)#interface range gi0/1- 3

DMZ_Switch (config-if-range)#switchport mode access

DMZ_Switch (config-if-range)#switchport port-security

DMZ_Switch (config-if-range)#switchport port-security mac-address sticky

DMZ_Switch (config-if-range)#switchport port-security maximum 1

DMZ_Switch (config-if-range)#switchport port-security violation shutdown

DMZ_Switch (config-if-range)#exit

# **Port security configurations on L3_Switch_1**

L3_Switch_1 (config)#interface gi0/3

L3_Switch_1 (config-if-range)#switchport mode access

L3_Switch_1 (config-if-range)#switchport port-security

L3_Switch_1 (config-if-range)#switchport port-security mac-address sticky

L3_Switch_1 (config-if-range)#switchport port-security maximum 1

L3_Switch_1 (config-if-range)#switchport port-security violation shutdown

L3_Switch_1 (config-if-range)#exit

L3_Switch_1 (config)#interface range gi1/0 - 3

L3_Switch_1 (config-if-range)#switchport mode access

L3_Switch_1 (config-if-range)#switchport port-security

L3_Switch_1 (config-if-range)#switchport port-security mac-address sticky

L3_Switch_1 (config-if-range)#switchport port-security maximum 1

L3_Switch_1 (config-if-range)#switchport port-security violation shutdown

L3_Switch_1 (config-if-range)#exit

L3_Switch_1 (config)#interface range gi1/2 - 3

L3_Switch_1 (config-if-range)#shutdown

# **Port security configurations on L3_Switch_2**

L3_Switch_2 (config)#interface range gi1/2 - 3

L3_Switch_2 (config-if-range)#switchport mode access

L3_Switch_2 (config-if-range)#switchport port-security

L3_Switch_2 (config-if-range)#switchport port-security mac-address sticky

L3_Switch_2 (config-if-range)#switchport port-security maximum 1

L3_Switch_2 (config-if-range)#switchport port-security violation shutdown

L3_Switch_2 (config-if-range)#exit

# **Port security configurations on Branch_Switch**

Branch_Switch(config)#int range gi0/1 - 3

Branch_Switch(config-if-range)#switchport mode access

Branch_Switch(config-if-range)#switchport port-security

Branch_Switch(config-if-range)#switchport port-security mac-address sticky

Branch_Switch(config-if-range)#switchport port-security violation shutdown

Branch_Switch(config-if-range)#exit

Branch_Switch (config)#interface gi0/3

Branch_Switch (config-if-range)#shutdown

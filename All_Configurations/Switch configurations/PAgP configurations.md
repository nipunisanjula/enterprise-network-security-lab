# **Etherchannel PAgP Configuration on L3_switch_2**

L3_switch_2(config)#int range gi 0/0-1

L3_switch_2(config-if-range)#channel-group 1 mode desirable

L3_switch_2(config-if-range)#int range gi 0/2 - 3

L3_switch_2(config-if-range)#channel-group 2 mode desirable

L3_switch_2(config-if-range)#int range gi 1/0 - 1

L3_switch_2(config-if-range)#channel-group 3 mode desirable

L3_switch_2(config)# int range port-channel 1 - 3

L3_switch_2(config-if-range)#switchport mode trunk

# **Etherchannel PAgP Configuration on Switch_2**

Switch_2(config)#int range gi0/0 - 1

Switch_2(config-if-range)#channel-group 2 mode auto

Switch_2(config)#int port-channel 2

Switch_2(config-if)#switchport mode trunk

# **Etherchannel PAgP Configuration on Switch_1**

Switch_1(config)#int range gi0/0 - 1

Switch_1(config-if-range)#channel-group 3 mode auto

Switch_1(config)#int port-channel 3

Switch_1(config-if)#switchport mode trunk

# **Etherchannel PAgP Configuration on L3_switch_1**

L3_switch_1(config)#int range gi0/1 - 2

L3_switch_1(config-if-range)#channel-group 1 mode auto

L3_switch_2(config)# int port-channel 1

L3_switch_2(config-if-range)#switchport mode trunk

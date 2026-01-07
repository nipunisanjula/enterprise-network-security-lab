# **IPsec site to site VPN configurations on Router_Office**

Office(config)#int tunnel 10

Office(config-if)#ip add 10.10.10.1 255.255.255.252

Office(config-if)#tunnel source gi0/1

Office(config-if)#tunnel destination 40.1.1.1

Office(config-if)#exit

Office(config)#router ospf 1

Office(config-router)#network 10.10.10.0 0.0.0.3 area 0

Office(config)#crypto isakmp policy 10

Office(config-isakmp)#encryption aes

Office(config-isakmp)#authentication pre-share

Office(config-isakmp)#hash md5

Office(config-isakmp)#lifetime 1000

Office(config-isakmp)#group 1

Office(config)#crypto isakmp key RTU address 40.1.1.1

Office(config)#crypto ipsec transform-set OB esp-3des esp-md5-hmac

Office(cfg-crypto-trans)#mode transport

Office(cfg-crypto-trans)#exit

Office(config)#crypto ipsec profile OB

Office(ipsec-profile)#set transform-set OB

Office(ipsec-profile)#exit

Office(config)#int tunnel 10

Office(config-if)#tunnel protection ipsec profile OB

# **IPsec Site to Site VPN configurations on Router_Branch**

Router_Branch(config)#int tunnel 10

Router_Branch (config-if)#ip add 10.10.10.2 255.255.255.252

Router_Branch(config-if)#tunnel destination 20.1.1.2

Router_Branch(config-if)#tunnel source gi0/0

Router_Branch(config)#router ospf 1

Router_Branch(config-router)#network 10.10.10.0 0.0.0.3 area 0

Router_Branch(config)#crypto isakmp policy 1

Router_Branch(config-isakmp)#encryption aes

Router_Branch(config-isakmp)#authentication pre-share

Router_Branch(config-isakmp)#hash md5

Router_Branch(config-isakmp)#lifetime 1000

Router_Branch(config-isakmp)#group 1

Router_Branch(config-isakmp)#exit

Router_Branch(config)#crypto isakmp key RTU address 20.1.1.2

Router_Branch(config)#crypto ipsec transform-set OB esp-3des esp-md5-hmac

Router_Branch(cfg-crypto-trans)#mode transport

Router_Branch(cfg-crypto-trans)#exit

Router_Branch(config)#crypto ipsec profile OB

Router_Branch(ipsec-profile)#set transform-set OB

Router_Branch(ipsec-profile)#exit

Router_Branch(config)#int tunnel 10

Router_Branch(config-if)#tunnel protection ipsec profile OB

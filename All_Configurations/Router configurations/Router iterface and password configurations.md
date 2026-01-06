# **Interface configurations and router passwords on ISP_NAT**

Internet(config)#hostname ISP_NAT

ISP_NAT(config)#banner motd # Welcome to Internet #

ISP_NAT#clock set 14:21:30 29 october 2025

ISP_NAT(config)#line console 0

ISP_NAT(config-line)#password int123

ISP_NA(config-line)#login

ISP_NAT(config)#line aux 0

ISP_NAT(config-line)#password int123

ISP_NAT(config-line)#login

ISP_NAT(config)#line vty 0 9

ISP_NAT(config-line)#password int123

ISP_NAT(config-line)#login

ISP_NAT(config-line)#transport input telnet

ISP_NAT(config)#enable password int123

ISP_NAT(config)# do show run

ISP_NAT(config)#enable secret int456

ISP_NAT(config)# do show run

ISP_NAT(config)#service password-encryption

ISP_NAT(config)# do show run

ISP_NAT(config)#interface gi0/0

ISP_NAT(config-if)#no shut

ISP_NAT(config-if)#ip address 192.168.100.1 255.255.255.0

ISP_NAT(config-if)#description ISP_1

ISP_NAT(config-if)#exit

ISP_NAT(config)#interface gi0/1

ISP_NAT(config-if)#no shut

ISP_NAT(config-if)#ip add dhcp

ISP_NAT(config-if)#duplex full

ISP_NAT(config-if)#description Internet

ISP_NAT(config-if)#exit

ISP_NAT(config)#interface gi0/2

ISP_NAT(config-if)#ip address 192.168.200.1 255.255.255.0

ISP_NAT(config-if)# description ISP_2

ISP_NAT(config-if)#no shut

ISP_NAT(config-if)#exit

ISP_NAT#sh ip int br

# **Interface configurations and router passwords on ISP_1**

Router(config)#hostname ISP_1

ISP_1(config)#banner motd # Welcome to ISP_1#

ISP_1(config)#line console 0

ISP_1(config-line)#password isp123

ISP_1(config-line)#login

ISP_1(config-line)#exit

ISP_1(config)#line aux 0

ISP_1(config-line)#password isp123

ISP_1(config-line)#login

ISP_1(config-line)#exit

ISP_1(config)#line vty 0 9

ISP_1(config-line)#password isp123

ISP_1(config-line)#login

ISP_1(config-line)#transport input telnet

ISP_1(config-line)#exit

ISP_1(config)#enable secret isp123

ISP_1(config)#service password-encryption

ISP_1(config)#interface gi0/0

ISP_1(config-if)#no shut

ISP_1(config-if)#ip address 40.1.1.2 255.255.255.192

ISP_1(config-if)#description Router_Branch

ISP_1(config-if)#exit

ISP_1(config)#interface gi0/1

ISP_1(config-if)#no shut

ISP_1(config-if)#ip address 20.1.1.1 255.255.255.0

ISP_1(config-if)#description ROUTER_OFFICE

ISP_1(config-if)#exit

ISP_1(config)#int gi0/2

ISP_1(config-if)#no shut

ISP_1(config-if)#ip add 192.168.100.2 255.255.255.0

ISP_1(config-if)#description ISP_NAT

ISP_1(config-if)#exit

# **Interface configurations and router passwords on ISP_2**

Router(config)#hostname ISP_2

ISP_2(config)#banner motd # Welcome to ISP_2#

ISP_2(config)#line console 0

ISP_2(config-line)#password isp456

ISP_2(config-line)#login

ISP_2(config-line)#exit

ISP_2(config)#line aux 0

ISP_2(config-line)#password isp456

ISP_2(config-line)#login

ISP_2(config-line)#exit

ISP_2(config)#line vty 0 9

ISP_2(config-line)#password isp456

ISP_2(config-line)#login

ISP_2(config-line)#transport input telnet

ISP_2(config-line)#exit

ISP_2(config)#enable secret isp456

ISP_2(config)#service password-encryption

ISP_2(config)#interface gi0/0

ISP_2(config-if)#no shut

ISP_2(config-if)#ip address 40.1.1.66 255.255.255.192

ISP_2(config-if)#description Router \_Branch

ISP_2(config-if)#exit

ISP_2(config)#interface gi0/1

ISP_2(config-if)#no shut

ISP_2(config-if)#ip address 30.1.1.1 255.255.255.0

ISP_2(config-if)#description ROUTER_OFFICE

ISP_2(config-if)#exit

ISP_2(config)#int gi0/2

ISP_2(config-if)#ip add 192.168.200.2 255.255.255.0

ISP_2(config-if)#no shut

ISP_2(config-if)#sdescription ISP_NAT

ISP_2(config-if)#exit

# **Interface configurations and router passwords on Router_Office**

Router(config)#hostname Office

Office(config)#banner motd # Welcome to Office #

Office(config)#line console 0

Office(config-line)#password Cs@1!2Ax

Office(config-line)#login

Office(config-line)#exit

Office(config)#line aux 0

Office(config-line)#password Cs@1!2Ax

Office(config-line)#login

Office(config-line)#exit

Office(config)#line vty 0 9

Office(config-line)#password Tl@1!2vbn

Office(config-line)#login

Office(config-line)#transport input telnet

Office(config-line)#exit

Office(config)#enable secret Es@1!2vbn

Office(config)#service password-encryption

Office(config)#interface gi0/0

Office(config-if)#no shut

Office(config-if)#ip address 192.168.1.1 255.255.255.0

Office(config-if)#description OFFICE_LAN

Office(config-if)#exit

Office(config)#interface gi0/1

Office(config-if)#ip address 20.1.1.2 255.255.255.0

Office(config-if)#description ISP_1

Office(config-if)#no shut

Office(config-if)#exit

Office(config)#interface gi0/2

Office(config-if)#ip address 30.1.1.2 255.255.255.0

Office(config-if)#description ISP_2

Office(config-if)#no shut

Office(config-if)#exit

# **Interface configurations and router passwords on Router_Branch**

Router(config)#hostname Router_Branch

Router_Branch(config)#banner motd # Welcome to Branch #

Router_Branch #clock set 14:21:30 29 october 2025

Router_Branch(config)#line console 0

Router_Branch(config-line)#password Rb123

Router_Branch(config-line)#login

Router_Branch(config-line)#exit

Router_Branch(config)#line aux 0

Router_Branch(config-line)#password Rb123

Router_Branch(config-line)#login

Router_Branch(config-line)#exit

Router_Branch(config)#line vty 0 9

Router_Branch(config-line)#password Rb123

Router_Branch(config-line)#login

Router_Branch(config-line)#transport input telnet

Router_Branch(config-line)#exit

Router_Branch(config)#enable secret Rb456

Router_Branch(config)#service password-encryption

Router_Branch(config)#interface gi0/0

Router_Branch(config-if)#no shut

Router_Branch(config-if)#ip address 40.1.1.1 255.255.255.192

Router_Branch(config-if)#description ISP_1

Router_Branch(config-if)#exit

Router_Branch(config)#interface gi0/1

Router_Branch(config-if)#ip address 40.1.1.65 255.255.255.192

Router_Branch(config-if)#description ISP_2

Router_Branch(config-if)#no shut

Router_Branch(config)#interface gi0/2

Router_Branch(config-if)#ip address 192.168.40.1 255.255.255.0

Router_Branch(config-if)#description Office_Lan

Router_Branch(config-if)#no shut

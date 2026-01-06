# **Firewall port configurations**

FMG-VM64-KVM # config system global

(global)# set hostname Office_Firewall

(global)# end

Office_Firewall # config system interface

Office_Firewall (interface) # edit port1

Office_Firewall (port1) # set mode static

Office_Firewall (port1) # set ip 192.168.3.1 255.255.255.0

Office_Firewall (port1) # set alias LAN

Office_Firewall (port1) # set role lan

Office_Firewall (port1) # set allowaccess http https ping ssh fgfm

Office_Firewall (port1) # next

Office_Firewall (interface) # edit port2

Office_Firewall (port2) # set mode static

Office_Firewall (port2) # set ip 192.168.1.2 255.255.255.0

Office_Firewall (port2) # set alias WAN

Office_Firewall (port2) # set role wan

Office_Firewall (port2) # set allowaccess ping https

Office_Firewall (port2) # next

Office_Firewall # config system interface

Office_Firewall (interface) # edit port3

Office_Firewall (port3) # set mode static

Office_Firewall (port3) # set ip 192.168.2.1 255.255.255.0

Office_Firewall (port3) # set alias DMZ

Office_Firewall (port3) # set role dmz

Office_Firewall (port3) # set allowaccess ping http https

Office_Firewall (port3) # end

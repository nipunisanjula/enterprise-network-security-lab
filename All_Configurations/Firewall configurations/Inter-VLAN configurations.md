# **Firewall Inter-VLAN Configuration**

Office_Firewall # config system interface

Office_Firewall (interface) # edit vlan10

Office_Firewall (vlan10) # set vdom root

Office_Firewall (vlan10) # set ip 192.168.10.1 255.255.255.0

Office_Firewall (vlan10) # set allowaccess ping https ssh http

Office_Firewall (vlan10) # set role lan

Office_Firewall (vlan10) # set interface port1

Office_Firewall (vlan10) # set vlanid 10

Office_Firewall (vlan10) # next

Office_Firewall (interface) # edit vlan20

Office_Firewall (vlan20) # set vdom root

Office_Firewall (vlan20) # set ip 192.168.20.1 255.255.255.0

Office_Firewall (vlan20) # set allowaccess ping https ssh http

Office_Firewall (vlan20) # set role lan

Office_Firewall (vlan20) # set interface port1

Office_Firewall (vlan20) # set vlanid 20

Office_Firewall (vlan20) # next

Office_Firewall (interface) # edit vlan30

Office_Firewall (vlan30) # set vdom root

Office_Firewall (vlan30) # set ip 192.168.30.1 255.255.255.0

Office_Firewall (vlan30) # set allowaccess ping https ssh http

Office_Firewall (vlan30) # set role lan

Office_Firewall (vlan30) # set interface port1

Office_Firewall (vlan30) # set vlanid 30

Office_Firewall (vlan30) # next

Office_Firewall (interface) # edit vlan70

Office_Firewall (vlan70) # set vdom root

Office_Firewall (vlan70) # set ip 192.168.70.1 255.255.255.0

Office_Firewall (vlan70) # set allowaccess ping https ssh http

Office_Firewall (vlan70) # set role lan

Office_Firewall (vlan70) # set interface port1

Office_Firewall (vlan70) # set vlanid 70

Office_Firewall (vlan70) # next

Office_Firewall (interface) # edit vlan80

Office_Firewall (vlan80) # set vdom root

Office_Firewall (vlan80) # set ip 192.168.80.1 255.255.255.0

Office_Firewall (vlan80) # set allowaccess ping https ssh http

Office_Firewall (vlan80) # set role lan

Office_Firewall (vlan80) # set interface port1

Office_Firewall (vlan80) # set vlanid 80

Office_Firewall (vlan80) # next

Office_Firewall (interface) # end

Office_Firewall (interface) # edit vlan50

Office_Firewall (vlan50) # set vdom root

Office_Firewall (vlan50) # set ip 192.168.50.1 255.255.255.0

Office_Firewall (vlan50) # set allowaccess ping https ssh http

Office_Firewall (vlan50) # set role dmz

Office_Firewall (vlan50) # set interface port3

Office_Firewall (vlan50) # set vlanid 50

Office_Firewall (vlan50) # next

Office_Firewall (interface) # end

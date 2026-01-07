# **Static routing(floating)on FortiGate**

Office_Firewall # config router static

Office_Firewall (static) # edit 1

Office_Firewall (1) # set dst 0.0.0.0 0.0.0.0

Office_Firewall (1) # set gateway 192.168.100.1

Office_Firewall (1) # set distance 100

Office_Firewall (1) # set device port2

Office_Firewall (1) # next

Office_Firewall (static) # edit 2

Office_Firewall (2) # set dst 0.0.0.0 0.0.0.0

Office_Firewall (2) # set gateway 192.168.200.1

Office_Firewall (2) # set distance 200

Office_Firewall (2) # set device port2

Office_Firewall (2) # next

Office_Firewall (static) # end

DHCP configuration on Router_Branch

Router_Branch(config)#ip dhcp pool OFFICE

Router_Branch(dhcp-config)#network 192.168.40.0 255.255.255.0

Router_Branch(dhcp-config)#default-router 192.168.40.1

Router_Branch(dhcp-config)#dns-server 8.8.8.8

DHCP Snooping configuration on Branch_Switch

Branch_Switch(config)#ip dhcp snooping

Branch_Switch(config)#int gi0/0

Branch_Switch(config-if)#ip dhcp snooping trust

Proxy server

sudo apt install squid

sudo systemctl restart squid

sudo systemctl status squid

sudo cp /etc/squid/squid.conf /etc/squid/squid.conf.back

sudo nano /etc/squid/squid.conf

tail -f /var/log/squid/access.log

Cacti server

sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql

sudo apt install php-snmp php-xml php-mbstring php-json php-gd php-curl -y

sudo su –

mysql -u root -p

CREATE USER ‘cacti’@‘localhost’ IDENTIFIED BY ‘123’;

GRANT ALL PRIVILEGES ON cacti.\*To‘cacti’@‘localhost’;

FLUSH PRIVILEGES;

EXIT

sudo apt install cacti cacti-spine

sudo apt install snmp snmpd

sudo systemctl restart snmpd.service

FTP server

sudo apt install vsftpd

sudo systemctl status vsftpd

sudo adduser ftpuser

sudo nano /etc/ssh/sshd_config

sudo mkdir /usr/ftpshare

sudo usermod -d /usr/ftpshare/ftpuser

sudo mkdir /usr/ftpshare/filezilla

sudo chown ftpuser:ftpuser /usr/ftpshare/filezilla

sudo nano /etc/vsftpd.conf

sudo cat /var/log/vsftpd.log

AAA server

sudo apt install freeradius freeradius-utils

sudo su –

ls /etc/freeradius/3.0/

nano /etc/freeradius/3.0/clients.conf

nano /etc/freeradius/3.0/users

sudo freeradius -C

sudo radtest admin linux localhost 0 rad123
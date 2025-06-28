Cisco ASA: 

###1.Create Object Network, binding the FTP server IP:
YJN-FW1# conf t
YJN-FW1(config)# object network YJN-FTP-Server
YJN-FW1(config-network-object)#  host 10.3.10.200

###2.ACL settings:
YJN-FW1#access-list OUTSIDE_ACL extended permit tcp any object YJN-FTP-Server eq ftp log
YJN-FW1#access-list OUTSIDE_ACL extended permit tcp any object YJN-FTP-Server range 50000 50009 log

###3.NAT settings:
YJN-FW1# conf t
YJN-FW1(config)# object network YJN-FTP-Server
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp ftp 8021
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp 50000 50009 --> probably not working: refer to step4

###4.Port Mapping Settings --> In case of port range mapping not working
YJN-FW1(config)# object network YJN-FTP-Data
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp 50000 50000
YJN-FW1(config)# object network YJN-FTP-Data1
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp 50001 50001
YJN-FW1(config)# object network YJN-FTP-Data2
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp 50002 50002
.
.
.
YJN-FW1(config)# object network YJN-FTP-Data9
YJN-FW1(config)# nat (inside_vlan1110,outside_2) static interface service tcp 50009 50009

###5.Confirm commands:
YJN-FW1#show run nat
YJN-FW1#show run access-list
YJN-FW1#show run object network
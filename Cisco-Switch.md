YJN-EDGESW1#show ip dhcp binding -->confirm mac address

YJN-EDGESW1#conf t
YJN-EDGESW1(config)#ip dhcp excluded-address 10.1.10.100

YJN-EDGESW1(config)ip dhcp pool FTP-Server
YJN-EDGESW1(dhcp-config)# host 10.1.10.100 255.255.255.0
YJN-EDGESW1(dhcp-config)# client-identifier 01bc.091b.e409.a8
YJN-EDGESW1(dhcp-config)# default-router 10.1.10.100

YJN-EDGESW1# show run | sec dhcp -->confirm settings


cmd: dhcp release
ipconfig /release
ipconfig /renew
ipconfig /flushdns

YJN-EDGESW1#show ip dhcp binding
Bindings from all pools not associated with VRF:
IP address      Client-ID/              Lease expiration        Type       State      Interface
                Hardware address/
                User name
10.3.10.33      01bc.091b.d2b5.1d       Jun 29 2025 06:16 PM    Automatic  Active     Vlan1101
10.3.10.35      01c8.5ea9.1ff9.87       Jun 29 2025 01:20 AM    Automatic  Active     Vlan1101
10.3.10.92      01c8.5ea9.1e1f.04       Jun 29 2025 06:04 PM    Automatic  Active     Vlan1101
10.3.10.113     01c8.5ea9.1e1e.f0       Jun 29 2025 02:08 AM    Automatic  Active     Vlan1101
10.3.10.133     01c8.5ea9.1eb6.e9       Jun 29 2025 07:37 PM    Automatic  Active     Vlan1101
10.3.10.136     01c8.5ea9.1e1f.27       Jun 29 2025 10:42 PM    Automatic  Active     Vlan1101
10.3.10.149     011c.e192.91d7.15       Jun 29 2025 11:54 AM    Automatic  Active     Vlan1101
10.3.10.154     01c8.5ea9.1ee3.8a       Jun 29 2025 11:54 AM    Automatic  Active     Vlan1101
10.3.10.200     01bc.091b.e409.a8       Infinite                Manual     Active     Vlan1101
10.3.30.15      01aa.4c17.d0d5.85       Jun 29 2025 08:04 PM    Automatic  Active     Vlan1101
10.3.30.44      0140.1a58.bc45.76       Jun 29 2025 11:57 AM    Automatic  Active     Vlan1101
10.3.30.48      0174.9779.c54e.d1       Jun 29 2025 11:41 AM    Automatic  Active     Vlan1101
10.3.30.137     01e2.ca96.0023.79       Jun 29 2025 12:15 PM    Automatic  Active     Vlan1101
# config
underlay - control-plane - unicast: ospf
underlay - control-plane - bum: ir w/ ibgp
overlay - control-plane: evpn w/ ibgp
overlay - data-plane: vxlan w/ mpls

# show
## preparation
show ip interface brief

## underlay
show cli history unformatted
show ip ospf neighbors 
show run bgp
show bgp l2vpn evpn summary

## overlay l2 bridging
ping 192.168.10.12 count unlimited interval 1
show run vlan
show run interface nve 1
show bgp l2vpn evpn summary
show bgp l2vpn evpn
show run | sec evpn
show vxlan
show nve interface 
show nve vni
show mac address-table dynamic

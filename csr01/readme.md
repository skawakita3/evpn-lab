# ref
https://www.cisco.com/c/en/us/td/docs/routers/ios/config/17-x/mpls/b-mpls/m-ce-evpn-single-homing.html

# config
underlay - control-plane - unicast: ospf
underlay - control-plane - bum: ir w/ ibgp
overlay - control-plane: evpn w/ ibgp
overlay - data-plane: evpn w/ mpls

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

# config
underlay - control-plane - unicast: ibgp w/ ospf
underlay - control-plane - bum: pim asm
overlay - control-plane: evpn w/ ibgp
overlay - data-plane: vxlan w/ vlan

# show
## preparation
show ip interface brief

## underlay
show cli history unformatted
show ip ospf neighbors 
show ip pim rp
show ip pim neighbor 
show run bgp
show bgp l2vpn evpn summary

## overlay l2 bridging
ping 192.168.10.12 count unlimited interval 1
show run vlan
show vxlan
show run interface nve 1
show run | sec evpn
show bgp l2vpn evpn summary
show nve interface 
show mac address-table dynamic
show nve vni

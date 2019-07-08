# OVS Problem

### 1. none of the usable flow formats 
> ovs-ofctl: none of the usable flow formats (OXM-OpenFlow13,OXM-OpenFlow14,OXM-OpenFlow15,OXM-OpenFlow16) is among the allowed flow formats (OpenFlow10,NXM)

A: 需要显示的指定OpenFlow的版本，例如加上`-O OpenFlow13`

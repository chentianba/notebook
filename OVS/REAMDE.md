# OVS Resource
* [OVS常用命令与使用总结](https://blog.csdn.net/u010378472/article/details/79043094)

# OVS Problem

### 1. none of the usable flow formats 
> ovs-ofctl: none of the usable flow formats (OXM-OpenFlow13,OXM-OpenFlow14,OXM-OpenFlow15,OXM-OpenFlow16) is among the allowed flow formats (OpenFlow10,NXM)

A: 需要显示的指定OpenFlow的版本，例如加上`-O OpenFlow13`

### 2. 使用2.8以上的OVS版本，但是查看meter功能时，显示不支持  
```
# ovs-ofctl -O OpenFlow13 meter-features s1
OFPST_METER_FEATURES reply (OF1.3) (xid=0x2):
max_meter:0 max_bands:0 max_color:0
band_types: 0
capabilities: 0
```
A: 使用命令将datapath设置为netdev
```
# ovs-vsctl set bridge s2 datapath_type=netdev
```
### 3. ovs-vsctl: unix:/usr/local/var/run/openvswitch/db.sock: database connection failed (No such file or directory)  
    **Solution:**
    ```Bash
    sudo /usr/share/openvswitch/scripts/ovs-ctl stop
    sudo /usr/share/openvswitch/scripts/ovs-ctl start
    ```
### 4. 默认ovs安装只安装低版本，高版本需要自己手动编译安装

   **查看版本命令:**
   > \# ovs-vsctl show
   
   [安装教程](https://www.cnblogs.com/goldsunshine/p/10331606.html)

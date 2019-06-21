## OVS
1. ovs-vsctl: unix:/usr/local/var/run/openvswitch/db.sock: database connection failed (No such file or directory)  
    **Solution:**
    ```Bash
    sudo /usr/share/openvswitch/scripts/ovs-ctl stop
    sudo /usr/share/openvswitch/scripts/ovs-ctl start
    ```
2. 其他
## 其他

## OVS
1. ovs-vsctl: unix:/usr/local/var/run/openvswitch/db.sock: database connection failed (No such file or directory)  
    **Solution:**
    ```Bash
    sudo /usr/share/openvswitch/scripts/ovs-ctl stop
    sudo /usr/share/openvswitch/scripts/ovs-ctl start
    ```
2. 默认ovs安装只安装低版本，高版本需要自己手动编译安装

   **查看版本命令:**
   > \# ovs-vsctl show
   
   [安装教程](https://www.cnblogs.com/goldsunshine/p/10331606.html)
## system
1. gnome-shell_systemd-c++
    >Q: In opensuse 42.3, CPU usage of system is always 100%.  
    A: By command "tracker daemon -k; tracker reset --hard", I solve it.
2. linux动态的使用教程  
   > create and use linux dynamic library  
   [Solution](https://blog.csdn.net/jiangnanyouzi/article/details/3321150)
3. When using ;-L./lib -lhello' and run showing **".so:cannot open shared object file: No such file or directory"**
   > Solution: copy .so file to path in '/etc/ld.so.conf' and 'sudo ldconfig'.
## virtualbox
1. virtualbox-additions
   >When installing virtualbox additions, we need to install 'kernel-devel make gcc' first. Above all, you should guarantee your system is up-to-date.
2. Opensuse42.3 安装vmware14时,需要提前使用以下命令，再进行安装
   ```
   # modprobe -r kvm_intel
   # modprobe -r kvm
   ```

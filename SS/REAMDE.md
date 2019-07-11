## SS搭建
1. 服务器搭建参考[图文教程搭建一个vpn翻墙](https://github.com/yukaiji/buildVpn)  
2. 客户端参考配置[SS Wiki](https://github.com/Shadowsocks-Wiki/shadowsocks)  
3. Windows搭建ss服务器成功过[参考1](https://blog.whsir.com/post-559.html)、[参考2](http://www.8964cn.net/?post=52)，使用Nodejs安装ss  

## Linux版
**Server：**
使用命令行配置
```
# ssserver -c /etc/shadowsocks.json -d start
```
**Client：**
1. 使用运行ss服务
```
# /usr/local/bin/sslocal -c /etc/shadowsocks.json -d start
```
2. 将系统的代理关闭，在浏览器例如firefox使用手动代理配置，SOCKS主机设置成配置文件中的local地址和端口，选用SOCKSv
5选项，其他不变
3. 步骤2中也可以用步骤3替代，即使用系统的代理打开，手动设置，配置和步骤2类似，但是浏览器中需要将代理关闭

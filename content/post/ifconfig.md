ifconfig的使用方法
ifconfig是一个在Linux系统中用于配置和显示网络接口信息的命令行工具。它可以用来查看和修改网卡的IP地址、子网掩码、广播地址、MAC地址等。

常用使用方法如下：
1. 查看当前所有网络接口的信息：ifconfig
2. 查看指定网卡的信息：ifconfig eth0
3. 启用指定网卡：ifconfig eth0 up
4. 停用指定网卡：ifconfig eth0 down
5. 分配静态IP地址：ifconfig eth0 192.168.1.100
6. 分配子网掩码：ifconfig eth0 netmask 255.255.255.0
7. 设置MAC地址：ifconfig eth0 hw ether 00:11:22:33:44:55
8. 激活网卡的广播：ifconfig eth0 broadcast 192.168.1.255
9. 配置MTU值：ifconfig eth0 mtu 1500
10. 启用网络广播包过滤：ifconfig eth0 promisc
11. 禁用网络广播包过滤：ifconfig eth0 -promisc
12. 显示已经接收和发送的字节数据：ifconfig eth0 | grep 'RX packets\|TX packets'
13. 查看网卡的链接状态：ifconfig eth0 | grep 'Link'
14. 设置网卡的多播地址：ifconfig eth0 multicast
15. 获取网卡信息并将结果重定向到文件：ifconfig eth0 > output.txt
16. 清除网卡配置：ifconfig eth0 0.0.0.0
17. 重启网卡：ifconfig eth0 restart
18. 配置IPv6地址：ifconfig eth0 inet6 add 2001:db8::1/64
19. 显示所有循环接口的信息：ifconfig -a
20. 查看帮助信息：ifconfig --help

安装方法：在CentOS中，ifconfig工具默认已经安装好，无需单独安装。
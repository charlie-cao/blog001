firewalld的使用方法
Firewalld是CentOS中默认的防火墙管理工具，它提供了一种简单而灵活的方式来管理系统的防火墙规则。

1. 查看防火墙状态：`sudo systemctl status firewalld`。
2. 启动防火墙：`sudo systemctl start firewalld`。
3. 停止防火墙：`sudo systemctl stop firewalld`。
4. 重启防火墙：`sudo systemctl restart firewalld`。
5. 设置防火墙开机自启：`sudo systemctl enable firewalld`。
6. 关闭防火墙开机自启：`sudo systemctl disable firewalld`。

添加规则：
7. 添加一个允许的端口：`sudo firewall-cmd --add-port=80/tcp --permanent`（80为端口号）。
8. 删除已添加的端口：`sudo firewall-cmd --remove-port=80/tcp --permanent`。
9. 添加一个允许的服务：`sudo firewall-cmd --add-service=http --permanent`（http为服务名）。
10. 删除已添加的服务：`sudo firewall-cmd --remove-service=http --permanent`。
11. 添加一个允许的IP地址：`sudo firewall-cmd --add-source=192.168.1.100 --permanent`。
12. 删除已添加的IP地址：`sudo firewall-cmd --remove-source=192.168.1.100 --permanent`。

查看规则：
13. 查看当前生效的规则：`sudo firewall-cmd --list-all`。
14. 查看已打开的端口列表：`sudo firewall-cmd --list-ports`。
15. 查看已开放的服务列表：`sudo firewall-cmd --list-services`。
16. 查看已允许的源IP列表：`sudo firewall-cmd --list-sources`。

其他：
17. 临时开启防火墙：`sudo systemctl is-active firewalld`。
18. 在不重启防火墙的情况下重新加载规则：`sudo firewall-cmd --reload`。
19. 开放某个接口的所有端口：`sudo firewall-cmd --zone=public --add-interface=eth0`（eth0为接口名）。
20. 移除某个接口的所有端口：`sudo firewall-cmd --zone=public --remove-interface=eth0`。

注：所有命令执行后，需要重启防火墙才能使规则生效：`sudo systemctl restart firewalld`。
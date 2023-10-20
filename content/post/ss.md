ss的使用方法
SS（Shadowsocks）是一种被广泛用于科学上网的代理工具，在CentOS中安装可以通过以下步骤进行：

1. 打开终端，使用root权限登录系统。
2. 安装Python包管理工具pip：`yum install python-pip`。
3. 安装shadowsocks：`pip install shadowsocks`。
4. 创建配置文件：`vi /etc/shadowsocks.json`。
5. 在配置文件中输入以下内容：
```
{
  "server": "服务器IP地址",
  "server_port": 8388,
  "password": "密码",
  "method": "加密方法",
  "timeout": 300
}
```
6. 启动Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d start`。

使用方法：
1. 启动Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d start`。
2. 停止Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d stop`。
3. 重启Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d restart`。
4. 查看Shadowsocks服务运行状态：`ssserver -c /etc/shadowsocks.json -d status`。
5. 修改Shadowsocks配置文件：`vi /etc/shadowsocks.json`，然后重启服务。
6. 添加用户：`ssserver -c /etc/shadowsocks.json -d add_user 用户名 密码`。
7. 修改用户密码：`ssserver -c /etc/shadowsocks.json -d modify_user_password 用户名 新密码`。
8. 删除用户：`ssserver -c /etc/shadowsocks.json -d del_user 用户名`。
9. 查看当前连接数和连接信息：`ssserver -c /etc/shadowsocks.json -d show_connections`。
10. 查看日志：`tail -f /var/log/shadowsocks.log`。
11. 指定配置文件启动Shadowsocks服务：`ssserver -c /path/to/config.json -d start`。
12. 使用HTTP代理模式启动Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d start --plugin obfs-server --plugin-opts "obfs=http;obfs-host=www.example.com"`。
13. 使用UDP转发模式启动Shadowsocks服务：`ssserver -c /etc/shadowsocks.json -d start --udp-relay`。
14. 通过服务端提供的HTTP API接口修改配置：`curl -X POST -d '{
  "server":"服务器IP地址",
  "server_port":8388,
  "password":"新密码",
  "method":"加密方法",
  "timeout":300
}' http://127.0.0.1:4040/udpate`。
15. 使用ss-local作为本地代理客户端：`ss-local -c /etc/shadowsocks.json -l 1080`。
16. 使用ss-redir作为本地透明代理客户端：`ss-redir -c /etc/shadowsocks.json -l 1080 -u -f /var/run/shadowsocks.pid`。
17. 使用ss-tunnel作为本地DNS加密代理客户端：`ss-tunnel -c /etc/shadowsocks.json -l 5353 -L 8.8.8.8:53 -u -f /var/run/shadowsocks.pid`。
18. 使用ss-manager作为服务器管理工具：`ss-manager -c /etc/shadowsocks.json -u -f /var/run/shadowsocks.pid`。
19. 使用ss-nat作为NAT透明代理服务器：`ss-nat -s 0.0.0.0 -G 0.0.0.0 -l 1080 -u -f /var/run/shadowsocks.pid`。
20. 使用ss-pcap作为抓包工具：`ss-pcap -i eth0 -o packet.pcap -U -g 'dst port 80'`。

以上是SS工具的常用使用方法和实例，不同实例适用于不同的需求和场景。请根据自己的需求选择合适的命令进行操作。
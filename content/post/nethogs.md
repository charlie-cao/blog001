nethogs的使用方法
nethogs是一个Linux下用于监视每个进程的网络流量的工具。安装nethogs很简单，只需在CentOS中运行以下命令：

```
sudo yum install nethogs
```

安装完成后，以下是nethogs的常用使用方法：

1. 启动nethogs：在终端中输入以下命令即可启动nethogs：

   ```
   sudo nethogs
   ```

2. 监视指定网络接口：可以通过在启动nethogs时添加接口名称来指定要监视的网络接口，例如：

   ```
   sudo nethogs eth0
   ```

3. 显示流量数据：nethogs默认以实时模式显示网络流量。它会显示每个进程的发送和接收数据量，并按照流量从高到低进行排序。

4. 打开文件的监视：nethogs支持监视正在进行的文件传输，可以通过在启动nethogs时添加文件名来指定要监视的文件，例如：

   ```
   sudo nethogs /path/to/file
   ```

5. 显示DNS域名：nethogs默认只显示进程ID，但可以通过按' M '键来切换到显示进程的DNS域名。

6. 按进程ID过滤：可以通过在启动nethogs时添加进程ID来只显示特定进程的网络流量，例如：

   ```
   sudo nethogs -p 1234
   ```

7. 排除本地流量：默认情况下，nethogs监视所有流量，包括本地回环流量。可以通过在启动nethogs时添加'-v'参数来排除本地流量，例如：

   ```
   sudo nethogs -v 0
   ```

8. 指定刷新时间间隔：默认情况下，nethogs的刷新间隔为1秒。可以通过在启动nethogs时添加'-d'参数来指定刷新的时间间隔（单位为秒），例如：

   ```
   sudo nethogs -d 5
   ```

9. 帮助信息：可以通过在终端中输入以下命令来查看nethogs的帮助信息：

   ```
   sudo nethogs -h
   ```

10. 退出nethogs：在nethogs运行期间，按下'q'键即可退出。

这些是nethogs的一些常用使用方法，可以帮助你监视和分析网络流量。
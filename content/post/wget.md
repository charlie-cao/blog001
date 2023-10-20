wget的使用方法
wget是一个常用的命令行工具，用于从网络上下载文件。它支持HTTP、HTTPS和FTP协议，并且具有断点续传的功能。

常用的使用方法有：

1. 下载文件：wget [URL]，例如：wget https://example.com/file.zip。

2. 下载到指定文件名：wget -O [文件名] [URL]，例如：wget -O myfile.zip https://example.com/file.zip。

3. 后台下载文件：wget -b [URL]，下载过程会在后台运行。

4. 断点续传：如果下载中断，重新运行相同的wget命令，它会从中断的地方继续下载。

5. 限速下载：wget --limit-rate=[速度] [URL]，例如：wget --limit-rate=200k https://example.com/file.zip，限制下载速度为200KB/s。

6. 下载列表中的多个文件：将要下载的文件的URL保存在一个文件中，使用wget -i [文件名]命令下载。

7. 递归下载：wget -r [URL]，下载指定URL下的所有文件和子目录。

8. 忽略robots.txt文件：wget -e robots=off [URL]，默认情况下，wget会遵守网站的robots.txt文件，使用该选项可以忽略该文件。

9. 执行后续命令：下载完成后，可以指定执行一个指定的命令，例如：wget -O myfile.zip https://example.com/file.zip; echo 'Download finished!'。

10. 显示详细进度信息：wget --progress=bar:force [URL]，显示以进度条的形式下载的进度。

11. 限制重定向次数：wget --max-redirect=[次数] [URL]，限制重定向的最大次数。

12. 静默模式：wget -q [URL]，禁止任何输出。

13. 设置用户代理：wget --user-agent="[用户代理]" [URL]，设置HTTP头部中的User-Agent字段。

14. 下载网页中的所有媒体文件：wget -p -k -nd -H -e robots=off -A [文件类型] -R [排除文件类型] [URL]，这个命令会下载指定URL网页中的所有媒体文件，如图片、音频、视频等。

15. 防止服务器主机休眠：wget -c [URL]，如果服务器主机休眠，该选项会持续尝试连接。

16. 使用代理服务器：wget --proxy=on/off --proxy-user=[用户名] --proxy-password=[密码] [URL]，可以使用该命令来使用代理服务器下载文件。

17. 后台持续下载：wget --continue -b [URL]，即使在断开ssh连接后，也会继续在后台进行下载。

18. 验证下载文件的完整性：wget --content-disposition [URL]，可以验证文件的完整性并保存到正确的位置。

19. 下载完整的目录结构：wget --no-parent -r [URL]，下载指定URL下的所有子目录以及文件。

20. 解析robots.txt文件：使用wget -qO- [URL]/robots.txt命令可以查看一个网站的robots.txt文件的内容。

安装wget：在CentOS上，可以使用以下命令安装wget：

```
sudo yum install wget
```

这样就可以使用wget命令了。
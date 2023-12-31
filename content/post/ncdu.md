ncdu的使用方法
ncdu是一款用于查看磁盘空间使用情况的工具。它可以显示出文件和目录所占用的空间大小，并且可以帮助用户快速找到磁盘上占用空间较大的文件或目录。

使用方法如下：
1. 在CentOS中安装ncdu：在终端中运行命令 `sudo yum install ncdu` 进行安装。

常用实例：
1. 进入指定目录并运行ncdu命令：在终端中使用 `cd` 命令进入要查看的目录，然后运行 `ncdu` 命令即可。

2. 查看整个磁盘的空间使用情况：在终端中使用 `ncdu /` 命令来查看整个磁盘的空间使用情况。

3. 排序并只显示最大的几个文件或目录：在终端中使用 `ncdu -x` 命令可以显示每个目录的总大小，并按大小排序。使用 `ncdu -x -q -n 10` 命令可以只显示最大的10个文件或目录。

4. 以图形界面显示空间使用情况：在终端中使用 `ncdu --color=dark -rr -x` 命令可以以图形界面的方式显示空间使用情况。

5. 忽略指定的目录或文件：在终端中使用 `ncdu --exclude <dir/file>` 命令可以忽略指定的目录或文件。例如： `ncdu --exclude /tmp` 将会忽略/tmp目录的空间使用情况。

6. 导出报告到文件：在终端中使用 `ncdu -o <output_file>` 命令可以将空间使用情况导出到指定的文件中。例如： `ncdu -o report.txt` 将会将空间使用情况导出到report.txt文件中。

7. 查看特定目录或文件的空间使用情况：在终端中使用 `ncdu <directory/file>` 命令可以查看特定目录或文件的空间使用情况。

8. 显示空间使用情况的百分比：在终端中使用 `ncdu -P` 命令可以显示空间使用情况的百分比。

9. 运行ncdu后使用键盘操作导航：在ncdu界面中可以使用上下方向键来移动光标，使用左右方向键来展开或折叠目录，使用Enter键进入目录，使用Backspace键返回上级目录，使用q键退出ncdu。

10. 指定特定的目录树的深度：在终端中使用 `ncdu --depth <depth>` 命令可以指定要显示的目录树的深度。例如： `ncdu --depth 2` 将会只显示两级目录。

以上是部分常用的ncdu的使用方法和实例，希望对您有帮助。
sed的使用方法
sed是一个在Linux中非常常用的文本处理工具，可以用于对文本文件进行编辑、替换、删除等操作。下面是sed的一些常用使用方法和实例：

1. 替换文本中的字符串：
   `sed 's/old/new/' file.txt`：将文本文件file.txt中的所有old替换为new。

2. 替换文本中的字符串（只替换第一次出现的）：
   `sed 's/old/new/1' file.txt`：只替换文本文件file.txt中第一次出现的old。

3. 替换文本中的字符串（仅替换匹配到的行）：
   `sed '/pattern/s/old/new/' file.txt`：只替换匹配到pattern的行中的old。

4. 替换文本中的字符串（全局替换）：
   `sed 's/old/new/g' file.txt`：将文本文件file.txt中的所有old替换为new。

5. 删除匹配到的行：
   `sed '/pattern/d' file.txt`：删除文本文件file.txt中匹配到pattern的行。

6. 删除空白行：
   `sed '/^\s*$/d' file.txt`：删除文本文件file.txt中的空白行。

7. 插入新行：
   `sed '3i\new line' file.txt`：在第三行之前插入一行new line。

8. 在匹配到的行前插入新行：
   `sed '/pattern/i\new line' file.txt`：在匹配到pattern的行前插入一行new line。

9. 在匹配到的行后插入新行：
   `sed '/pattern/a\new line' file.txt`：在匹配到pattern的行后插入一行new line。

10. 打印匹配到的行：
    `sed -n '/pattern/p' file.txt`：只打印出匹配到pattern的行。

11. 打印指定行范围内的行：
    `sed -n '5,10p' file.txt`：打印出文件file.txt的第5到第10行。

12. 打印指定行号的行：
    `sed -n '5p' file.txt`：只打印出文件file.txt的第5行。

13. 使用正则表达式进行匹配：
    `sed -n '/^pattern/p' file.txt`：只打印出以pattern开头的行。

14. 将输出结果保存到新文件中：
    `sed 's/old/new/' file.txt > newfile.txt`：将替换结果保存到新文件newfile.txt。

15. 修改原文件（需要备份）：
    `sed -i.bak 's/old/new/' file.txt`：在替换的过程中备份原文件为file.txt.bak。

16. 忽略大小写：
    `sed 's/old/new/I' file.txt`：忽略大小写进行替换。

17. 执行多个编辑命令：
    `sed -e 's/old/new/' -e 's/pattern/replace/' file.txt`：执行多个编辑命令，分别替换文本中的old和pattern。

18. 只处理文件的部分内容：
    `sed '1,10d' file.txt`：删除文件file.txt的第1到第10行。

19. 指定文件的扩展名：
    `sed -i.bak 's/old/new/' *.txt`：在所有扩展名为txt的文件中替换old为new，并备份原文件。

20. 调用sed脚本文件：
    `sed -f script.sed file.txt`：根据script.sed中的脚本，对文件file.txt进行编辑。
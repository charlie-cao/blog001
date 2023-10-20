wc的使用方法
1. wc命令用于统计文本文件的行数、字数和字符数。
2. 基本语法：wc [选项] [文件]，选项可选，文件是要统计的文件列表。
3. 常用选项：
   -l 或 --lines: 输出行数。
   -w 或 --words: 输出字数。
   -c 或 --bytes: 输出字符数。
   -m 或 --chars: 输出字符数（和-c选项相同）。
   -L 或 --max-line-length: 输出最长行的长度。
   -s 或 --summarize: 输出文件总计行数、字数和字符数。
   -h 或 --help: 显示帮助信息。
4. 示例：
   - 统计文件的行数：wc -l file.txt
   - 统计文件的字数：wc -w file.txt
   - 统计文件的字符数：wc -c file.txt
   - 统计多个文件的行数、字数和字符数：wc -l -w -c file1.txt file2.txt
   - 输出文件总计行数、字数和字符数：wc -l -w -c -s file1.txt file2.txt
   - 输出最长行的长度：wc -L file.txt
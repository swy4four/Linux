# Linux （GNU/Linux）

# 常用

# 	根目录  cd /

# 	ctrl +c 强制停止

# ctrl+alt+t 打开终端

# ctrl+shift+Q w关闭

## 一 、步入Linux的世界

### 001.Linux四大组成部分

#### Linux操作系统 四个部分：

###### **1.Linux kernel 内核** (核心)  重点

###### **2.GNU工具 （最深的）****（开发  命令）

###### 3.GUI Desktop环境  （界面）

###### 4.Application 应用

### 002.Linux系统组成部分

​                                        GUI （界面）

###### **应用软件** 记事本  -->				|(上到下)						-->Linux内核 -->硬件 （键盘鼠标） 

​										GNU （命令）

### 003.Linux 内核组成部分  重点

###### Linux内核 ：

1. 硬件设备 管理使用 
2. 软件程序 （系统）------>操作软件
3. 系统内存管理
4. 文件管理  ---> 保存文件 删除文件  修改文件 。

### 004 文件系统

######  文件系统

###### 读写的标准 

不同文件系统 有不同的读写标准

###### 文件系统类型

Linux 支持的文件系统类型  ext ext2 ext3  ext4（通常使用） 等  

引导 （vfat）

Linux 分区   有不同的格式 

### 005 GNU核心 coreutils and shell

###### GNU 组织 

Unix 上具有的一些软件，Linux内核本身没有，所以GNU 他们模仿Unix，为Linux写了一些必要的软件

###### 1 、GNU核心

 原本在Unix上的一些命令和工具 被模仿（移植）到了Linux上 

供Linux 使用的这套工具 ：coreutils coreutilities 软件包



（1）用来处理文件的工具

（2） 用来操作文本的工具

（3）用来管理进程的工具

###### 2 shell （壳层）提供给用户使用的软件 ：用户拿他来使用电脑，并且和电脑交互

命令行壳层提供一个命令行界面（CLI）《核心》；而图形壳层提供一个图形用户界面（GUI） 



###### Linux shell ----〉CLI Command-Line Interface

### 006 Shell — CLI 和 GUI  重点

###### shell 一些介绍

bash shell 基础shell 

zsh （包含 下面 三个） MAC-〉Unix  专业人士选择

ash

korn

tcsh

### 007 Desktop—XW KDE GNOME Unity

###### GUI ：

1. X  Windows
2. KDE   windows  mac os
3. GNOME  红帽 
4.  Unity   ubuntu

## 二、Shell 命令

### 001.CLI准备

### 002.打开CLI终端

ya@fuck:~$ ^C

用户名 @机器名 ：当前 所在目录

~ 用户home目录

$ 等待用户输入....

### 003.Linux命令（常见）

简单的命令  **ls** 查看当前文件夹 

​					 **ls -a**  隐藏文件

​					**ll**  文件形式 缩写 

​			   	**cd**  切换目录 cd /正斜线  Linux   根目录

​											\反斜线    windows

$  ls          # 仅列出当前目录可见文件
$  ls -l       # 列出当前目录可见文件详细信息
$  ls -hl     # 列出详细信息并以可读大小显示文件大小
$  ls -al     # 列出所有文件（包括隐藏）的详细信息
$  ls --human-readable --size -1 -S --classify    # 按文件大小排序
$  du -sh * | sort -h          # 按文件大小排序(同上)



网站 [Linux命令搜索引擎 命令，Linux Linux命令搜索引擎 命令详解：最专业的Linux命令大全，内容包含Linux命令手册、详解、学习，值得收藏的Linux命令速查手册。 - Linux 命令搜索引擎 (wangchujiang.com)](https://wangchujiang.com/linux-command/)





###### **练习** 

### 004 Linux 根目录

###### **cd**  切换目录 cd /   根目录



cd / 

ls

查看根目录

### 005 Linux根目录解析

## **基本目录解释

##### / ：根目录 ，所有目录的最顶层目录，从任何用户执行该命令都会进入同一个目录，即所有用户共享。

##### /home：/下面的home目录，名为家目录，但是很多人叫为用户列表目录，因为/home下是这台机器的用户名。

##### ~目录：当前用户的家目录

##### 在root用户下，~就代表/root。

##### 在普通用户目录下，~就代表/home/普通用户名

![](F:\Note\photo\Snipaste_2023-09-13_16-09-16.png)

###### 根目录

**/bin**   二进制目录 GNU工具 ls等系统自带的命令   存放许多用户级

**/usr** 用户二进制目录 ，GNU工具

**/sbin** 系统二进制目录 GNU高级管理员使用的命令工具

**cd ..**   返回上一目录 

**/cdrom** 光盘

**/etc** 系统配置文件

#### **/home** 主目录 显示 所有用户目录

**/lib** 库目录 存放依赖的文件 

**/mnt** 挂载目录 外在设备 与电脑进行连接

**/proc** 伪文件系统

**/run** 运行目录 

**/snap** 

**/tep** 临时目录 （temp）

**/var** 可变目录 

**/boot** 启动目录

**/dev** 设备目录

**/media** 媒体目录

**/opt** 可选目录

**/root** root 用户的主目录 管理员

**/pwd**显示当前目录

*sudo rm -rf /* 删库命令** 



**/srv** 服务目录 本地服务



**FHS 文件系统层级标准**



### 006cd命令

######  cd 回到最初目录

### 007 Ctrl+c 在Linux上 

强制退出

复制 Ctrl Shift c

撤销  无概念 可通过

### 008 绝对路径

###### 绝对路径 全路径 

###### 相对路径 不全  一部分下的路径

###   010 Linux上的路径

######    **绝对路径** /

######  相对路径 无/    ./ 或者 ~/

gedit ~/Desktop/1.txt    绝对路径

gedit ./Desktop/1.txt     相对路径

gedit Desktop/1.txt		相对路径

**绝对路径**也可称完整路径，是指向文件系统中某个固定位置的路径，不会因当前的[工作目录](https://zh.wikipedia.org/wiki/工作目錄)而产生变化。为做到这点，它必须包括[根目录](https://zh.wikipedia.org/wiki/根目录)。

**相对路径**则是以指定的工作目录作为基点，避开提供完整的绝对路径。[文件名称](https://zh.wikipedia.org/wiki/檔案名稱)就可以被视为以指定工作目录为基点的一个相对路径（虽然一般不将其称之为路径）。

### 011 练习

###### 单点符.当前文件夹

###### 双点符 ..当前目录的父目录

ya@fuck:~$ cd .
ya@fuck:~$ cd ..
ya@fuck:/home$ cd
ya@fuck:~$ 



cd  路径 

ls 查看文件夹

### 012 进阶用法 文件夹下

###### ya@fuck:~$ ls  Pictures -F -R 

Pictures:
photo/

Pictures/photo:
nothing/



###### **文件扩展匹配符** 

？   * 

###### **元字符通配符**

[ ] 

### *013 touch

######  创建 文件

### 014 cp

###### copy

具体文件 

具体文件 绝对或相对路径 

绝对或相对路径  绝对或相对路径 

###### 文件对文件 文件对目录 目录对文件 目录对目录

 既可以复制文件也可以复制文件夹

没有复制的文件 就会创建

会覆盖文件内容

##### 谨慎使用

cp **-i** 1.txt 2.txt 

**ya@fuck:~/Documents$ cp -i 1.txt 2.txt**



###### 把文件夹连同内容都复制进去 cp -r

连同文件夹 -r

ya@fuck:~/Documents$ **cp -r  /home/ya/Documents/photo/ /home/ya/Downloads/**

-r 遍历

###### 仅复制目标文件夹中的内容 cp /绝对路径（相对路径）/ * /绝对路径（相对路径）/

ya@fuck:~/Documents$ **cp /home/ya/Documents/photo/* /home/ya/Downloads**

 例子是绝对路径 也可以是相对路径

###### 直接复制到文件夹中（相对路径）

ya@fuck:~/Documents$ cp -i 1.txt ~/Downloads/

###### 复制到上一层 cp 文件名 ../

ya@fuck:~/Documents/photo$ cp fuck1.txt ../

##### 将一个文件夹中的文件 复制到当前文件夹中  

ya@fuck:~/Documents$ cd pdf
ya@fuck:~/Documents/pdf$ **cp ../photo/* .**

### 015 练习

pwd : 输出当前目录的绝对路径

###### 在 home 中 把一个文件夹中的 文件 拷贝到 另一文件中

ya@fuck:~/Project$ cp -R ./*.py ~/Documents//temp/



##### cd - 返回到 上一次的目录

### 016 终端光标移动技巧

###### TAb 键 快速写入

ctrl l 向上移动一个制表符

ctrl b 光标向前

ctrl t 移动光标所在的字母

ctrl u 删除光标前的内容

### 017lnk 链接文件

##### 1.符号链接（软链接）Symbolic links (soft links)——快捷方式 3rws

原来的文件或者文件夹 必须是存在的

不同存储介质 只能使用软链接

##### 2.硬链接 

###### 创建副本 

原来的文件/文件夹 必须是存在的

范围小  

##### 只能在同一个文件系统中才能创建

##### 不能给目录创建

ln为文件创建链接，链接类型分为硬链接和符号链接两种，默认的链接类型是硬链接。如果要创建符号链接必须使用"-s"选项。

注意：符号链接文件不是一个独立的文件，它的许多属性依赖于源文件，所以给符号链接文件设置存取权限是没有意义的。

## 018 符号链接和硬链接

#### 软链接（命令行）

ln -s 1.py 1_linkfile

###### 是一个单独的文件

原文件 大小 0

软链接 大小 6

硬链接 0

#### 硬链接

ln  1.py 2_linkfile

#### 注意事项

cp 命令 复制一个文件 是一个链接文价 是什么结果 

## 020.mv重命名

move 

可以移动亦可以重命名 

ya@fuck:~/Project$ mv 1-linkfile  4.py 

##### 重命名 mv + 文件名 + 新名字

###### cd !$ 执行上一条命令的最后一条路径

##### 移动 

##### ya@fuck:~/Documents$ mv 2.txt ~/Documents/pdf

## 021.rm Linux 最危险的命令之一

### 谨慎使用

removing  rm 

#### sudo rm -rf /*  

#### /* 根目录 删除

###### ya@fuck:~/Documents/pdf$ rm -rf jack

删除 Documents 下 pdf 中的 jack -rf 遍历删除

##### rm **-i** text.c 

会有 确定删除 的选项

##### 语法

###### rm (选项)(参数)

-d：直接把欲删除的目录的硬连接数据删除成0，删除该目录；
-f：强制删除文件或目录；
-i：删除已有文件或目录之前先询问用户；
-r或-R：递归处理，将指定目录下的所有文件与子目录一并处理；
--preserve-root：不对根目录进行递归操作；
-v：显示指令的详细执行过程。

## 022.创建文件夹以及删除文件夹

#### 目录 （文件夹）

make directories 

####  mkdir 

ya@fuck:~/Documents/temp$ mkdir python

在 temp 中创建 python 目录

##### 语法

mkdir (选项)(参数)

##### 选项

-Z：设置安全上下文，当使用SELinux时有效；
-m<目标属性>或--mode<目标属性>建立目录的同时设置目录的权限；
-p或--parents 若所要建立目录的上层目录目前尚未建立，则会一并建立上层目录；
--version 显示版本信息。

###  参数

目录：指定要创建的目录列表，多个目录之间用空格隔开



###### 复制temp中 后缀是.py的文件 到 temp中 python

###### 目录下 然后删除掉temp 中.py 后缀的文件

###### 用来达到把文件迁移的目的

ya@fuck:~/Documents/temp$ cp ./*.py ~/Documents/temp/python
ya@fuck:~/Documents/temp$ cd !$
cd ~/Documents/temp/python
ya@fuck:~/Documents/temp/python$ ls
1.py  2.py  3.py
ya@fuck:~/Documents/temp/python$ cd ..
ya@fuck:~/Documents/temp$ rm -i ./*.py

## 023 文件类型

##### file 查看文件类型

##### file Project 查看文件夹

#### 语法

file(选项)(参数)

#### 选项

-b：列出辨识结果时，不显示文件名称；
-c：详细显示指令执行过程，便于排错或分析程序执行的情形；
-f<名称文件>：指定名称文件，其内容有一个或多个文件名称时，让file依序辨识这些文件，格式为每列一个文件名称；
-L：直接显示符号连接所指向的文件类别；
-m<魔法数字文件>：指定魔法数字文件；
-v：显示版本信息；
-z：尝试去解读压缩文件的内容。



## 024. cat more less 查看文件类型

##### cat 短的文件

###### cat -A 全部显示 

cat -n 带行号 不实用

##### more 分屏上下翻页浏览文件内容

- 按 `Space` 键：显示文本的下一屏内容。

- 按 `Enter` 键：只显示文本的下一行内容。

- 按斜线符`|`：接着输入一个模式，可以在文本中寻找下一个相匹配的模式。

- 按H键：显示帮助屏，该屏上有相关的帮助信息。

- 按B键：显示上一屏内容。

- 按Q键：退出more命令。

  ##### 选项

-<数字>：指定每屏显示的行数；
-d：显示“[press space to continue,'q' to quit.]”和“[Press 'h' for instructions]”；
-c：不进行滚屏操作。每次刷新这个屏幕；
-s：将多个空行压缩成一行显示；
-u：禁止下划线；
+<数字>：从指定数字的行开始显示。

#### less(选项)(参数) 最实用 pgup pgdn

##### 选项

-e：文件内容显示完毕后，自动退出；
-f：强制显示文件；
-g：不加亮显示搜索到的所有关键词，仅显示当前显示的关键字，以提高显示速度；
-l：搜索时忽略大小写的差异；
-N：每一行行首显示行号；
-s：将连续多个空行压缩成一行显示；
-S：在单行显示较长的内容，而不换行显示；
-x<数字>：将TAB字符显示为指定个数的空格字符。

##### less

### 025. tail 和 head

#### **tail命令** 用于输入文件中的尾部内容。

- 默认在屏幕上显示指定文件的末尾10行。

- 处理多个文件时会在各个文件之前附加含有文件名的行。

- 如果没有指定文件或者文件名为`-`，则读取标准输入。

- 如果表示字节或行数的`NUM`值之前有一个`+`号，则从文件开头的第`NUM`项开始显示，而不是显示文件的最后`NUM`项。

- ```
  NUM
  ```

  值后面可以有后缀：

  - `b` : 512
  - `kB` : 1000
  - `k `: 1024
  - `MB` : 1000 * 1000
  - `M `: 1024 * 1024
  - `GB` : 1000 * 1000 * 1000
  - `G `: 1024 * 1024 * 1024
  - `T`、`P`、`E`、`Z`、`Y`等以此类推

- 

  ###### tail -n 2 demo.c

  显示后两行

##### 实例

tail file #（显示文件file的最后10行）
tail -n +20 file #（显示文件file的内容，从第20行至文件末尾）
tail -c 10 file #（显示文件file的最后10个字节）

tail -25 mail.log # 显示 mail.log 最后的 25 行
tail -f mail.log # 等同于--follow=descriptor，根据文件描述符进行追踪，当文件改名或被删除，追踪停止
tail -F mail.log # 等同于--follow=name --retry，根据文件名进行追踪，并保持重试，即该文件被删除或改名后，如果再次创建相同的文件名，会继续追踪

#### head 显示前十行



## 三 .系统上的shell

### 001.认识任务管理器

ps  当前在终端干的事情 报告当前系统状态

PID 号  

##### ps -aux | grep named # 查看named进程详细信息

 kill  pid 

kill 6222 

kill  -9 强制执行 

#### 进程 ps 会有用

top 



#### 004.挂载

#### sudo fdisk -l  显示出当前使用

![](F:\Note\photo\挂载u盘位置.png)

 真实挂载位置 /dev/sdb1

##### 挂载到 sudo mount /dev/sdb1 /mnt 

![](F:\Note\photo\挂载到mnt目录下.png)

##### umount 删除挂载

sudo umount /mnt

![](F:\Note\photo\删除挂载点.png)



### 007 df和du

##### 不能将目录挂载到目录 应该将分区挂载到目录

##### df

以挂载的

用于显示磁盘分区上的可使用的磁盘空间。

![](F:\Note\photo\df.png)

##### du -h 

查看文件夹 使用情况

 

### 008.sort文件排序

#### sort 对文本文件中所有行进行排序。

##### 选项

```
	-b, --ignore-leading-blanks    忽略开头的空白。
	-d, --dictionary-order         仅考虑空白、字母、数字。
	-f, --ignore-case              将小写字母作为大写字母考虑。
	-g, --general-numeric-sort     根据数字排序。
	-i, --ignore-nonprinting       排除不可打印字符。
	-M, --month-sort               按照非月份、一月、十二月的顺序排序。*
	-h, --human-numeric-sort       根据存储容量排序(注意使用大写字母，例如：2K 1G)。
	-n, --numeric-sort             根据数字排序。
	-R, --random-sort              随机排序，但分组相同的行。
	--random-source=FILE           从FILE中获取随机长度的字节。
	-r, --reverse                  将结果倒序排列。
	--sort=WORD                    根据WORD排序，其中: general-numeric 等价于 -g，human-num
	                               eric 等价于 -h，month 等价于 -M，numeric 等价于 -n，random
                                   等价于 -R，version 等价于 -V。
	-V, --version-sort             文本中(版本)数字的自然排序。
```

![](F:\Note\photo\两个命令合并.png)

### 009.grep基础认识，搜索文件

#### grep [要搜索文件中字符] 文件路径

![](F:\Note\photo\grep 遍历搜索01.png)

### [grep介绍](https://wangchujiang.com/linux-command/c/grep.html)

### 010.打包压缩归档解压缩

gzip .gz 

.zip 

bzip2 .bz2

.tar.gz 打包 后压缩

linux 只能压缩一个文件 所以先打包在压缩 

- ### [tar介绍](https://wangchujiang.com/linux-command/c/tar.html)注：c参数代表create（创建），x参数代表extract（解包），v参数代表verbose（详细信息），f参数代表filename（文件名），所以f后必须接文件名。

- `tar -cvf log.tar log2012.log    仅打包，不压缩！`

- `tar -zcvf log.tar.gz log2012.log   打包后，以 gzip 压缩`

- `tar -jcvf log.tar.bz2 log2012.log  打包后，以 bzip2 压缩`

#### 实例

- z：有gzip属性的
- j：有bz2属性的
- Z：有compress属性的
- v：显示所有过程
- O：将文件解开到标准输出

`tar -cf archive.tar foo bar  # 从文件 foo 和 bar 创建归档文件 archive.tar。`
`tar -tvf archive.tar         # 详细列举归档文件 archive.tar 中的所有文件。`
`tar -xf archive.tar          # 展开归档文件 archive.tar 中的所有文件。`

下面的参数-f是必须的

-f: 使用档案名字，切记，这个参数是最后一个参数，后面只能接档案名。

```shell
tar -cf all.tar *.jpg
# 这条命令是将所有.jpg的文件打成一个名为all.tar的包。-c是表示产生新的包，-f指定包的文件名。

tar -rf all.tar *.gif
# 这条命令是将所有.gif的文件增加到all.tar的包里面去。-r是表示增加文件的意思。

tar -uf all.tar logo.gif
# 这条命令是更新原来tar包all.tar中logo.gif文件，-u是表示更新文件的意思。

tar -tf all.tar
# 这条命令是列出all.tar包中所有文件，-t是列出文件的意思
tar -cvf archive.tar foo bar  # 从文件foo和bar创建archive.tar。
tar -tvf archive.tar         # 详细列出archive.tar中的所有文件。
tar -xf archive.tar          # 从archive.tar提取所有文件。
```

### 解压缩

#### .tar.gz 格式

方式一：利用前面已经打包好的tar文件，直接用压缩命令。

压缩：gzip [原文件名].tar
解压：gunzip [原文件名].tar.gz

方式二：一次性打包并压缩、解压并解包

打包并压缩： tar -zcvf [目标文件名].tar.gz [原文件名/目录名]
解压并解包： tar -zxvf [原文件名].tar.gz
注：z代表用gzip算法来压缩/解压。

#### tar格式（该格式仅仅打包，不压缩）

打包：tar -cvf [目标文件名].tar [原文件名/目录名]
解包：tar -xvf [原文件名].tar
注：c参数代表create（创建），x参数代表extract（解包），v参数代表verbose（详细信息），f参数代表filename（文件名），所以f后必须接文件名。

##### 打包并压缩

![](F:\Note\photo\打包并压缩.png)

##### 解压并解包

![](F:\Note\photo\解压缩tar.gz.png)

## 四.父子shell

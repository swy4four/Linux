# Linux
# Linux （GNU/Linux）

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
4. Unity   ubuntu

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

### 004 Linxu 根目录

###### **cd**  切换目录 cd /   根目录



cd / 

ls

查看根目录

### 005 Linux根目录解析

###### 根目录

**/bin**   二进制目录 GNU工具 ls等系统自带的命令   存放许多用户级

**/usr** 用户二进制目录 ，GNU工具

**/sbin** 系统二进制目录 GNU高级管理员使用的命令工具

**cd ..**   返回上一目录 

**/cdrom** 光盘

**/etc** 系统配置文件

**/home** 主目录 显示 所有用户目录

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

### 013 touch

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

### 016

###### TAb 键 快速写入

ctrl l 向上移动一个制表符

ctrl b 光标向前

ctrl t 移动光标所在的字母

ctrl u 删除光标前的内容


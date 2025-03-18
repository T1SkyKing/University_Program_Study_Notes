# Linux 复习

## 配置 Linux 环境

首先应自行搭建**VMware**虚拟机环境，再将基于 Linux 开发的 Ubuntu 操作系统安装在虚拟机中，得以运行。

<!-- 如何给显示中的代码添加行号？ -->
<!-- ```的用法 -->
<!-- 注释快捷键：ctrl + / -->

<!-- 在需要输入Linux命令时则需要bash -->
<!-- 但在输出时并不会有颜色变化，因为本来就没有颜色变化 -->

## [<font color = "grey">Linux 常用命令</font>](https://blog.csdn.net/wzk4869/article/details/132855372)

```bash
vim test.c
```

创建一个名字为 test 的 c 文件，并进入文件内进行编辑

当显示
`"test.c" 16L, 168B`则进入选择状态
按下`i`则进入输入修改编辑模式，此时显示
`-- 插入 --`

修改完成后按下 Esc 键，并输入`:wq`则保存并退出

```bash
gcc test.c -o t
```

对 test.c 文件进行编译，并输出了一个名为 t 的可执行文件

`-o t` 这个选项是指定输出文件的名称

`-o`后面跟的是要生成的可执行文件的名称。在这里，生成的文件名是 t，没有文件扩展名。

```bash
./t
```

编译成功后运行可执行文件 `./文件编译输出名`

---

## C 语言基础复习

### 数据类型

### 变量

### 输入输出函数

### 三大函数结构

### 函数

### 数组

### 指针

### 结构体

### 枚举

### 动态内存管理

### 线性表

<!-- 在 Linux 环境下编写 c 代码:

```c {.line-numbers}
#include <stdio.h>
int main() {
	int h = 0;
	while (h < 4) {

		int a = 1;v

		while (a <= (2 * h + 1)) {
			printf("*");
			a += 1;
		}
		h += 1;
		printf("\n");
	}
}
``` -->

## Linux 基础复习

### Linux 常用命令

```bash
sky@sky-virtual-machine:~$    //命令行提示符
	sky: 用户名
	@: 间隔符
	sky-virtual-machine: 主机名
	: 分隔符
	~: 工作目录
	$:普通用户
	#: 超级用户
pwd		#查看当前路径
ls		#显示当前路径下的所有文件
sudo su		#切换为超级用户
su 用户名	#切换为普通用户
cd 		#跳转到工作目录
.  		#当前路径
..		#上级路径
cd ..		#绝对路径:从根目录开始的路径:/home/linux
cd + 路径	#相对路径:相对当前位置而言的路径

touch + 文件名			#创建文件
mkdir  + 文件名			#创建文件夹
rm + 文件名  			#删除普通文件
rm -r +文件名  			#删除文件夹
cp 文件名 			#要拷贝到的路径  拷贝文件
cp -r 文件夹名 			#要拷贝到的路径
mv 要移动的文件	要移动到的文件	#移动文件
mv 旧文件 新文件 		#新文件不存在表示重命名
mv 1.c test
vim +文件名   	#创建并打开文件
# 命令行模式---i--->编辑模式
# 命令行模式------->底行模式  按shift+;输出:
# 底行模式/编辑模式----->命令行模式 按esc

# 命令行模式下:
	yy	#复制
	nyy	#复制n行
	p	#粘贴
	dd	#剪切
	ndd	#剪切n行
	U	#撤销
	ctrl+r	#反撤销
# 底行模式:
	:w		#保存
	:q		#退出
	:wq		#保存并退出
	:set nu		#显示行号
	:set nonu	#隐藏行号
	# 快捷方式: ctrl shift 加+表示放大终端
	# ctrl + l （clear） 清屏
```

`ls -l`

```bash
drwxrwxr-x 2 sky sky 4096 11 月 21 22:44 Test
-rw-rw-r-- 1 sky sky 72 11 月 10 09:58 test1.c
-rwxrwxr-x 1 sky sky 60 11 月 10 10:01 test1.sh
#          用户
#0 000 000 000
#- rw- rw- r--
#-表示是文件/d表示是文件夹（含有地址）
#rwx r代表可读 w代表可写 x代表可执行 -代表无这个权限(0)
```

### [<font color = "grey">Linux Ubuntu 22.04 使用技巧 | 解决开机卡在 /dev/sda3 : clean , **_files , _**blocks Ubuntu 日志文件 var/log/syslog 占满空间导致死机</font>](https://blog.csdn.net/zhangqian_shai/article/details/123948452)

进入[Grub 模式](https://blog.csdn.net/SunshineLiy/article/details/134372529)：
在开启虚拟机时，显示到启动界面时快速按下 Shift 键不要松，直到出现 Grub 界面

通过以下代码查看根目录下所有文件和目录的磁盘使用情况：

```bash
du -sh /*
```

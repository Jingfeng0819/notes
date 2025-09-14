### 基本命令

##### Linux常见目录介绍

- **/**：根目录
- **/bin**：可执行的二进制文件
- **/boot**：放置linux系统启动时用到的一些文件
- **/dev**：存放linux系统下的设备文件
- **/etc**：系统配置文件存放的目录
- **/home**：系统默认的家目录
- **/lib**：系统使用的函数库目录
- **/media和/mnt**：光盘默认挂载点
- **/opt**：安装第三方软件所需的默认目录
- **/proc**：此目录的数据都在内存中(不占用磁盘空间)，如系统核心、外部设备等
- **/root**：系统管理员的家目录
- **/sbin**：放置给系统管理员root使用的命令
- **/srv**：服务器启动之后需要访问的数据目录，如www服务需要访问的网页数据存放在/srv/www内
- **/var**：放置系统执行过程中经常变化的文件，如随时更改的日志文件、邮件；

##### Bash解析器常用快捷键

- **Tab键**：补齐命令、补齐路径、显示当前目录下的所有目录
- **中断进程**：ctrl+c
- **光标瞬移**：ctrl+a移动到光标头部，ctrl+e移动到光标尾部
- **字符删除**：ctrl+u删除光标前所有内容，ctrl+k删除光标后所有内容

##### 终端相关快捷键

- Ctrl+Shift+N：新建一个终端
- Ctrl+Shift+T：在终端里新建一个标签
- Ctrl+Shift+W：关闭标签页
- Ctrl+Shift+Q：关闭窗口
- Ctrl+Shift+C：复制
- Ctrl+Shift+V：粘贴
- Alt+[1-9]：终端标签页的切换
- Ctrl+D：关闭一个终端
- Alt+F4：关闭全部终端

##### 相对路径和绝对路径

**绝对路径**：

- 绝对路径是从目录树的树根“/”目录开始往下直至到达文件所经过的所有节点目录
- 下级目录接在上级目录后面用“/”隔开
- 绝对路径都是从“/”开始的，所以第一个字符一定是“/”；

**相对路径**：

- 相对路径是指目标目录相对于当前目录的位置
- 目录 . 指向当前目录，而 .. 指向当前目录的上一级

##### 目录相关的命令

###### pwd

打印当前所在目录的名字

###### cd

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683713604263-a007a098-db0f-458e-9307-2737f6232d64.png)

###### mkdir

mkdir用于创建一个空目录（不是新建普通文件）

用法：mkdir+选项+目录

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683713866707-3dc85ad1-b37b-46c0-9ed6-173122944b9e.png)

###### rmdir

删除指定的**空**目录，而且必须离开当前的目录；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683715042357-c8a7d1b4-b365-49bb-b28c-878ce63e1165.png)

##### Linux文件类型

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683717240160-b746eee1-3386-4e90-94b1-2ed0392493d0.png)

在Linux系统中，文件类型可以分为以下几类：

1.  普通文件 (regular file)：包括文本文件、二进制文件和数据文件。 
2.  目录 (directory)：用于组织文件和子目录。 
3.  符号链接 (symbolic link)：指向另一个文件的链接。 
4.  块设备文件 (block special file)：与设备进行交互，如硬盘和 CD-ROM。 
5.  字符设备文件 (character special file)：使用字符流与设备进行交互，如键盘和鼠标。 
6.  套接字 (socket)：用于网络编程。 
7.  管道 (named pipe)：用于进程间通信。  

使用命令“ls -l”可以查看文件类型。输出的第一列中，第一个字符表示文件类型，例如“-”表示普通文件，“d”表示目录，“l”表示符号链接，“b”表示块设备文件，“c”表示字符设备文件，“s”表示套接字，“p”表示管道。

##### 文件相关命令

###### ls

ls是英文单词list的简写，其功能为列出目录的内容

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683718219501-7db1d327-1465-4db2-97aa-2d8929b40fb6.png)

###### touch

用于创建普通文件

1. 如果文件不存在则创建普通文件
2. 如果文件存在，则更新文件时间

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683719420085-f893401d-5840-4839-a3d7-7bf406716b6b.png)

###### cp(拷贝)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683719480238-9f2e40a5-ae8c-4953-9bf8-4ac6df13d9bd.png)

###### rm

可以用于删除文件或目录

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683720760238-de03f88b-9fd5-4b94-8995-49b0b2dda10d.png)

###### mv

用于移动文件或目录，也可以给文件或目录重命名

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683721409100-79f2dc75-022e-4a12-82e3-ef861d6dcd8a.png)

##### 文件内容查看命令

###### cat

cat将文件内容一次性输出到终端

缺点是当文件太长则无法显示全部

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683789091242-4621e6b8-8b0b-44bc-9bb9-30a9f5fc8f97.png)

###### less

less命令将文件内容分页显示到终端，可以自由地上下切换

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683789601858-5668c394-5ff8-4da3-a344-5ca125abf4a3.png)

###### head

head -n[行数] 文件名

head命令从文件头部开始查看前n行的内容

如果没有指定行数，默认显示前10行的内容

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683789899119-23d84ae1-879c-48be-a61c-130741917a74.png)

###### tail

- 从文件尾部向上查看最后n行的内容
- 使用方式：tail -n[行数] 文件名
- 如果没有指定行数 默认显示最后10行的内容

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683790125511-53dd17b8-1d09-4286-bd64-f136671f72ff.png)

###### du和df

du -sh 文件名：查看文件所占磁盘空间大小

df -h ：查看所有磁盘分区占用情况

##### 查找相关命令

###### find

通常用于特定的目录下搜索符合条件的文件，也可以用来搜索特定用户属主的文件

**按文件名查询**：

命令：find + 路径 + -name + "文件名"

示例：find ./ -name test                  //在当前目录寻找test文件



**按文件大小查询**：

命令：find + 路径 + -size + 范围(+是大于，-是小于)

示例：find ./ -size +100k                //在当前目录寻找大于100k的文件



**按文件类型查询**：

命令：find + 路径 + -type + 类型

d：目录

b：块

l：链接

p：管道

-：普通文件(用f表示，而不是 - )

c：设备文件

s：socker，网络套接字

###### grep

find主要用于查找文件，而grep用于在某个位置查找指定的字符

语法：grep -r “字符”路径

##### 压缩包管理

###### tar打包

tar是Linux中最常用的备份工具，此命令可以把一系列文件归档到一个大文件中，也可以把归档文件解开已恢复数据

**语法**：tar  [参数]  打包后的文件名  要打包的文件

**示例**：tar  -cvf  testfile  test1.txt  test2.txt test3.txt； 将这三个文本文件生成一个归档文件testfile 

**常用**：

tar -cvf：创建归档文件并显示进度

tar -xvf：接触归档文件(还原)并显示进度

tar -tvf：查看档案中包含的文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683794771327-399b3671-90bc-4dff-9597-ee14e532e1e4.png)

###### gzip压缩

- tar与gzip结合使用才能实现打包、压缩
- tar只负责打包文件，但不压缩，用gzip打包后的文件 其扩展名一般用xxx.tar.gz
- **语法**：gizp [选项] 被压缩文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683796145872-376697f6-13b2-4544-a8f3-93fd0753d43e.png)



在Linux中，gzip命令可以压缩文件和目录，但**它只能压缩目录中的文件，并不能直接压缩整个目录**。当你使用gzip压缩目录时，它会一次性压缩目录中的所有文件，并将它们存储到单个压缩文件中。

如果你想要压缩整个目录（包括子目录），可以考虑使用tar命令将目录打包，然后再使用gzip进行压缩。具体操作如下：

压缩整个目录：

```shell
 tar cvzf compressed.tar.gz directory/
```

解压目录：

```plain
tar xvzf compressed.tar.gz
```

解压到指定目录：

```shell
tar xvzf compressed.tar.gz -C /temp
```

上述命令中，`tar`命令用于打包文件和目录，`z`选项指定压缩格式为gzip，`c`选项表示压缩，`x`选项表示解压缩，`v`选项表示在打包或解包的过程中显示进度和详细信息。

需要注意的是，使用`gzip`命令压缩大型目录时可能会导致压缩时间较长，并且会给系统带来一定的负担。因此，在压缩较大的目录时，最好使用`tar`命令打包后再进行压缩。

###### bzip2

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1683798122628-3df6a790-398b-4e06-b2df-197f110302f2.png)

bzip2与gzip功能相同，都是与tar结合使用；

bizp是-j，gzip是-z

小文件用gzip，大文件用bzip

###### zip和unzip

压缩：zip  huifile  hui1.txt  hui2.txt  hui3.txt

解压：unzip  huifile

###### 三种压缩方式的选择

`gzip`，`zip`和`bzip2`都是在Linux系统中常见的文件压缩格式，它们使用不同的算法和方法压缩文件，选择哪种格式取决于你想要实现的目标，如压缩比、速度和系统资源的占用等。以下是对三种格式的简介和比较：

1.  `gzip`：使用Lempel-Ziv算法和哈夫曼编码算法，压缩速度快，压缩比较高，**适用于较小的文件**或数据流。由于压缩和解压缩速度较快，因此经常被用作文件传输和备份。文件扩展名为`.gz`
2.  `zip`：使用LZ77算法和哈夫曼编码算法，**适用于较大或结构复杂的文件**和目录，压缩速度较慢，但压缩比较好。在Windows和Mac OS X系统中，zip格式已成为标准压缩格式。文件扩展名为`.zip`
3.  `bzip2`：使用Burrows-Wheeler变换和霍夫曼编码算法，具有更高的压缩比，但是压缩速度比`gzip`和`zip`慢。**适用于需要更高压缩比的大型文件**和数据集的压缩和备份。文件扩展名为`.bz2`



##### 文件权限管理

###### 访问用户分类

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684027696838-a402fe7b-c4da-472d-a21b-4ada68891eb8.png)

###### chmod

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684028017447-317b8ada-3cad-41d2-9ce1-ea1105b99d4f.png)

**示例1**：给其他用户添加了可写权限(chmod o+w 文件名)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684028239136-c687ce04-1c7f-4f1e-9310-7b4bb0bae6ad.png)

**示例2**：撤销用户所有组的可写权限(chmod g-w 文件名)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684028417302-a49498ec-7820-4c17-aa6b-7d9f5a23304e.png)

**示例3**：将所有者的权限设为读写，所有组和其他用户只能读

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684028683876-15c609b9-7dfe-46ca-9a11-fcddf87ef7b5.png)

##### 软连接和硬连接

[https://blog.csdn.net/q610098308/article/details/104389596?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522168403141016800197078961%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=168403141016800197078961&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-104389596-null-null.142^v87^control_2,239^v2^insert_chatgpt&utm_term=linux%E8%BD%AF%E8%BF%9E%E6%8E%A5%E5%92%8C%E7%A1%AC%E8%BF%9E%E6%8E%A5&spm=1018.2226.3001.4187](https://blog.csdn.net/q610098308/article/details/104389596?ops_request_misc=%7B%22request%5Fid%22%3A%22168403141016800197078961%22%2C%22scm%22%3A%2220140713.130102334..%22%7D&request_id=168403141016800197078961&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-104389596-null-null.142^v87^control_2,239^v2^insert_chatgpt&utm_term=linux软连接和硬连接&spm=1018.2226.3001.4187)

### Linux下编写程序

##### vim编辑器工作模式

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684044725158-e6938bdf-5013-45c2-8ae5-81257b32a73b.png)

###### 命令模式

任何时候，不管用户处于何种模式，只要按下ESC键 即可进入命令模式；我们在shell环境下输入vim命令进入编辑器时，也是处于该模式下

###### 编辑模式

在命令模式下输入命令i（I）、附加命令a（A）、打开命令o（O）、替换命令s（S）都可以进入文本输入模式，此时vi窗口的最后一行会显示"插入"；

###### 末行模式

末行模式下，用户可以对文件进行一些附加处理，如：字符串查找、替换、显示行号等；

在命令模式下输入冒号即可进入末行模式，用户输完命令后按回车执行，之后vi编辑器又自动返回到命令模式下；

##### vim实用操作

###### 命令模式下的操作

1. 切换到编辑模式

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684045974978-b1a390d3-7fed-4e46-952b-d5d8ea15f0a5.png)

1. 光标移动

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684046348695-05371e96-72e9-49e9-bdf8-4a880b694713.png)

1. 复制粘贴

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684046517591-55d51af9-afc8-49d4-b029-71bb3ca706c4.png)

1. 删除

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684046663583-0e4d9d0b-afb2-4e86-84bc-4997df1f6114.png)

1. 撤销恢复

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684046822852-d3072fc4-1463-455f-9d4f-64f069f35e1f.png)、

1. 可视模式

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684047228733-28bbc447-5421-4890-9d3f-6c3287fbe8d7.png)

###### 末行模式下的操作 

1. 保存退出

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684047284904-596b8eac-22e9-4616-9c2b-10b55026ff4b.png)

1. 替换

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684047486525-b3fb09cb-dd90-4210-b1c9-b410437efdcf.png)

1. 分屏

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684047719810-239a36d9-9981-4c9f-8e52-f4a500c76798.png)

1. 其他用法

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684047806523-040970d8-b38f-46e6-aa71-4f3418991507.png)

##### GCC编译器

上面所将的编辑器(vi、vim、记事本)是指我们用来写程序的，而我们写好的程序是需要使用编译器去运行；

###### gcc编译步骤

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684050358402-6feb8eed-1736-47d8-a260-512cb6cb1e7d.png)

**具体操作**：

1. 预处理

解释：首先编写好了代码文件1hello.c，然后gcc -E进行预处理，-o的意思是将输出结果到1hello.i中，

此时生成了预处理文件1hello.i

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684051813400-2d891b53-e3e8-4c98-bf0f-c01131fbcae0.png)

1. 编译

解释：将预处理文件1hello.i编译成了1hello.s汇编文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684052167408-e95b8045-62f4-4869-85ef-46caf3a0cee9.png)

1. 汇编

解释：将1hello.s汇编文件转为了机器语言(二进制)1hello.o

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684052403162-626abb35-a244-4ac6-bb65-234a34018c34.png)

1. 链接

解释：生成可执行文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684052711094-bdddc71a-64e0-4d12-86c5-4b98723c0033.png)

1. 执行文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684052774365-67298a01-f52c-4a2a-8775-7f31c7d657f4.png)



**简化操作**：

直接一步到位，从预处理直接到可执行文件，相当于执行了上面四步操作；

`gcc 代码文件 -o 生成的执行文件名`(如果没有指定生成的执行文件名，会使用默认名a.out)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684053006791-c8b00285-ec43-415a-8534-a729433e7e4b.png)

##### 静态链接和动态链接

###### 静态链接

由链接器在链接时将库的内容加入到可执行程序中

优点：

- 对运行环境的依赖性较小，具有较好的兼容性

缺点：

- 生成的程序比较大，需要更多的系统资源，在装入内存时会消耗更多的时间；
- 库函数有了更新，必须重新编译应用程序

###### 动态链接

连接器在链接时仅仅建立于所需库函数之间的链接关系，在程序运行时才将所需资源调入可执行程序；

优点：

- 在需要的时候才会调入对应的资源
- 简化程序的升级，有着较小的程序体积
- 实现进程之间的资源共享

缺点：

- 依赖动态库，不能独立运行
- 动态库依赖版本问题严重

###### 对比

在gcc编译的最后一步(链接)加上-static，就可以把生成的可执行文件变为静态的

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684054894765-042c0c5a-adc2-45f9-acf3-062ae2e7e8ea.png)

静态的是将库的内容直接加入到可执行文件中；

动态的是将库和可执行文件直接建立了链接，当要执行文件时，才将内容加进去

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684055206110-91105b36-29ed-4a66-958e-1fd4bbccabe2.png)

##### GDB调试器

###### GDB简介

GNU工具集中的调试器是GDB，该程序是一个交互式工具，工作在字符模式；

GDB主要帮忙完成下面四个方面的功能：

1. 启动程序，可以按照你的自定义的要求随心所欲的运行程序
2. 可让被调试的程序在你所指定的调置的断点处停住
3. 当程序被停住时，可以检查此时你的程序中所发生的事
4. 动态的改变你程序的执行环境

###### 生成调试信息

a.out是一个可执行文件，然后使用命令 gcc -g gdbtest.c 后 它生成的可执行文件就具备了调试信息；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684057732643-2aa65cae-f958-4ffb-b4db-b8a6a524e35d.png)

###### 启动GDB

1. 启动gdb

`语法：gdb target;` 这里的target就是你具备调试信息的可执行文件；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684058609420-9ca6d70e-f64f-4c39-acfc-ed26989adc0b.png)

1. 设置参数

```
set args 可指定运行时参数，(如:set args 10 20 30 40)
show args 查看设置的运行参数
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684058721106-bc9d58e6-fd5b-453f-aa23-fdb0efa17361.png)

1. 启动程序

```
run：运行整个程序，如果程序有断点，则在第一个断点停住
start：一步一步的执行
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684058871431-4976090e-ba81-4742-a730-a125b2556e8f.png)

###### 显示源代码

用list代码打印程序的源代码，默认打印十行

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684059038250-5ec88b99-7713-43f4-92cb-a50041fa6ad7.png)

- list linenum：打印第linenum行的上下文内容
- list function：打印函数名为function的函数的源程序
- list：打印当前行后面的十行源代码
- list-：打印当前行前面的十行源代码
- set listsize count：设置一次显示源代码的行数
- show listsize：查看当前listsize的设置
- l 1：从第一行开始打印

###### 断点操作

1. **简单断点**

- break 设置断点，可以简写为b
- b 10，在源代码第十行设置断点
- b func，在func函数入口处设置断点
- info break || i  b，查询所有断点

1. **多文件设置断点**

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684059949045-24a2accd-94bb-4eed-a638-b563d93a849a.png)

###### 条件断点

```
b test.c:23 if i == 5
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684060185695-083d813b-a7b7-4380-ac6f-42c7916cf6ef.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684060234866-9d1b717c-6978-40cc-9198-be69a7bef302.png)

如果该程序23行中的i等于5，那么程序就在这里停住

###### 维护断点

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684060826828-e1d6e83b-41c5-4888-9edd-fa999e9a5607.png)

###### 调试代码

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684061086881-6c80d5d2-b6fd-4019-ad1d-24bb332d8916.png)

###### 数据查看

print 打印变量、字符串、表达式的值，可简写为p

p count 打印count的值

###### 查看和修改变量的值

```
ptype width，查看变量width的属性
p width，查看width的值
```

### Makefile

##### makefile简介

makefile定义了一系列的规则来指定如何编译文件，makefile带来的好处就是--“自动化编译”，一旦写好 只需要一个make命令，整个工程就完全自动化编译，极大的提高了软件开发的效率；

**make主要解决了两个问题**：

1. **大量代码的关系维护**

- 大项目中源代码比较多，手工维护、编译时间长而且编译命令复杂，难以记忆及维护；
- 而将代码维护命令和编译命令写入makefile中，然后在用make工具解析写入的命令，就可实现代码的合理编译

1. **减少重复编译时间**

- 在改动其中一个文件的时候，能判断哪些文件被修改过，可以只对该文件进行重新编译 节省编译的时间；

##### makefile语法规则

**一条规则**：

```shell
目标：依赖文件列表
<Tab> 命令列表

//目标：通常是指要产生的文件名称，目标可以是可执行文件或其他文件
//依赖文件：用来输入从而产生目标的文件，一个目标可以有多个依赖文件 也可以没有
//命令：make执行的动作，一个规则可以包含几个命令
```

例：**1.mk文件**，如果文件后缀名是.mk，那么就需要使用-f来指定文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684115301727-64604b2e-e0e1-4e31-86cf-bd2b5cd5f3ab.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684115348460-3925e176-7f0d-4f95-aa82-597c8352a27a.png)



例：**Makefile文件**，如果文件名为Makefile或者makefile，那么就可以直接使用make命令执行

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684115446379-f094d189-3e96-410d-b241-0e65639e0b8a.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684115578846-14b10552-2d58-4d6c-9d33-4ba0a2e19832.png)

##### makefile加减乘除示例

代码首先执行第一行(依赖文件列表)，然后依次去执行 依赖文件中的代码，最后生成目标可执行文件；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684116129476-aaf2e31b-9576-4482-a956-1a3d4456ba02.png)

##### makefile中的变量

在makefile中使用变量有点类似于C语言中的宏定义，使用变量来保存命令或者依赖文件，使用时直接引用变量即可；

**自定义变量**：

1. 定义变量：变量名=变量值
2. 引用变量：$(变量名)或者${变量名}

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684116893725-7a7b2260-b45c-46df-a0b0-c9bebabe7097.png)

**makefile内置变量**：

$@：表示目标；

$^：表示所有的依赖；

$<：表示第一个依赖；

最终精简版本：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684117416998-4b81b509-fc8f-400f-9e33-bb29fe39e4e4.png)

##### makefile中的函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684117780116-f55cd583-3f8b-45c5-a060-353ec2607cd5.png)

### 文件和系统调用

##### 系统调用简介和实现

###### 什么是系统调用？

系统调用，顾名思义，说的是操作系统提供给用户程序调用的一组特殊接口，用户程序可以通过这个特殊接口来获得操作系统内核提供的服务

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684225179953-ec3ef567-f643-4832-a089-f9d3f82afb5d.png)

###### 系统调用的实现

系统调用是属于操作系统内核的一部分，必须已某种方式提供给进程让它们去调用，相应的操作系统也有不同的运行级别 **用户态**和**内核态**，内核态可以毫无限制的访问各种资源，而用户态下的用户进程的各种操作都有限制，显然 属于内核的**系统调用是运行在内核态下**，那么如何切换到内核态呢？

答案是**软件中断**，操作系统一般是通过软件中断从用户态切换到内核态

###### 系统调用和库函数的区别

库函数主要由两类函数组成：

1. 不需要调用系统调用

不需要切换到内核空间即可完成函数全部功能，如strcpy、bzero等字符串操作函数

1. 需要调用系统调用

需要切换到内核空间，这类函数通过封装系统调用去实现相应的功能，如print、fread等

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684226013852-5517aee7-60c1-42ff-b82b-ae7f1f92d613.png)

##### 错误处理函数

errno用于记录系统的最后一次错误代码，返回一个int值(错误码)，在errno.h中定义，不同的错误码表示不同的含义

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684228400287-a806394c-cd81-4f89-a508-5d8057f89eff.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684228519508-ac1919af-9118-4e62-a7c9-a2d8920afab4.png)

也可以使用perror函数来直接获取错误原因：perror(“xxxx”)

##### 虚拟地址空间

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684229477856-a8df053d-e0ca-4e1d-8e4f-56d8095cb753.png)

**文件描述符**：

- 当我们打开文件或者新建文件时，系统会返回一个文件描述符用来指定已打开的文件，这个文件描述符相当于这个已打开文件的标号，操作这个文件描述符就相当于操作这个描述符所指定的文件；
- 程序运行起来后每个进程都有一张文件描述符的表，标准输入、输出，标准错误输出设备文件被打开，对应的文件描述符0、1、2就记录在表中，程序运行起来后这三个文件描述符是默认打开的

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684232738975-3debd113-d579-45eb-be78-4f074d5a581d.png)

##### 常用文件IO函数 

###### open函数  

**基本语法**：

```cpp
#include <sys/types.h>
#include <sys.stat.h>
#include <fcntl.h>

int open(const char *pathname, int flags);
int open(const char *pathname, int flags, mode_t mode);
参数：
    pathname：文件的路径及文件名
    flags：打开文件的行为标识(只读、只写、可读可写)
    mode：这个参数只有在文件不存在时有效,指新建文件时指定文件的权限
返回值：
      成功：返回打开的文件描述符
      失败：-1
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684234776703-7f87e672-d50b-452d-9905-b743e612828c.png)

###### close函数

**基本语法**：

```cpp
#include <unistd.h>

int close(int fd);
功能：
    关闭已打开的文件
参数：
    fd：文件描述符，open()的返回值
返回值：
    成功：0
    失败：-1，并设置errno
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684236818540-59038d16-c37a-414d-a7cc-b385fb600283.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684236785723-d52427f0-d0ae-410f-8745-328ee5281ecb.png)

###### write函数

```cpp
#include <unistd.h>
ssize_t write(int fd, const void *buf, size_t count);
功能：
    把指定数目的数据写到文件(fd)
参数：
    fd：文件描述符
    buf：数据首地址
    count：写入数据的长度(字节)
返回值：
    成功：实际写入数据的字节个数
    失败：-1
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684237781873-d7768647-20fa-4a80-87db-9b488e7609db.png)

代码解释：

1. 首先以可写的方式打开一个文件，如果没有该文件则新建；
2. 写入文件，参数分别是：文件描述符、数据首地址、写入的字符长度
3. 关闭文件
4. gcc 成功执行后，就会将数据写入文件中

###### read函数

```cpp
#include <unistd.h>

ssize_t read(int fd, void *buf, size_t count);
功能：
    把指定数目的数据读到内存(缓冲区)
参数：
    fd：文件描述符
    buf：内存首地址
    count：读取的字节个数
返回值：
    成功：实际读取到的字节个数
    失败：-1
```

###### lseek函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684307956440-1d83dcf3-afad-4d21-b63d-f3bd5eb7a72c.png)

文件的读和写使用的是同一偏移位置；

使用lseek获取文件大小：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684314480206-d9068428-3db2-4079-969e-e91262e0e280.png)

##### 文件描述符复制

###### 概述

dup()和dup2()是两个非常有用的系统调用，都是用来复制一个文件的描述符，使新的文件描述符也标识旧的文件描述符所标识的文件；

这个过程类似于现实生活中的配钥匙，一把钥匙对应一把锁，然后我们又去配了一把新钥匙，此时两把钥匙都可以打开锁，而dup()和dup2()也一样，原来的文件描述符和新复制出来的文件描述符都指向同一个文件，我们操作这两个文件描述符的任何一个 都能操作它所对应的文件

###### dup函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684319775922-21dd183b-472a-4a83-b029-97e4b309c2f7.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684320327409-a6c3a4ed-ff36-4afe-a005-1aba08d44db7.png)

运行后输出：ABCDEFG1234567；因为它俩是共享一个偏移量，因此不会覆盖

###### dup2函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684320586906-6b736ead-e877-4c6a-859a-884cfdbe258a.png)

与dup函数的区别：可以指定文件描述符(第二个参数 newfd);

###### 头文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684375721469-d54d1cc3-537c-4c46-9fe8-6108b80d7c43.png)

###### fcntl函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684395302501-9739ec48-e507-44bb-934e-fafe4bb3a1d4.png)

**功能一**：复制文件描述符（与dup相同）

fcntl的第三个参数0 表示返回一个最小的可用的文件描述符，并且大于或等于0；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684396258520-4ef802b3-5177-4422-91d3-01845341955d.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684396271652-04b81310-bd2f-45c8-9538-dce63593e33d.png)

执行后输出123abc表示复制成功，fd和newfd指向了同一个文件，共用一个偏移量

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684396406973-bc6d3f9d-0b85-4c10-9901-293c3fb2bb26.png)

##### 目录相关操作

###### getcwd函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684397914614-2d5de263-f530-441d-b6e7-9f72b7bbdbbe.png)

###### chdir函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684397945483-9bab224e-15a8-4747-98d1-776f82057632.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684398404621-54a319c9-9b43-4550-9414-16ece979a716.png)

###### opendir函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684399052864-df8cb031-8175-4bc5-9d01-51943727a6b2.png)

###### closedir函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684399117812-e0b2c5fb-4328-4b3e-8dbd-4e10c39dbf32.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684399589512-6350579e-caa3-45e5-824f-c5d76badf520.png)

###### readdir函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684399950464-824bc6d8-8c88-4913-8e65-3660da45300e.png)

### 进程

##### 进程和程序

我们平时写好的代码，通过编译后生成的可执行文件就是一个程序，当这个程序被运行起来后(没结束之前) 它就成为了一个进程。

程序是静态的，进程是动态的(创建、调度、消亡) 

##### 进程的状态

在三态模型中，进程状态分为三个基本状态，即：**运行态、就绪态、阻塞态**；

在五态模型中，进程状态分为五个基本状态，即：**新建态、终止态、运行态、就绪态、阻塞态**；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684461616110-d0e3d793-e295-4fb2-ab3c-22e9a2fbe77c.png)

###### ps命令

ps命令可以查看进程的详细状况，常用选项如下：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684461927313-2e8982f1-53a4-46e3-8aeb-011ba53871b1.png)

###### top命令

top命令用来动态显示运行中的进程

###### kill命令

**使用方法**：

1. 让进程在后台睡眠

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684462241179-0457ec57-4292-465e-bca7-2a0c97d537bc.png)

1. ps -a，找到该进程的PID

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684462316311-b5421c63-2b3a-43a7-b920-499ad77c8543.png)

1. kill PID，即可杀死此进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684462346904-bd2b0e6e-f7aa-4d62-abc3-6f40e656be6e.png)



但是有些进程我们不能直接杀死，这时候我们需要加上参数-9，强制结束

killall可以通过进程名来杀死进程

##### 进程号和相关函数

每个进程都由一个进程号来标识，其类型为pid，进程号的范围：0~32767，进程号总是唯一的，但进程号可以重用，当一个进程终止后 其进程号就可以再次使用；

接下来在给大家介绍三种进程号：

**进程号(PID)**：

标识进程的一个非负整形数

**父进程号(PPID)**:

任何进程都是由另一个进程创建，该进程称为被创建进程的父进程，对应的进程号称为父进程号（PPID），如 A进程创建了B进程，A的进程号就是B进程的父进程号

**进程组号(PGID)**:

进程组是一个或多个进程的集合，它们之间相互关联，进程组可以接收同一终端的各种信号，关联的进程有一个进程组号（PGID），默认情况下 当前的进程号会当作当前的进程组号

###### getpid

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684463634084-9319b670-8fc7-4b6f-8fa9-54a2e394defb.png)

```c
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main(void)
{
//获取当前进程的进程号
int pid = getpid();
printf("pid = %d\n", pid);

return 0;
}

执行后：
hui@hui-virtual-machine:~/test$ ls
pid.c
hui@hui-virtual-machine:~/test$ gcc pid.c 
hui@hui-virtual-machine:~/test$ ./a.out
pid = 4707
hui@hui-virtual-machine:~/test$ ./a.out
pid = 4708
hui@hui-virtual-machine:~/test$ ./a.out
pid = 4709
```

###### getppid

```c
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main(void)
{
//获取当前进程的进程号
int pid = getpid();
printf("当前进程 = %d\n", pid);

//获取当前进程的父进程号
pid = getppid();
printf("父进程 = %d\n", pid);

return 0;
}


hui@hui-virtual-machine:~/test$ gcc pid.c 
hui@hui-virtual-machine:~/test$ ./a.out
当前进程 = 4739
父进程 = 3760
hui@hui-virtual-machine:~/test$ 
```

###### getpgid

该函数必须传入一个参数>>要获取哪个进程的进程组号

```c
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main(void)
{
//获取当前进程的进程号
int pid = getpid();
printf("当前进程 = %d\n", pid);

//获取当前进程的父进程号
pid = getppid();
printf("父进程 = %d\n", pid);

//获取当前进程的进程组号
pid = getpgid(getpid());
printf("进程组 = %d\n", pid);

return 0;
}



hui@hui-virtual-machine:~/test$ gcc pid.c 
hui@hui-virtual-machine:~/test$ ./a.out
当前进程 = 4794
父进程 = 3760
进程组 = 4794
hui@hui-virtual-machine:~/test$ ./a.out
当前进程 = 4795
父进程 = 3760
进程组 = 4795
hui@hui-virtual-machine:~/test$ 
```

##### 进程的创建

系统允许一个进程创建新进程，新进程即为子进程，子进程还可以创建新的子进程，形成进程树结构模型

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684484514576-a9c1bd55-853a-4d6a-8524-6036179ea469.png)

示例代码：

```c
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main(void)
{
//创建子进程
fork();

printf("hello world\n");

return 0;
}

hui@hui-virtual-machine:~/test$ gcc fork.c 
hui@hui-virtual-machine:~/test$ ./a.out       
hello world                                 //上面的代码执行后会打印两次，是为什么呢？
hello world
```

因为我们复制出来的子进程就相当于父进程的克隆体，而它们的PC指针指向了下一条执行的语句，所以打印两次

**我们说进程调用 fork ，当控制转移到内核的 fork 代码后，内核会**：

1. 将父进程部分数据拷贝给子进程；
2. 分配新的内存块和数据结构给子进程；
3. 子进程添加到进程列表；
4. fork 返回，开始调度

因此 fork 之前父进程独立执行，fork 后父子分别执行，但是谁先谁后完全取决于调度器。

fork 之后，共享的只有 fork 后的代码吗？一般情况下，是父子共享所有代码，虽然子进程执行后续代码，它是相当于共享了所有代码但是子进程只能从某个地方开始执行！什么原理呢？很简单，在 CPU 里面有一种寄存器能保存当前的执行进度，它叫 eip，普遍喜欢叫它程序计数器或者 pc 指针，通过保存当前正在执行指令的下一条指令，拷贝给子进程。

##### 循环创建进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684805974249-652107e4-c90d-4677-ac03-60e762188bc2.png)

##### 父子进程关系

1. 使用fork()函数得到的子进程是父进程的一个复制品，它从父进程继承了整个进程的地址空间：包括进程上下文、进程堆栈、打开的文件描述符、信号控制设定、进程优先级、进程组号等。
2. 但是子进程也有它独有的进程号，计时器等。
3. linux内核引入了 读时共享，写时拷贝；如果父子进程都是只读的话 那么它们就共享同一个地址空间(避免造成资源浪费)，只有写入的时候才会复制地址空间，那么此时它俩都拥有各自的空间。
4. fork之后的父子进程共享文件偏移量。

##### 区分父子进程

通过fork的返回值来区分，fork函数被调用一次但返回两次，两次返回的区别是：子进程的返回值是0，而父进程的返回值则是子进程的PID； 

```c
int main(void)
{
pid_t pid = -1;

//创建一个子进程
pid = fork();

if(0 == pid)
{
//子进程
printf("我是子进程%d,我的父进程是%d\n",getpid(),getppid());
exit(0);
}
else
{
//父进程
printf("我是父进程%d,我的子进程是%d\n",getpid(),pid);
}

return 0;
}


hui@hui-virtual-machine:~/test$ gcc fork.c 
hui@hui-virtual-machine:~/test$ ./a.out
我是父进程2553,我的子进程是2554
我是子进程2554,我的父进程是2553
hui@hui-virtual-machine:~/test$ 
```

##### 父子进程地址空间

代码解释：定义了一个变量var=88，然后让子进程睡眠1s，此时父进程肯定先执行 然后将var++，那么子进程睡醒之后去获取var的值依然是88，遵循读时共享，写时拷贝；

如果在堆区开辟了空间，那么释放的时候要释放两次(子进程和父进程)，否则会造成内存泄漏

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684488737907-a56343bc-729a-4090-84ab-47dc7263b5e5.png)

##### 进程退出函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684489800351-a29abe30-134a-46d2-a979-0e05dd29bf50.png)

##### 等待子进程退出的函数★

###### 概述

在每个进程退出的时候，内核释放该进程所有的资源，包括打开的文件、占用的内存等。但是仍然为其保留了一定的信息，这些信息主要是指进程控制块PCB的信息(包括进程号、退出状态、运行时间等)。

父进程可以通过调用wait或waitpid得到它的退出状态同时彻底清除掉这个进程。

wait()和waitpid()的功能一样，区别在于wait()会阻塞（如果子进程没结束，那么就一直等待不做其他事），waitpid()可以设置不阻塞，waitpid()还可以指定等待哪个子进程结束

注意：一次wait或waitpid调用只能清理一个子进程，清理多个子进程应使用循环

###### wait函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684491518147-e9f590d5-d36d-438f-850f-5be0cf182dee.png)

**示例一**：

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>

int main(void)
{
int status = 0;
int i = 0;
pid_t pid = -1;

//创建子进程
pid = fork();
if(-1 == pid)
{
perror("fork");
return 1;
}
    
//如果pid=0，那么就是子进程
if(pid == 0)
{
for(i=0; i<5; i++)
{
printf("child process do thing %d\n", i+1);
sleep(1);
}

//子进程终止
exit(10);
}
    
//下面是父进程执行
printf("父进程等待子进程结束，回收其资源\n");
int ret = wait(&status);
if(-1 == ret)
{
perror("wait");
return 1;
}
printf("父进程回收了子进程的资源\n");

return 0;       
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684495340949-323b7d91-e778-4a2e-a710-b568cec7cf9e.png)



**使用宏函数来获取进程退出时的状态**：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684495656963-dfab15a3-a130-4eae-bf33-4182be8ec8ec.png)

```c
//使用宏函数来获取进程退出时的状态信息
if(WIFEXITED(status))
{
printf("子进程退出状态码:%d\n",WEXITSTATUS(status));
}
else if(WIFSIGNALED(status))
{
printf("子进程被信号%d杀死了...\n",WTERMSIG(status));
}
else if(WIFSTOPPED(status))
{
printf("子进程被信号%d暂停...\n",WSTOPSIG(status));
}
```

**第一组**：正常结束进程，然后获取退出状态(exit的参数)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496414109-9f82889a-83c1-4575-9e26-8ead4a9f5d7d.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496342074-167c0546-fd09-486e-aa74-bd9215297e18.png)

**第二组**：异常终止，然后获得使进程终止的信号的编号

1. 此进程的PID是121114

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496664585-e4861f8c-9399-4b95-9c39-ede19c59619d.png)

1. 杀死进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496729060-21c345ec-e1fa-4c62-b4e3-968697f3d0e2.png)

1. 获得终止信号的编号
2. ![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496767283-e1163d6c-3685-4851-84f2-bd61a472494b.png)

**第三组**：进程暂停，取得使进程暂停的那个信号的编号

1. 此进程的PID是121422

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496943796-2dcbca2f-eacf-4bbb-8e0f-0125a253f2e4.png)

1. 使用 kill  -19暂停进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684496985668-e1a2e1b8-599e-4df5-850b-15e339333a59.png)

1. 此时进程暂停了
2. 使用 kill  -18开始进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684497078013-7b895e16-9f6f-4231-a7c0-b518b0f0abe2.png)

1. 进程正常开始运行

###### waitpid函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684497595207-c3cb0661-9169-431f-9209-1f805ebc320c.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684497683477-497e5e5e-285a-4dda-967d-94f6fdf94d5d.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684497775290-7d48718b-d2ec-4068-b001-dc4f416d806c.png) 此状态下为不阻塞，即不会等待子进程执行，直接去执行自己的任务

wait和waitpid只能回收子进程，并且调用一次只能清理一个，如需清理多个得使用循环；

##### 僵尸进程&孤儿进程

孤儿进程：父进程结束了，但是子进程还在运行，此时内核的init进程会等待该子进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684498354774-2f1db35d-439f-4167-ada9-56c469ebb3db.png)

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/wait.h>

int main(void)
{
pid_t pid = -1;
int status = -1;

//创建子进程
pid = fork();
if(pid == -1)
{
perror("fork");
return 1;
}

//编写子进程代码
if(pid == 0)
{
    
for(int i=0; i<10; i++)
{
printf("子进程正在执行:%d\n",i);
sleep(1);
}

exit(0);
}

//父进程
printf("父进程等待子进程结束，回收其资源\n");
printf("父进程执行完毕\n");

return 0;
}
```

僵尸进程：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684498425884-a1b63ffd-0766-416f-9c49-e8472eea6225.png)

##### 进程替换

Linux进程替换指的是将当前正在运行的一个进程的代码和数据替换成另一个可执行文件的代码和数据，同时保留其原有的进程ID和其他系统资源（如文件描述符、信号处理程序等），从而实现了进程的动态更新。这种技术通常用于实现程序的热更新、回滚、重新加载等功能，同时也可以用于实现不同版本之间的平滑升级或回滚。在UNIX和Linux系统中，常用的进程替换函数包括exec()系列函数、system()函数、popen()函数等。 

###### exec函数族

fork创建子进程后执行的是和父进程相同的程序，我们可以使用exec函数族来让它执行另一个程序，但进程PID不变，换核不换壳

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684542178745-b07dbe3d-0829-442b-a50a-2897b38d1bad.png)

###### execlp

**该函数通常用来调用系统的可执行程序，如：cat、ls、date**

语法：int execlp(const  char *file，const  char *arg，...)

参数一：要执行的文件名；参数二：文件名；参数三：要执行的文件的参数(可以是多个)；最后要加上NULL，因为它是变参

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684543953241-b72e4b2e-2cb9-4e08-a958-41e6d2d935e1.png)

成功的话无返回值，失败的话返回-1

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>

int main(void)
{
pid_t pid = fork();

if(pid < 0)
{
//fork失败
perror("fork");
exit(1);
}
else if(pid == 0)
{
//子进程
execlp("ls","ls","-l","-h",NULL);
perror("execlp error");  //如果execlp成功，下面的不执行
exit(1);
}
else if(pid > 0)
{
//父进程
sleep(1);
printf("我是父进程:%d\n",getpid());
}

return 0;
}
```

###### execl

**该函数通常用来执行自己的可执行文件**；

语法：int execl(const  char *path，const  char  *arg，...);

参数一：自己要执行文件的路径；参数二：文件名；参数三：要执行的文件的参数(可以是多个，也可以为空)；最后要加上NULL，因为它是变参



需求：在execl中fork子进程去执行该目录下的wait可执行文件

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684544432574-677e0db2-da67-431f-9e4c-a4fe848361ef.png)

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>

int main(void)
{
pid_t pid = fork();

if(pid < 0)
{
//fork失败
perror("fork");
exit(1);
}
else if(pid == 0)
{
//子进程
execl("./wait","wait"，NULL);
perror("execlp error");  //如果execl成功，下面的不执行
exit(1);
}
else if(pid > 0)
{
//父进程
sleep(1);
printf("我是父进程:%d\n",getpid());
}

return 0;
}
```

### 进程间通信★

##### 概念

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684548350314-f4e3bede-e66d-41fc-b27d-e88f9e540627.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684548591979-6a36c34d-2543-4296-ac33-0c40a7104b09.png)



##### 无名管道PIPE ★

###### 管道的概念

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684549194082-8a7de497-aabc-4bee-998d-3fef4589952f.png)

**无名管道是作用于有血缘关系的进程之间完成数据传递**，调用pipe系统函数即可创建一个管道

**实现原理**：内核借助环形队列机制，使用内核缓冲区实现

**管道有如下特质**：

1. 其本质是一个伪文件(实为内核缓冲区)
2. 由两个文件描述符引用，一个表示读端，一个表示写端
3. 规定数据从管道的写端流入管道，从读端流出

**管道的局限性**：

1. 数据不能进程自己写，自己读
2. 管道中数据不可反复读取，一旦读走 管道中将不存在此数据
3. 采用半双工通信方式，数据只能在单方向上流动
4. 只能在有公共祖先的进程间使用管道

###### pipe函数★

用于创建并打开管道；

**语法：int  pipe(int pipefd[2]);    fd[0]是读端，fd[1]是写端**

返回值：成功：0，失败：-1并设置perror



1. 父进程调用了pipe()，相当于创建了一个管道并打开了读端和写端，pipefd[0]是读端，pipefd[1]是写端
2. 父进程fork出一个子进程，此时子进程也掌握着父进程管道的读端和写端
3. 父进程写入数据(读端关闭)，子进程读取数据(写端关闭)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684560342123-1e00cc68-2cb2-4431-a7f2-19ac5d1e954d.png)

1. 最后就实现了单通道传递数据

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>

int main(void)
{
int ret;
int fd[2];
pid_t pid;

char buf[1024];
char *str = "hello pipe\n";

//创建管道
ret = pipe(fd);
if(ret < 0)
{
perror("pipe");
exit(1);
}
    
//fork进程
pid = fork();
    
if(pid > 0)
{
close(fd[0]); //父进程关闭读端
write(fd[1],str,strlen(str)); //写入数据
close(fd[1]); //写完后关闭写端
}
else if(pid == 0)
{
close(fd[1]); //子进程关闭写端
ret = read(fd[0],buf,sizeof(buf)); //读取数据到buf中
 
write(STDOUT_FILENO,buf,ret); //将buf的数据打印到屏幕上，ret是字节数
close(fd[0]);  //关闭读端
}


return 0;
}
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>

int main(void)
{
int ret;
int fd[2];
pid_t pid;

    
//创建管道
ret = pipe(fd);
if(ret<0)
{
perror("pipe");
exit(1);
}

//fork进程
pid = fork();
if(pid>0)
{
close(fd[0]);                 //dup2：将参数2指向参数1
dup2(fd[1],STDOUT_FILENO);    //STDOUT_FILENO标准输出，表示将此进程的结果输出到管道中
execlp("ls","ls",NULL);
}
else if(pid == 0)
{
close(fd[1]);
dup2(fd[0],STDIN_FILENO);    //STDIN_FILENO标准输入，表示将此进程的输入要从管道中获取
execlp("wc","wc","-l",NULL);
}

return 0;
}
```

###### 管道的读写行为

**读管道**：

1. 管道有数据：返回实际读到的字节数
2. 管道无数据：（1）无写端，read返回0； （2）有写端，read阻塞等待

**写管道**：

1. 无读端：异常终止
2. 有读端：（1）管道已满，阻塞等待；（2）管道未满，返回写出的字节个数

###### 兄弟进程间通信

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h> 

int main(void)
{
    int ret;
    int fd[2];
    pid_t pid;

    char *str = "hello brother";
    char buf[1024];

    // 创建管道
    ret = pipe(fd);
    if(ret < 0)
    {
        perror("pipe");
        exit(1);
    }

    // 循环 fork 进程
    for(int i=0; i<2; i++)
    {
        pid = fork();

        if(pid == -1)
        {
            perror("fork");
        }

        if(pid == 0)
        {
            break;
        }
    }

    // 兄进程
    if(pid == 0)
    {
        close(fd[0]); // 关闭读端
        ret = write(fd[1], str, strlen(str));
        if(ret < 0) {
            perror("write");
            exit(1);
        }
        close(fd[1]); // 关闭写端
    }
    // 弟进程
    else if(pid == 1)
    {
        close(fd[1]); // 关闭写端
        ret = read(fd[0], buf, sizeof(buf));
        if(ret < 0) {
            perror("read");
            exit(1);
        }
        close(fd[0]); // 关闭读端

        ret = write(STDOUT_FILENO, buf, ret);
        if(ret < 0) {
            perror("write");
            exit(1);
        }
    }
    // 父进程
    else if(pid > 0)
    {
        wait(NULL);
        wait(NULL);
        printf("已经回收子进程\n");
    }

    return 0;
}
```

##### 有名管道FIFO

###### 概念

**fifo可以实现没有血缘关系进程间的通信**；

创建方式：

1. 命令：mkfifo 管道名
2. 库函数：int  mkfifo(const  char *pathname，mode_t mode)；成功0，失败-1
3. 参数解析：参数1是管道名，参数二是权限0664；

```c
int main(void)
{
int ret = mkfifo("myfifo",0664)

if(ret == -1)
{
perror("mkfifo");
exit(1);
}

return 0;
}
```

一旦使用mkfifo创建了一个FIFO，就可以使用open打开它，常见的I/O函数都可以用于FIFO，如：open,close....

###### 实现非血缘关系的通信

argc和argv是程序的输入参数。

argc是一个整数类型的变量，代表了传递给程序的参数个数，其中argc至少为1，因为第一个参数总是程序本身的名称。

argv是一个字符指针数组，每个元素指向一个传递给程序的参数字符串，包括程序名称。数组的第一个元素argv[0]通常为程序名称，那么argv[1]就是该程序后面接的文件，例如：writefifo  myfifo，myfifo管道文件就是argv[1]；

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/stat.h>
#include <fcntl.h>

int main(int argc, char *argv[])
{
int fd,i;
char buf[4096];

if(argc < 2)
{
printf("Enter like this: ./a.out fifoname\n");
return -1;
}

fd = open(argv[1],O_WRONLY);
if(fd < 0)
{
perror("open");
exit(-1);
}

i = 0;
while(1)
{
sprintf(buf,"hello%d\n",i++);

write(fd,buf,strlen(buf));
sleep(1);
}
close(fd);

return 0;
}
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/stat.h>
#include <fcntl.h>

int main(int argc,char *argv[])
{
int fd,i;
char buf[4096];

if(argc < 2)
{
printf("要指定文件\n");
return -1;
}

fd = open(argv[1],O_RDONLY);
if(fd<0)
{
perror("open");
exit(-1);
}

while(1)
{
int len = read(fd,buf,sizeof(buf));
write(STDOUT_FILENO,buf,len);
sleep(1);
}

close(fd);

return 0;
}
```

一个写，一个读

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684576247564-f917409a-a673-40c5-8349-5190f62a1a18.png)

##### 存储映射I/O ★

存储映射使一个磁盘文件与存储空间中的一个缓冲区相映射，这个映射工作可以通过mmap函数来实现

###### 扩展内存

ftruncate(fd,10);

###### mmap函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684578408786-b4d1d0df-77b5-446f-8f64-9b63847b8f16.png)

munmap(p,len);  释放

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/mman.h>

int main(int argc, char *argv[2])
{
char *p = NULL;
int fd;

//1. 打开一个文件作为映射区
fd= open("testmmap",O_RDWR);
if(fd == -1)
{
perror("open");
return -1;
}

//2.  扩展内存大小
ftruncate(fd,20); 
int len = lseek(fd,0,SEEK_END);
    
//3. 开始映射
p = mmap(NULL, len, PROT_READ|PROT_WRITE, MAP_SHARED, fd, 0);
if(p == MAP_FAILED)
{
perror("mmap error");
exit(1);
}

//4. 使用p对文件进行读写操作
strcpy(p,"hello mmap");  //写
printf("----%s\n",p);    //读

//5. 释放内存区
int ret = munmap(p,len);
if(ret < 0)
{
perror("munmap");
exit(1);
}
return 0;
}
```

###### mmap注意事项

问题：

1. 可以open的时候O_CREAT一个新文件来创建映射区吗？
2. 如果open时 O_RDONLY, mmap时PROT参数指定PROT_READ|PROT_WRITE会怎样？
3. 文件描述符先关闭，对mmap映射有没有影响？
4. 如果文件偏移量为1000会怎么样？
5. 对mem越界操作会怎样？
6. 如果mem++，munmap可否成功？
7. mmap什么情况下会调用失败？
8. 如果不检测mmap的返回值会怎样？

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684585289036-33906048-26ec-46e4-a312-371256ea6585.png)

###### 父子进程间mmap通信

1. 父进程先创建映射区，open(O_RDWR)  mmap(MAP_SHARED)；
2. fork创建子进程
3. 一个进程读，另外一个进程写

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/mman.h>
#include <sys/types.h>
#include <sys/wait.h>

int main(void)
{
int *p = NULL;
int fd;
pid_t pid;

//1. 打开一个文件
fd = open("txt",O_RDWR|O_CREAT,0644);
if(fd==-1)
{
perror("open error");
exit(1);
}

//2. 扩展内存
ftruncate(fd,4);
int len = lseek(fd,0,SEEK_END);
    
//3. 开始映射
p = (int *)mmap(NULL,len,PROT_WRITE|PROT_READ,MAP_SHARED,fd,0);
if(p==MAP_FAILED)
{
perror("mmap error");
exit(1);
}

//4. fork进程
pid = fork();
if(pid<0)
{
perror("fork error");
exit(1);
}
else if(pid==0)
{
//子进程写
*p = 2000;
printf("子进程里的p=%d\n",*p);
}
else if(pid>0)
{
//父进程读
sleep(1);
printf("父进程里的p=%d\n",*p);
wait(NULL);

//5. 释放映射
int ret = munmap(p,4);
if(ret==-1)
{
perror("munmap error");
exit(1);
}
}
    
return 0;
}
```

###### 无关系进程间mmap通信★

**重点**：

写入时直接使用memcpy函数:参数一是指针，参数二是数据，参数三是字节数

读出时直接打印指针：printf(p)

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/mman.h>
#include <sys/types.h>
#include <sys/wait.h>

int main(void)
{
char *p = NULL;

//1. 打开文件
int fd = open("txt",O_RDWR|O_CREAT,0644);
if(fd==-1)
{
perror("open error");
exit(1);
}

//2. 开辟内存
ftruncate(fd,1024);
int len = lseek(fd,0,SEEK_END);

//3. 映射
p = mmap(NULL,len,PROT_WRITE|PROT_READ,MAP_SHARED,fd,0);
if(p == MAP_FAILED)
{
perror("mmap error");
exit(1);
}
close(fd);

//4. 写入
int i = 0;
while(1){
memcpy(p+i,"a",1);
i++;
sleep(1);
}

//5. 释放
munmap(p,len);

return 0;
}
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/mman.h>
#include <sys/types.h>
#include <sys/wait.h>

int main(void)
{
char *p = NULL;
 
//1.打开文件
int fd = open("txt",O_RDONLY,0644);
if(fd == -1)
{
perror("open error");
exit(1);
}

//2. 开辟内存
ftruncate(fd,1024);
int len = lseek(fd,0,SEEK_END);

//3. 映射
p = mmap(NULL,len,PROT_READ,MAP_SHARED,fd,0);
if(p==MAP_FAILED)
{
perror("mmap error");
exit(1);
}
close(fd);

//4. 读
while(1)
{
printf("%s\n",(char*)p);
sleep(1);
}

//5. 释放
munmap(p,len);

return 0;
}
```

### 信号★

##### 信号的概念

共性：简单、不能携带大量信息、满足条件才发送；

###### 信号的机制

A给B发送信号，B收到信号之前在执行自己的代码，**收到信号后，不管执行到程序的什么位置，都要暂停运行去处理信号**，处理完毕再去继续执行自己的代码，与硬件中断类似——异步模式。

每个进程收到的所有信号，都是由内核负责发送的，内核处理；

###### 与信号相关的事件和状态

**产生信号**：

1. 按键产生：如 Ctrl+c、Ctrl+z、Ctrl+\
2. 系统调用产生：如 kill、raise、abort
3. 软件条件产生：如 定时器alarm
4. 硬件异常产生：如 非法访问内存、内存对齐出错
5. 命令产生：如 kill命令

**递达**：

递送并且到达进程

**未决**：

产生和递达之间的状态，主要由于阻塞导致该状态

**信号的处理方式**：

1. 执行默认动作
2. 忽略(丢弃)
3. 捕捉(调用户处理函数)

**阻塞信号集(信号屏蔽字)**：

将某些信号加入集合，对他们设置屏蔽，当屏蔽x信号后，再收到该信号，该信号的处理将推后(解除屏蔽后)，

一旦被屏蔽的信号，再解除屏蔽前 一直处于未决态

**未决信号集**：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684651206873-ec5408eb-9c77-4b17-bdda-6e4d93b92f32.png)

###### 信号的编号

kill -l  获取全部信号



1) SIGHUP

本信号在用户终端连接(正常或非正常)结束时发出, 通常是在终端的控制进程结束时, 通知同一session内的各个作业, 这时它们与控制终端不再关联。
登录Linux时，系统会分配给登录用户一个终端(Session)。在这个终端运行的所有程序，包括前台进程组和后台进程组，一般都属于这个Session。当用户退出Linux登录时，前台进程组和后台有对终端输出的进程将会收到SIGHUP信号。这个信号的默认操作为终止进程，因此前台进程组和后台有终端输出的进程就会中止。不过可以捕获这个信号，比如wget能捕获SIGHUP信号，并忽略它，这样就算退出了Linux登录，wget也能继续下载。

此外，对于与终端脱离关系的守护进程，这个信号用于通知它重新读取配置文件。

2) SIGINT


程序终止(interrupt)信号, 在用户键入INTR字符(通常是Ctrl-C)时发出，用于通知前台进程组终止进程。

3) SIGQUIT


和SIGINT类似, 但由QUIT字符(通常是Ctrl-\)来控制. 进程在因收到SIGQUIT退出时会产生core文件, 在这个意义上类似于一个程序错误信号。

4) SIGILL


执行了非法指令. 通常是因为可执行文件本身出现错误, 或者试图执行数据段. 堆栈溢出时也有可能产生这个信号。

5) SIGTRAP


由断点指令或其它trap指令产生. 由debugger使用。

6) SIGABRT


调用abort函数生成的信号。

7) SIGBUS


非法地址, 包括内存地址对齐(alignment)出错。比如访问一个四个字长的整数, 但其地址不是4的倍数。它与SIGSEGV的区别在于后者是由于对合法存储地址的非法访问触发的(如访问不属于自己存储空间或只读存储空间)。

8) SIGFPE


在发生致命的算术运算错误时发出. 不仅包括浮点运算错误, 还包括溢出及除数为0等其它所有的算术的错误。

9) SIGKILL


用来立即结束程序的运行. 本信号不能被阻塞、处理和忽略。如果管理员发现某个进程终止不了，可尝试发送这个信号。

10) SIGUSR1


留给用户使用

11) SIGSEGV


试图访问未分配给自己的内存, 或试图往没有写权限的内存地址写数据.

12) SIGUSR2


留给用户使用

13) SIGPIPE


管道破裂。这个信号通常在进程间通信产生，比如采用FIFO(管道)通信的两个进程，读管道没打开或者意外终止就往管道写，写进程会收到SIGPIPE信号。此外用Socket通信的两个进程，写进程在写Socket的时候，读进程已经终止。

14) SIGALRM


时钟定时信号, 计算的是实际的时间或时钟时间. alarm函数使用该信号.

15) SIGTERM


程序结束(terminate)信号, 与SIGKILL不同的是该信号可以被阻塞和处理。通常用来要求程序自己正常退出，shell命令kill缺省产生这个信号。如果进程终止不了，我们才会尝试SIGKILL。

17) SIGCHLD


子进程结束时, 父进程会收到这个信号。

如果父进程没有处理这个信号，也没有等待(wait)子进程，子进程虽然终止，但是还会在内核进程表中占有表项，这时的子进程称为僵尸进程。这种情况我们应该避免(父进程或者忽略SIGCHILD信号，或者捕捉它，或者wait它派生的子进程，或者父进程先终止，这时子进程的终止自动由init进程来接管)。

18) SIGCONT


让一个停止(stopped)的进程继续执行. 本信号不能被阻塞. 可以用一个handler来让程序在由stopped状态变为继续执行时完成特定的工作. 例如, 重新显示提示符

19) SIGSTOP


停止(stopped)进程的执行. 注意它和terminate以及interrupt的区别:该进程还未结束, 只是暂停执行. 本信号不能被阻塞, 处理或忽略.

20) SIGTSTP


停止进程的运行, 但该信号可以被处理和忽略. 用户键入SUSP字符时(通常是Ctrl-Z)发出这个信号

21) SIGTTIN


当后台作业要从用户终端读数据时, 该作业中的所有进程会收到SIGTTIN信号. 缺省时这些进程会停止执行.

22) SIGTTOU


类似于SIGTTIN, 但在写终端(或修改终端模式)时收到.

23) SIGURG


有"紧急"数据或out-of-band数据到达socket时产生.

24) SIGXCPU


超过CPU时间资源限制. 这个限制可以由getrlimit/setrlimit来读取/改变。

25) SIGXFSZ


当进程企图扩大文件以至于超过文件大小资源限制。

26) SIGVTALRM


虚拟时钟信号. 类似于SIGALRM, 但是计算的是该进程占用的CPU时间.

27) SIGPROF


类似于SIGALRM/SIGVTALRM, 但包括该进程用的CPU时间以及系统调用的时间.

28) SIGWINCH


窗口大小改变时发出.

29) SIGIO


文件描述符准备就绪, 可以开始进行输入/输出操作.

30) SIGPWR


Power failure

31) SIGSYS


非法的系统调用。

在以上列出的信号中，

程序不可捕获、阻塞或忽略的信号有：SIGKILL,SIGSTOP
不能恢复至默认动作的信号有：SIGILL,SIGTRAP
默认会导致进程流产的信号有：SIGABRT,SIGBUS,SIGFPE,SIGILL,SIGIOT,SIGQUIT,SIGSEGV,SIGTRAP,SIGXCPU,SIGXFSZ
默认会导致进程退出的信号有：SIGALRM,SIGHUP,SIGINT,SIGKILL,SIGPIPE,SIGPOLL,SIGPROF,SIGSYS,SIGTERM,SIGUSR1,SIGUSR2,SIGVTALRM
默认会导致进程停止的信号有：SIGSTOP,SIGTSTP,SIGTTIN,SIGTTOU
默认进程忽略的信号有：SIGCHLD,SIGPWR,SIGURG,SIGWINCH

###### 信号的四要素

信号使用前应确定它的四要素

1. 编号
2. 名称
3. 事件
4. 默认处理动作

###### kill函数/命令产生信号

`int kill(pid_t pid, int sig)`成功：0，失败:-1；参数一是进程pid，参数二是信号名

pid>0：发送信号给指定的进程

pid=0：发送信号给与调用kill函数进程属于同一进程组的所有进程

pid<0：取绝对值，杀死该绝对值所对应的进程组的所有组员

pid=-1：发送给进程给有权限发送的系统中所有进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684661312437-21bfadbe-c79a-4cec-83e9-5ef9c4d668ed.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684661327762-06350297-3af4-4403-b1c7-75aee6a1d166.png)

代码解释：让父进程进入死循环，子进程睡2秒(确保父进程先执行)，然后再子进程中使用kill杀死父进程

kill -9 10698：杀死PID为10698的这个进程

kill -9 -10698：杀死进程组为10698的所有进程

###### alarm函数

返回值是它上次定时所剩余的秒数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684663336278-635a0aff-ddb8-443c-9356-66811cc02f53.png)

###### setitimer函数

setitimer函数

设置闹钟，可以替代alarm函数，精度微秒us，可以实现周期定时

```
int setitimer(int which, const struct itimerval *new_value, struct itimerval *old_value);
```

参数：

​	which：	ITIMER_REAL： 采用自然计时。 ——> SIGALRM

​			ITIMER_VIRTUAL: 采用用户空间计时  ---> SIGVTALRM

​			ITIMER_PROF: 采用内核+用户空间计时 ---> SIGPROF

​	new_value：定时秒数

​	old_value：传出参数，上次定时剩余时间。

返回值：

​	成功： 0

​	失败： -1 errno



类型

`struct itimerval` {

`struct timeval` {

time_t      tv_sec;         /* seconds */

suseconds_t tv_usec;        /* microseconds */

}it_interval;---> 用于设定两个定时任务之间的间隔时间

`struct timeval` {

time_t      tv_sec;         

suseconds_t tv_usec;        

}it_value;  ---> 第一次定时秒数

};



可以理解为有2个定时器

- 一个用于第一个闹钟什么时候触发打印
- 一个用于之后间隔多少时间再次触发闹钟。



例子

使用setitimer定时，向屏幕打印信息：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684664016461-43066a60-8246-42b1-a784-4cef475920d4.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684664027932-46061bfe-52af-4e77-a995-d76ba5fea66e.png)

第一次信息打印是两秒间隔，之后都是5秒间隔打印一次

##### 信号集操作函数

内核通过读取未决信号集来判断信号是否应该被处理，信号屏蔽字mask可以影响未决信号集 而我们可以在应用程序中自定义set来改变mask，已达到屏蔽指定信号的目的

###### 信号集设定

由于我们不能直接操作内核里的阻塞信号集，因此我们要自己设定一个 然后用函数对它操作，可以将我们自己设定的信号集与系统内核的信号集进行位或&位与&替换；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684743712012-0f8dc911-8cd2-4c02-aeba-ab168fee0b6d.png)

自己写的叫set，系统内核PCB里的叫mask，视频P134里解释原理

###### 信号集函数练习

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <signal.h>

void print_set(sigset_t *set)
{
    int i;

    for(i=1; i<32; i++) {
        if(sigismember(set,i))
            putchar('1');
        else
            putchar('0');
    }

    printf("\n");
}


int main(void)
{
//1. 定义自己的信号集
    sigset_t set, oldset, pedset;

    sigemptyset(&set); //清空信号集
    sigaddset(&set,SIGINT);//将2号信号(Ctrl C)加入信号集内

//2. 将系统的信号集替换为自己的
    int ret = sigprocmask(SIG_BLOCK,&set,&oldset); //SIG_BLOCK设为阻塞
    if(ret == -1)
    {
        perror("sigprocmask error");
        exit(1);
    }

//3. 查看未决信号集的状态
    while(1) {
        ret = sigpending(&pedset); //这个函数会传出状态，用pedset接收
        if(ret == -1)
        {
            perror("sigpending error");
            exit(1);
        }
        print_set(&pedset); //调用上面的函数 查看是否在信号集中
        sleep(1);
    }

    return 0;
}
```

**代码解释**：

1. 定义自己的信号集set；
2. 清空信号集，使用sigaddset()加指定的信号加入信号集内
3. 使用sigprocmask()将系统的信号集替换为自己的，它的第一个参数是设置条件(阻塞，取消阻塞)
4. 使用sigpending()查看未决信号集
5. 封装一个sigismember函数，来打印sigpending传出的信号集



开始执行：

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684748874183-2e67f979-3765-4770-a09c-d4306dc0a6bf.png)

按下Ctrl C之后，信号2 从0变成了1，一直处于了未决状态，如果没设置阻塞，它会从0变为1然后迅速变为0

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684748923267-231a7ebb-cc5c-47c4-aa09-2b688d5ae69d.png)

##### 信号捕捉

捕捉(调用户处理函数)，捕捉到信号后 用户自定义让它去做什么

###### signal函数

**注册**一个信号捕捉函数；

signal（要捕捉的信号，要执行的函数）

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <signal.h>

void sig_cath(int signo)  //signo是信号的编号
{
printf("catch you!! %d\n",signo);
return;
}
 

int main(void)
{

signal(SIGINT,sig_cath);  //signal（要捕捉的信号，捕捉到后要执行的函数）
while(1);
    
return 0;
}
```

因为代码中有循环，所以程序停在了这里；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684750680983-cf14f858-3ffb-45a1-a582-48c4739f5daa.png)

按下Ctrl C后，执行参数二的函数，2表示这个信号的编号

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684750740511-f7c0821a-ada7-45ed-9c7f-aea5e0e50add.png)

###### sigaction函数★

**注册**一个信号捕捉函数；

```
int sigaction(int signum，const struct sigaction *act， struct sigaction *oldact);
```

参数一：要捕捉的信号，参数二：一个结构体 新的处理状态，参数三：保存它旧有的对这个信号的处理状态；

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684752807989-52c78919-f526-49d5-b0ec-d00d55365581.png)

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <signal.h>

void sig_cath(int signo) //回调函数
{
printf("catch you!! %d\n",signo);
return;
}


int main(void)
{
struct sigaction act, oldact; //定义sigaction结构体

act.sa_handler = sig_cath;   //回调 
sigemptyset(&act.sa_mask);   //清空sa_mask屏蔽字,只在sig_cath工作时有效
act.sa_flags = 0;            //默认值

sigaction(SIGINT,&act,&oldact); //注册信号捕捉函数
    
while(1);

return 0;
}
```

###### 信号捕捉的特性

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684756602748-2d605936-fa7e-41a9-aec7-b752aeded82f.png)

##### SIGCHLD信号

###### SIGCHLD产生的条件

- 只要子进程的状态发生变化就会产生SIGCHLD信号；

###### 借助SIGCHLD回收子进程

核心思路：

1. 循环创建多个子进程
2. 在注册信号捕捉前加上信号屏蔽集去屏蔽SIGCHLD信号，以免信号捕捉未注册完  子进程就死亡了
3. 父进程中注册sigaction信号捕捉（回调函数中循环回收子进程）
4. 取消屏蔽SIGCHLD信号

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <signal.h>
#include <sys/types.h>
#include <sys/wait.h>

//回调函数
void catch_child(int signo)
{
pid_t wpid;

while((wpid = wait(NULL)) != -1)
{
printf("----------catch%d\n",wpid);
}

return ;
}

int main(void)
{

pid_t pid;

//阻塞
sigset_t set;
sigemptyset(&set);
sigaddset(&set,SIGCHLD);
sigprocmask(SIG_BLOCK,&set,NULL);

//循环创建子进程
int i;
for(i=0; i<5; i++)
        if((pid=fork()) == 0)
                break;

if(5 == i)
{
//父进程中信号捕捉
struct sigaction act;
act.sa_handler = catch_child;
sigemptyset(&act.sa_mask);
act.sa_flags = 0;
sigaction(SIGCHLD,&act,NULL);

//解除阻塞
sigprocmask(SIG_UNBLOCK,&set,NULL);

printf("我是父进程,pid是%d\n",getpid());

while(1);
}
else
{
printf("我是子进程,pid是%d\n",getpid());
}
return 0;
}
```

### 守护进程★

##### 概念和特性

多个进程就是一个进程组，而多个进程组就是一个会话

##### 创建会话

**组长进程不能创建会话**

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684843419560-37434fe8-4d95-490c-a3d9-d6b5af70003e.png)



**getsid函数：**

获取进程所属的会话ID

```
pid_t getsid(pid_t pid);
```

成功返回所属会话ID，失败返回-1并设置error



**setsid函数**：

创建一个会话，并以自己的ID设置进程组ID，同时也是新会话的ID；

```
pid_t setsid(void);
```

成功返回会话ID，失败返回-1并设置error 

调用了setsid函数的进程，既是新的会长，也是新的组长

##### 守护进程

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684844524449-9e08eb7d-838e-4de2-8d6f-eb40640ad75d.png)

守护进程创建步骤：

1.  fork子进程，让父进程终止。 
2. 子进程调用 setsid() 创建新会话  
3. 改变工作目录位置 chdir()， 防止目录被卸载。 
4.  通常根据需要，重设umask文件权限掩码，影响新文件的创建权限。  
5.  关闭/重定向 文件描述符 
6.  守护进程 业务逻辑。while（） 

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/types.h>
#include <pthread.h>
#include <sys/stat.h>


int main(void)
{
        pid_t pid;
        int fd;

        pid = fork();
        if(pid>0)
                exit(0);         //1. 退出父线程

        pid = setsid();  //2. 子进程创建会话
        if(pid==-1)
        {
                perror("setsid error");
                exit(1);
        }

        //3. 改变文件目录
        chdir("/home/hui/test");

        //4. 设置权限掩码
        umask(0022);

        //5. 关闭/重定向 文件描述符

        close(STDIN_FILENO); //关闭文件描述符 0;
        fd = open("/dev/null",O_RDWR); //此时fd=0(open使用可用的最小的，因为0刚>刚关闭了)
        dup2(fd,STDOUT_FILENO);
        dup2(fd,STDERR_FILENO);

        //6. 守护进程逻辑
        while(1)
        {
                printf("哈哈哈 我是被守护的进程\n");
                sleep(5);
        }

        return 0;
}
```

执行文件后即可在后台发现此进程(不受用户登录、注销的影响，一直运行着)，可以使用kill -9 PID  强制结束

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684847022608-099aab63-4bc5-47ca-98c7-b51073ea125c.png)

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684847049580-d66e8e35-d234-4d23-b87f-ffab6d285e1d.png)

### 线程★

##### 线程的概念

进程：有独立的进程地址空间，有独立的pcb

线程：有独立的pcb，没有独立的进程地址空间

ps -Lf 进程id  ---> 线程号 LWP --->cpu执行的最小单位

如果一个进程创建了多个线程，那么它就能更快的去争夺CPU，更快的执行

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684894173072-a7278537-bed1-42f0-8094-ca065aae8260.png)

**线程共享**：

独享 栈空间（内核栈、用户栈）

共享 ./text./data ./rodataa ./bsss heap  ---> 共享【全局变量】（errno不共享）

##### 线程函数

###### pthread_self

```
pthread_t pthread_self();
```

获取线程id，返回值就是本线程的id

###### pthread_create

创建线程，对应fork

```
int pthread_create(pthread_t *thread, const pthread_attr_t *attr, void *(*start_routine) (void *), void *arg);
```

参数一：传出参数，表示新创建的子线程 id，pthread_t 类型的&;

参数二：线程属性，传NULL表示使用默认属性

参数三：子线程的回调函数 void *tfn(void *arg)，创建成功 pthread_create函数返回时，该函数会被自动调用

参数四：参数三函数的参数，如果没有则传NULL

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/types.h>
#include <pthread.h>


//回调函数
void *tfn(void *arg)
{
printf("thread: pid==%d,  wid==%lu\n",getpid(),pthread_self());
return NULL;
}


int main(void)
{
pthread_t tid;

printf("main: pid==%d,  wid==%lu\n",getpid(),pthread_self());
    
//创建线程
int ret = pthread_create(&tid,NULL,tfn,NULL);
if(ret!=0)
{
perror("pthread_create error");
}
sleep(1);

return 0;
}
```

###### 循环创建线程

```c
	#include <stdio.h>  
	#include <stdlib.h>  
	#include <string.h>  
	#include <unistd.h>  
	#include <errno.h>  
	#include <pthread.h>   
	  
	  
	void *tfn(void *arg){  
	    int i = (int)arg;  
	    sleep(i);  
	    printf("--I'm %dth thread: pid = %d, tid = %lu\n",i+1, getpid(), pthread_self());  
	  
	    return NULL;  
	}  
	  
	int main(int argc, char *argv[]){  
	    int i;  
	    int ret;  
        pthread_t tid;  
	      
	    for(i=0;i<5;i++){  
	        ret = pthread_create(&tid, NULL, tfn, (void *)i);  
	        if (ret != 0) {  
            perror("pthread_create error");
            exit(1);
            }  
	    }
        
	    sleep(i);  
	    printf("I'm main, pid = %d, tid = %lu\n", getpid(), pthread_self());  
	  
	    return 0;  
}  
```

编译时会出现类型强转的警告，指针4字节转int的8字节，不过不存在精度损失，忽略就行。

###### pthread_exit

将当前线程退出

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1684981132988-c3fb950b-0150-42f4-bda5-2d6b41386e59.png)

###### pthread_join

阻塞等待线程退出，获取线程退出状态，其作用对应进程中的waitpid()函数；

```
int pthread_join(pthread_t thread, void **retval);
```

**thread 参数用于指定接收哪个线程的返回值；retval 参数表示接收到的返回值，而线程退出的时候返回值**

**void \*类型的，所以我们接收的时候应该使用void \**来解引用，如果 thread 线程没有返回值，又或者我们不需要接收 thread 线程的返回值，可以将 retval 参数置为 NULL。**

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <errno.h>
#include <pthread.h>


//结构体

struct thrd{
int var;
char str[256];
};

//回调函数
void *tfn(void *arg)
{
struct thrd *tval;       //定义了一个tval指针，指向结构体thrd；

tval = malloc(sizeof(tval)); //开辟空间空间大小为sizeof(tval)
                             //即指针变量 tval 自身所占的大小（通常为4或8个字节）
tval->var = 100;
strcpy(tval->str,"hello thread"); //strcpy函数将参数二赋值给参数一

return (void*)tval; //将指向结构体thrd的指针tval传出去
}

int main(void)
{

//创建线程
pthread_t tid;
struct thrd *retval;

int ret = pthread_create(&tid,NULL,tfn,NULL);
if(ret!=0)
{
perror("pthread_create error");
exit(1);
}

//回收线程
ret = pthread_join(tid,(void **)&retval); //参数二来解引用该线程回调函数中的返回值

if(ret!=0)
{
perror("pthread_join error");
exit(1); 
}

printf("child thread exit with var=%d,str=%s\n",retval->var,retval->str);

pthread_exit(NULL);
}
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <errno.h>
#include <pthread.h>

void *tfn(void *arg)
{
    int *hui;
    hui = malloc(sizeof(int));
    *hui = 666;
    return (void*)hui;
}

int main()
{
    pthread_t tid;
    void *retval; //接收返回值

    // 创建线程
    int ret = pthread_create(&tid, NULL, tfn, NULL);
    if(ret == -1)
    {
        perror("pthread_create error");
        exit(1);
    }

    //回收线程
    ret = pthread_join(tid, &retval);
    if(ret != 0)
    {
        perror("pthread_join error");
        exit(1);
    }

    printf("这是线程中定义的hui：%d\n", *(int*)retval);

    // 释放线程返回值所占用的内存
    free(retval);

    pthread_exit(NULL);
}
```

###### pthread_cancel

```
int pthread_cancel(pthread_t thread);
```

杀死(取消)线程，其作用对应进程中的kill函数；

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <errno.h>
#include <pthread.h>

void *tfn(void *arg)
{
while(1)
{
printf("I'm thread,pid:%d,tid:%lu\n",getpid(),pthread_self());
sleep(1);
}

return NULL;
}

int main(void)
{
pthread_t tid;

//创建线程
int ret = pthread_create(&tid,NULL,tfn,NULL);
if(ret!=0)
{
perror("pthread_create error");
exit(1);
}

printf("I'm main,pid:%d,tid:%lu\n",getpid(),pthread_self());
sleep(5);

// 终止线程
ret = pthread_cancel(tid);

while(1);


pthread_exit(NULL);
}
```

###### pthread_detach

```
int pthread_detach(pthread_t thread);
```

实现线程分离，线程终止后会自动清理PCB，无需回收；

thread：待分离的线程id



在线程中perror无效，可以使用：

```
fprintf(stderr,"xxx error:%s\n", strerror(ret));
```

##### 线程使用注意事项

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685096792529-7c19fed0-e3e6-4099-9f16-3dc6725faff8.png)

##### 线程同步

###### 线程同步概念

协同步调，对公共区域数据按序访问。防止数据混乱，产生与时间有关的错误。

数据混乱的原因：

1. 资源共享(独享资源则不会)
2. 调度随机(意味着数据访问会出现竞争)
3. 线程间缺乏必要同步机制

###### 互斥锁 mutex

Liunx中提供一把互斥锁 mutex（也称之为互斥量）

每个线程在对资源操作前都尝试先加锁，成功加锁才能操作，操作结束后解锁

资源还是共享的，线程间也还是竞争的

但通过"锁"就将资源的访问变成互斥操作 而后与时间有关的错误也不会在产生了

**建议锁！对公共数据进行保护，所以线程应该在访问公共数据前先拿锁在访问，但是锁本身不具备强制性**

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685150813911-a39b75e3-077c-40e9-b337-1caec8dad538.png)

下面是一个小例子，数据共享未加锁导致的混乱：

因为主线程和子线程打印输出一句话后就sleep了，那么cpu此时挂起，等睡眠结束后 谁抢夺到cpu就去打印谁

```c
#include <stdio.h>
#include <string.h>
#include <pthread.h>
#include <stdlib.h>
#include <unistd.h>

//子线程
void *tfn(void *arg)
{
srand(time(NULL));

while(1)
{
printf("hello ");
sleep(rand() % 3);
printf("world\n");
sleep(rand() % 3);
}

return NULL;
}

int main(void)
{
pthread_t tid;
srand(time(NULL));

// 创建线程
pthread_create(&tid,NULL,tfn,NULL);
while(1)
{
printf("HELLO ");
sleep(rand() % 3);
printf("WORLD\n");
sleep(rand() % 3);
}

//回收线程
pthread_join(tid,NULL);

return 0;
}
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685152690527-ba9d30fb-1bc9-4220-a5ab-91ed14797c83.png)



**互斥锁的主要函数**：

pthread_mutex_init           函数

pthread_mutex_destory    函数

pthread_mutex_lock          函数

pthread_mutex_trylock      函数

pthread_mutex_unlock      函数

pthread_mutex_t               类型

以上5个函数的返回值都是：成功返回0，失败返回错误号；

**加锁步骤**：

1. pthread_mutex_t  lock；创建锁
2. pthread_mutex_init；初始化
3. pthread_mutex_lock；加锁
4. 访问共享数据
5. pthread_mutex_unlock；解锁
6. pthread_mutex_destroy；销毁锁

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685154669558-eb9bb105-4ba3-404a-96b3-631a56f33cb2.png)

```c
#include <stdio.h>
#include <string.h>
#include <pthread.h>
#include <stdlib.h>
#include <unistd.h>

pthread_mutex_t mutex; //定义一把互斥锁

//子线程
void *tfn(void *arg)
{
srand(time(NULL));

while(1)
{
pthread_mutex_lock(&mutex); //访问公共数据前加锁
    
printf("hello ");
sleep(rand() % 3);
printf("world\n");
    
pthread_mutex_unlock(&mutex); //解锁
sleep(rand() % 3);
}
return NULL;
}

int main(void)
{
pthread_t tid;
srand(time(NULL));

pthread_mutex_init(&mutex,NULL);  //初始化锁

// 创建线程
pthread_create(&tid,NULL,tfn,NULL);
while(1)
{
pthread_mutex_lock(&mutex); //访问公共数据前加锁
    
printf("HELLO ");
sleep(rand() % 3);
printf("WORLD\n");
    
pthread_mutex_unlock(&mutex); //解锁
sleep(rand() % 3);
}
//回收线程
pthread_join(tid,NULL);

pthread_mutex_destroy(&mutex); //销毁锁

return 0;
}
```

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685154199805-29011b68-01a9-44a9-b9be-bcc6f742b369.png)

###### 读写锁 rwlock

读写锁与互斥锁类似，但读写锁允许更高的并行性，其特性为：**写独占 读共享**。写锁优先级高

锁只有一把，以读方式给数据加锁--读锁，以写方式给数据加锁--写锁，

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685155839195-46407606-8508-4690-a352-eb805ed5564b.png)

函数：

pthread_rwlock_t  rwlock;

pthread_rwlock_init(&rwlock, NULL);

pthread_rwlock_rdlock(&rwlock);    try

pthread_rwlock_wrlock(&rwlock);    try

pthread_rwlock_unlock(&rwlock);

pthread_rwlock_destroy(&rwlock);

```c
1.	/* 3个线程不定时 "写" 全局资源，5个线程不定时 "读" 同一全局资源 */  
2.	  
3.	#include <stdio.h>  
4.	#include <unistd.h>  
5.	#include <pthread.h>  
6.	  
7.	int counter;                          //全局资源  
8.	pthread_rwlock_t rwlock;  
9.	  
10.	void *th_write(void *arg)  
11.	{  
12.	    int t;  
13.	    int i = (int)arg;  
14.	  
15.	    while (1) {  
16.	        t = counter;                    // 保存写之前的值  
17.	        usleep(1000);  
18.	  
19.	        pthread_rwlock_wrlock(&rwlock);  
20.	        printf("=======write %d: %lu: counter=%d ++counter=%d\n", i, pthread_self(), t, ++counter);  
21.	        pthread_rwlock_unlock(&rwlock);  
22.	  
23.	        usleep(9000);               // 给 r 锁提供机会  
24.	    }  
25.	    return NULL;  
26.	}  
27.	  
28.	void *th_read(void *arg)  
29.	{  
30.	    int i = (int)arg;  
31.	  
32.	    while (1) {  
33.	        pthread_rwlock_rdlock(&rwlock);  
34.	        printf("----------------------------read %d: %lu: %d\n", i, pthread_self(), counter);  
35.	        pthread_rwlock_unlock(&rwlock);  
36.	  
37.	        usleep(2000);                // 给写锁提供机会  
38.	    }  
39.	    return NULL;  
40.	}  
41.	  
42.	int main(void)  
43.	{  
44.	    int i;  
45.	    pthread_t tid[8];  
46.	  
47.	    pthread_rwlock_init(&rwlock, NULL);  
48.	  
49.	    for (i = 0; i < 3; i++)  
50.	        pthread_create(&tid[i], NULL, th_write, (void *)i);  
51.	  
52.	    for (i = 0; i < 5; i++)  
53.	        pthread_create(&tid[i+3], NULL, th_read, (void *)i);  
54.	  
55.	    for (i = 0; i < 8; i++)  
56.	        pthread_join(tid[i], NULL);  
57.	  
58.	    pthread_rwlock_destroy(&rwlock);            //释放读写琐  
59.	  
60.	    return 0;  
61.	}  
```

### 条件变量

条件变量本身不是锁，但它也可以造成线程阻塞，通常与互斥锁配合使用，给多线程提供一个会合的场所。

##### 主要应用函数

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685172081989-705f1340-9132-4c81-a95d-0cf9f229e8b2.png)

###### wait

阻塞等待一个条件变量；

pthread_cond_wait(&cond, &mutex);

作用：

1.  阻塞等待条件变量满足
2. 解锁已经加锁成功的信号量 （相当于 pthread_mutex_unlock(&mutex)），1 2两步为一个原子操作(一起执行，不可分割)
3. 当条件满足，函数返回时，解除阻塞并重新申请获取互斥锁。重新加锁信号量 （相当于pthread_mutex_lock(&mutex);）

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685174054873-af74ac91-a406-46c3-b33e-97fe31b7877d.png)

##### 条件变量的生产者消费者模型分析

![img](https://cdn.nlark.com/yuque/0/2023/png/28009832/1685175574165-2ef3c5c8-bfdb-4c1b-bf50-4c35a1a00cc4.png)

##### 条件变量的生产者消费者代码实现

```c
1.#include <stdio.h>  
2.#include <stdlib.h>  
3.#include <string.h>  
4.#include <unistd.h>  
5.#include <errno.h>  
6.#include <pthread.h>  
7.  
8.void err_thread(int ret, char *str)  
9.{  
10.    if (ret != 0) {  
11.        fprintf(stderr, "%s:%s\n", str, strerror(ret));  
12.        pthread_exit(NULL);  
13.    }  
14.}  
15.  
16.struct msg {  
17.    int num;  
18.    struct msg *next;  
19.};  
20.  
21.struct msg *head;  
22.  
23.pthread_mutex_t mutex = PTHREAD_MUTEX_INITIALIZER;      // 定义/初始化一个互斥量  
24.pthread_cond_t has_data = PTHREAD_COND_INITIALIZER;      // 定义/初始化一个条件变量  
25.  
26.void *produser(void *arg)  
27.{  
28.    while (1) {  
29.        struct msg *mp = malloc(sizeof(struct msg));  
30.  
31.        mp->num = rand() % 1000 + 1;                        // 模拟生产一个数据`  
32.        printf("--produce %d\n", mp->num);  
33.  
34.        pthread_mutex_lock(&mutex);                         // 加锁 互斥量  
35.        mp->next = head;                                    // 写公共区域  
36.        head = mp;  
37.        pthread_mutex_unlock(&mutex);                       // 解锁 互斥量  
38.  
39.        pthread_cond_signal(&has_data);                     // 唤醒阻塞在条件变量 has_data上的线程.  
40.  
41.        sleep(rand() % 3);  
42.    }  
43.  
44.    return NULL;  
45.}  
46.  
47.void *consumer(void *arg)  
48.{  
49.    while (1) {  
50.        struct msg *mp;  
51.  
52.        pthread_mutex_lock(&mutex);                         // 加锁 互斥量  
53.        if (head == NULL) {  
54.            pthread_cond_wait(&has_data, &mutex);           // 阻塞等待条件变量, 解锁  
55.        }                                                   // pthread_cond_wait 返回时, 重写加锁 mutex  
56.  
57.        mp = head;  
58.        head = mp->next;  
59.  
60.        pthread_mutex_unlock(&mutex);                       // 解锁 互斥量  
61.        printf("---------consumer:%d\n", mp->num);  
62.  
63.        free(mp);  
64.        sleep(rand()%3);  
65.    }  
66.  
67.    return NULL;  
68.}  
69.  
70.int main(int argc, char *argv[])  
71.{  
72.    int ret;  
73.    pthread_t pid, cid;  
74.  
75.    srand(time(NULL));  
76.  
77.    ret = pthread_create(&pid, NULL, produser, NULL);           // 生产者  
78.    if (ret != 0)   
79.        err_thread(ret, "pthread_create produser error");  
80.  
81.    ret = pthread_create(&cid, NULL, consumer, NULL);           // 消费者  
82.    if (ret != 0)   
83.        err_thread(ret, "pthread_create consuer error");  
84.  
85.    pthread_join(pid, NULL);  
86.    pthread_join(cid, NULL);  
87.  
88.    return 0;  
89.}  
```
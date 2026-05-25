---
title: CMD-命令提示符简介及常用命令
categories:
  - [计算机]
  - [Windows, CMD]
  - [Windows, 批处理]
tags:
  - 计算机
  - CMD
  - Windows
  - 批处理
  - batch
abbrlink: 980c
date: 2021-02-28 13:41:25
---
## 简介
Windows 命令提示符（cmd.exe）是 [Windows NT](https://baike.so.com/doc/5508294-5744040.html) 下的一个用于运行 Windows 控制面板程序或某些 DOS 程序的shell程序；或在 Windows CE 下只用于运行控制面板程序的外壳程序。      

## 常用命令
<table>
 <tr>
    <td><b><center>命令名称</center></b></td>
    <td><b><center>命令含义</center></b></td>
	<td><b><center>使用方法</center></b></td>
	</b>
 </tr>
 <tr>
	<td>help</td>
	<td>获取帮助文档</td>
	<td>有关某个命令的详细信息，请键入 HELP [命令名]。</td>
 </tr>
 <tr>
 	<td>cd</td>
 	<td>显示当前目录名或改变当前目录</td>
 	<td>CD [/D] [drive:][path]</td>
 </tr>
 <tr>
 	<td>dir</td>
 	<td>列出目录和文件名</td>
 	<td></td>
 </tr>
 <tr>
 	<td>echo</td>
 	<td>显示消息，或者启用或关闭命令回显。</td>
 	<td></td>
 </tr>
 <tr>
 	<td>rem</td>
 	<td>在批处理文件或 CONFIG.SYS 里加上注解或说明。</td>
 	<td>rem [comment]</td>
 </tr>
 <tr>
 	<td>xcopy</td>
 	<td>拷贝目录和文件</td>
 	<td></td>
 </tr>
</table>

### Help命令
输入help命令，显示CMD的命令列表。
``` [CMD] [CMD Help 命令] 
C:\Users\dell>help
有关某个命令的详细信息，请键入 HELP 命令名
ASSOC          显示或修改文件扩展名关联。
ATTRIB         显示或更改文件属性。
BREAK          设置或清除扩展式 CTRL+C 检查。
BCDEDIT        设置启动数据库中的属性以控制启动加载。
CACLS          显示或修改文件的访问控制列表(ACL)。
CALL           从另一个批处理程序调用这一个。
CD             显示当前目录的名称或将其更改。
CHCP           显示或设置活动代码页数。
CHDIR          显示当前目录的名称或将其更改。
CHKDSK         检查磁盘并显示状态报告。
CHKNTFS        显示或修改启动时间磁盘检查。
CLS            清除屏幕。
CMD            打开另一个 Windows 命令解释程序窗口。
COLOR          设置默认控制台前景和背景颜色。
COMP           比较两个或两套文件的内容。
COMPACT        显示或更改 NTFS 分区上文件的压缩。
CONVERT        将 FAT 卷转换成 NTFS。你不能转换
               当前驱动器。
COPY           将至少一个文件复制到另一个位置。
DATE           显示或设置日期。
DEL            删除至少一个文件。
DIR            显示一个目录中的文件和子目录。
DISKPART       显示或配置磁盘分区属性。
DOSKEY         编辑命令行、撤回 Windows 命令并
               创建宏。
DRIVERQUERY    显示当前设备驱动程序状态和属性。
ECHO           显示消息，或将命令回显打开或关闭。
ENDLOCAL       结束批文件中环境更改的本地化。
ERASE          删除一个或多个文件。
EXIT           退出 CMD.EXE 程序(命令解释程序)。
FC             比较两个文件或两个文件集并显示
               它们之间的不同。
FIND           在一个或多个文件中搜索一个文本字符串。
FINDSTR        在多个文件中搜索字符串。
FOR            为一组文件中的每个文件运行一个指定的命令。
FORMAT         格式化磁盘，以便用于 Windows。
FSUTIL         显示或配置文件系统属性。
FTYPE          显示或修改在文件扩展名关联中使用的文件
               类型。
GOTO           将 Windows 命令解释程序定向到批处理程序
               中某个带标签的行。
GPRESULT       显示计算机或用户的组策略信息。
GRAFTABL       使 Windows 在图形模式下显示扩展
               字符集。
HELP           提供 Windows 命令的帮助信息。
ICACLS         显示、修改、备份或还原文件和
               目录的 ACL。
IF             在批处理程序中执行有条件的处理操作。
LABEL          创建、更改或删除磁盘的卷标。
MD             创建一个目录。
MKDIR          创建一个目录。
MKLINK         创建符号链接和硬链接
MODE           配置系统设备。
MORE           逐屏显示输出。
MOVE           将一个或多个文件从一个目录移动到另一个
               目录。
OPENFILES      显示远程用户为了文件共享而打开的文件。
PATH           为可执行文件显示或设置搜索路径。
PAUSE          暂停批处理文件的处理并显示消息。
POPD           还原通过 PUSHD 保存的当前目录的上一个
               值。
PRINT          打印一个文本文件。
PROMPT         更改 Windows 命令提示。
PUSHD          保存当前目录，然后对其进行更改。
RD             删除目录。
RECOVER        从损坏的或有缺陷的磁盘中恢复可读信息。
REM            记录批处理文件或 CONFIG.SYS 中的注释(批注)。
REN            重命名文件。
RENAME         重命名文件。
REPLACE        替换文件。
RMDIR          删除目录。
ROBOCOPY       复制文件和目录树的高级实用工具
SET            显示、设置或删除 Windows 环境变量。
SETLOCAL       开始本地化批处理文件中的环境更改。
SC             显示或配置服务(后台进程)。
SCHTASKS       安排在一台计算机上运行命令和程序。
SHIFT          调整批处理文件中可替换参数的位置。
SHUTDOWN       允许通过本地或远程方式正确关闭计算机。
SORT           对输入排序。
START          启动单独的窗口以运行指定的程序或命令。
SUBST          将路径与驱动器号关联。
SYSTEMINFO     显示计算机的特定属性和配置。
TASKLIST       显示包括服务在内的所有当前运行的任务。
TASKKILL       中止或停止正在运行的进程或应用程序。
TIME           显示或设置系统时间。
TITLE          设置 CMD.EXE 会话的窗口标题。
TREE           以图形方式显示驱动程序或路径的目录
               结构。
TYPE           显示文本文件的内容。
VER            显示 Windows 的版本。
VERIFY         告诉 Windows 是否进行验证，以确保文件
               正确写入磁盘。
VOL            显示磁盘卷标和序列号。
XCOPY          复制文件和目录树。
WMIC           在交互式命令 shell 中显示 WMI 信息。

有关工具的详细信息，请参阅联机帮助中的命令行参考。
```

### ECHO命令
ECHO命令的使用方法：
``` [CMD] [CMD ECHO 命令]
C:\Users\dell>echo /?
显示消息，或者启用或关闭命令回显。

  ECHO [ON | OFF]
  ECHO [message]

若要显示当前回显设置，请键入不带参数的 ECHO。
```
### PAUSE命令
PAUSE命令的使用方法：
``` [CMD] [CMD PAUSE 命令]
C:\Users\dell>pause /?
暂停批处理程序，并显示以下消息:
    请按任意键继续. . .
```
### TITLE命令
TITLE命令的使用方法：
``` [CMD] [CMD TITLE 命令]
C:\Users\dell>title /?
设置命令提示窗口的窗口标题。

TITLE [string]

  string       指定命令提示窗口的标题。
```
### CD命令
CD命令的使用方法：
``` [CMD] [CMD CD 命令]
C:\Users\dell>help cd
显示当前目录名或改变当前目录。

CHDIR [/D] [drive:][path]
CHDIR [..]
CD [/D] [drive:][path]
CD [..]

  ..   指定要改成父目录。

键入 CD drive: 显示指定驱动器中的当前目录。
不带参数只键入 CD，则显示当前驱动器和目录。

使用 /D 开关，除了改变驱动器的当前目录之外，
还可改变当前驱动器。

如果命令扩展被启用，CHDIR 会如下改变:

当前的目录字符串会被转换成使用磁盘名上的大小写。所以，
如果磁盘上的大小写如此，CD C:\TEMP 会将当前目录设为
C:\Temp。

CHDIR 命令不把空格当作分隔符，因此有可能将目录名改为一个
带有空格但不带有引号的子目录名。例如:

     cd \winnt\profiles\username\programs\start menu

与下列相同:

     cd "\winnt\profiles\username\programs\start menu"

在扩展停用的情况下，你必须键入以上命令。
```

### DIR命令
DIR命令的使用方法：
``` [CMD] [CMD DIR 命令]
C:\Users\dell>help dir
显示目录中的文件和子目录列表。

DIR [drive:][path][filename] [/A[[:]attributes]] [/B] [/C] [/D] [/L] [/N]
  [/O[[:]sortorder]] [/P] [/Q] [/R] [/S] [/T[[:]timefield]] [/W] [/X] [/4]

  [drive:][path][filename]
              指定要列出的驱动器、目录和/或文件。

  /A          显示具有指定属性的文件。
  属性         D  目录                R  只读文件
               H  隐藏文件            A  准备存档的文件
               S  系统文件            I  无内容索引文件
               L  重新分析点          O  脱机文件
               -  表示“否”的前缀
  /B          使用空格式(没有标题信息或摘要)。
  /C          在文件大小中显示千位数分隔符。这是默认值。用 /-C 来
              禁用分隔符显示。
  /D          跟宽式相同，但文件是按栏分类列出的。
  /L          用小写。
  /N          新的长列表格式，其中文件名在最右边。
  /O          用分类顺序列出文件。
  排列顺序     N  按名称(字母顺序)     S  按大小(从小到大)
               E  按扩展名(字母顺序)   D  按日期/时间(从先到后)
               G  组目录优先           -  反转顺序的前缀
  /P          在每个信息屏幕后暂停。
  /Q          显示文件所有者。
  /R          显示文件的备用数据流。
  /S          显示指定目录和所有子目录中的文件。
  /T          控制显示或用来分类的时间字符域
  时间段      C  创建时间
              A  上次访问时间
              W  上次写入的时间
  /W          用宽列表格式。
  /X          显示为非 8dot3 文件名产生的短名称。格式是 /N 的格式，
              短名称插在长名称前面。如果没有短名称，在其位置则
              显示空白。
  /4          以四位数字显示年份

可以在 DIRCMD 环境变量中预先设定开关。通过添加前缀 - (破折号)
来替代预先设定的开关。例如，/-W。
```
### PING命令
PING命令的使用方法：
```[CMD] [CMD PING 命令]
C:\Users\dell>ping /?

用法: ping [-t] [-a] [-n count] [-l size] [-f] [-i TTL] [-v TOS]
            [-r count] [-s count] [[-j host-list] | [-k host-list]]
            [-w timeout] [-R] [-S srcaddr] [-c compartment] [-p]
            [-4] [-6] target_name

选项:
    -t             Ping 指定的主机，直到停止。
                   若要查看统计信息并继续操作，请键入 Ctrl+Break；
                   若要停止，请键入 Ctrl+C。
    -a             将地址解析为主机名。
    -n count       要发送的回显请求数。
    -l size        发送缓冲区大小。
    -f             在数据包中设置“不分段”标记(仅适用于 IPv4)。
    -i TTL         生存时间。
    -v TOS         服务类型(仅适用于 IPv4。该设置已被弃用，
                   对 IP 标头中的服务类型字段没有任何
                   影响)。
    -r count       记录计数跃点的路由(仅适用于 IPv4)。
    -s count       计数跃点的时间戳(仅适用于 IPv4)。
    -j host-list   与主机列表一起使用的松散源路由(仅适用于 IPv4)。
    -k host-list    与主机列表一起使用的严格源路由(仅适用于 IPv4)。
    -w timeout     等待每次回复的超时时间(毫秒)。
    -R             同样使用路由标头测试反向路由(仅适用于 IPv6)。
                   根据 RFC 5095，已弃用此路由标头。
                   如果使用此标头，某些系统可能丢弃
                   回显请求。
    -S srcaddr     要使用的源地址。
    -c compartment 路由隔离舱标识符。
    -p             Ping Hyper-V 网络虚拟化提供程序地址。
    -4             强制使用 IPv4。
    -6             强制使用 IPv6。
```

### XCOPY命令
XCOPY命令的使用方法：
``` [CMD] [CMD XCOPY 命令]
C:\Users\dell>xcopy /?
复制文件和目录树。

XCOPY source [destination] [/A | /M] [/D[:date]] [/P] [/S [/E]] [/V] [/W]
                           [/C] [/I] [/Q] [/F] [/L] [/G] [/H] [/R] [/T] [/U]
                           [/K] [/N] [/O] [/X] [/Y] [/-Y] [/Z] [/B] [/J]
                           [/EXCLUDE:file1[+file2][+file3]...] [/COMPRESS]

  source       指定要复制的文件。
  destination  指定新文件的位置和/或名称。
  /A           仅复制有存档属性集的文件，
               但不更改属性。
  /M           仅复制有存档属性集的文件，
               并关闭存档属性。
  /D:m-d-y     复制在指定日期或指定日期以后更改的文件。
               如果没有提供日期，则只复制
               源时间比目标时间新的文件。
  /EXCLUDE:file1[+file2][+file3]...
               指定含有字符串的文件列表。每个字符串
               在文件中应位于单独的一行。如果任何
               字符串与复制文件的绝对路径的任何部分相符，
               则排除复制该文件。例如，
               指定如 \obj\ 或 .obj 的字符串会分别
               排除目录 obj 下面的所有文件或带有
               .obj 扩展名的所有文件。
  /P           创建每个目标文件之前均进行提示。
  /S           复制目录和子目录，不包括空目录。
  /E           复制目录和子目录，包括空目录。
               与 /S /E 相同。可以用来修改 /T。
  /V           验证每个新文件的大小。
  /W           提示在复制前按键。
  /C           即使有错误，也继续复制。
  /I           如果目标不存在，且要复制多个文件，
               则假定目标必须是目录。
  /Q           复制时不显示文件名。
  /F           复制时显示完整的源文件名和目标文件名。
  /L           显示要复制的文件。
  /G           允许将加密文件复制到
               不支持加密的目标。
  /H           隐藏文件和系统文件也会复制。
  /R           覆盖只读文件。
  /T           创建目录结构，但不复制文件。不
               包括空目录或子目录。/T /E 包括
               空目录和子目录。
  /U           只复制已经存在于目标中的文件。
  /K           复制属性。一般的 Xcopy 会重置只读属性。
  /N           用生成的短名称复制。
  /O           复制文件所有权和 ACL 信息。
  /X           复制文件审核设置(隐含 /O)。
  /Y           取消提示以确认要覆盖
               现有目标文件。
  /-Y          触发提示，以确认要覆盖
               现有目标文件。
  /Z           在可重新启动模式下复制网络文件。
  /B           复制符号链接本身与链接目标。
  /J           复制时不使用缓冲的 I/O。推荐复制大文件时使用。
  /COMPRESS    如果适用，在传输期间请求网络
               压缩。

开关 /Y 可以预先在 COPYCMD 环境变量中设置。
这可能被命令行上的 /-Y 覆盖。
```

### TREE命令
以图形显示驱动器或路径的文件夹结构。

TREE命令的使用方法:
``` [CMD] [CMD TREE 命令]
TREE [drive:][path] [/F] [/A]

   /F   显示每个文件夹中文件的名称。
   /A   使用 ASCII 字符，而不使用扩展字符。
```

## 批处理
[批处理](https://baike.so.com/doc/3361951-3539709.html)(Batch)，就是对某对象进行批量的处理。批处理文件的扩展名为bat 。​批处理（Batch）实际上是一种简化的[脚本语言](https://baike.so.com/doc/2874347-3033293.html#2874347-3033293-1)，也称作宏，它应用于DOS和Windows系统中，它是由DOS或者Windows系统内嵌的命令解释器（通常是COMMAND.COM或者CMD.EXE）解释运行。类似于Unix中的Shell脚本。批处理文件具有.bat或者.cmd的扩展名，其最简单的例子，是逐行书写在命令行中会用到的各种命令。更复杂的情况，需要使用 if，for，goto等命令控制程序的运行过程，如同C，Basic等高级语言一样。如果需要实现更复杂的应用，利用外部程序是必要的，这包括系统本身提供的外部命令和第三方提供的工具或者软件。批处理程序虽然是在命令行环境中运行，但不仅仅能使用命令行软件，任何32位的Windows程序都可以放在批处理文件中运行。

**批处理特点：**
1. 批处理在计算机安全攻防中，是必要技能，黑客一般都懂DOS命令即批处理命令，例如：`ping`，`ipconfig /all`，`net`，`telnet`，etc. 
2. 一般的批处理文件直接改扩展名（即文件后缀名），即可反编译查看源码。 
3. DOS程序运行完后都有返回码，有助于调试程序。 
4. .编辑批处理命令，所有字符必须在英文格式和半角状态下。 
5. .批处理只认行、不认命令数。即批处理对断行很敏感，而对一行之中包含多少命令却无所谓，只要用`&` `&&` `|` `||`等连接即可。
6. "-"和"/"等价。（-：dash，/：slash，\：backslash【英文普及下，多加一个反斜杠】），例如：`shutdown /s`等价于`shutdown -s`。 
7. 查看帮助。可以使用 `help`，如 `help dir`。或者使用 `/?`，如 `for /?`。将调出的帮助信息存储到文件中，方法如下：`help /? > help.txt` 就可以在当前目录得到一个help.txt的文本，内含`help`命令的帮助信息。

### 批处理中的变量和参数
批处理中的变量分为两类：系统变量和自定义变量。

系统变量的值由系统将其根据事先定义的条件自动赋值，即这些变量系统已经给它们定义了值，不需要给它赋值，只需要调用即可。系统变量具体如下：

变量名称|本地/系统|含义
----|---|---
%ALLUSERSPROFILE%|本地|返回 "所有用户" 配置文件的位置
%APPDATA%|本地|返回默认情况下应用程序存储数据的位置
%CD%|本地|返回当前目录字符串。也就是获得当前路径，并将其转换为字符串
%CMDCMDLINE% |本地|返回用来启动当前的 cmd.exe 的准确命令行
%CMDEXTVERSION%|系统|返回当前的 "命令处理程序扩展" 的版本号
%COMPUTERNAME%|系统|返回计算机名称
%COMSPEC%|系统|返回命令行解释器可执行程序的准确路径。也就是返回 cmd.exe 的路径，一般在 C:\WINDOWS\system32\cmd.exe
%DATE%|系统|返回当前日期字符串。和使用 date/t 效果一样
%ERRORLEVEL% |系统|返回上一条命令的错误代码。通常用 0 表示正确，非0 表示错误
%HOMEDRIVE% |系统|返回连接到用户主目录的本地工作站驱动器号。基于主目录值而设置。用户主目录是在 "本地用户和组" 中指定的
%HOMEPATH% |系统|返回用户主目录的完整路径。基于主目录值而设置。用户主目录是在 "本地用户和组" 中指定的
%HOMESHARE%|系统|返回用户的共享目录的网络路径。基于主目录值而设置。用户主目录是在 "本地用户和组" 中指定的
%LOGONSERVER%|系统|返回验证当前登录会话的域控制器的名称
%NUMBER_OF_PROCESSORS%|系统|显示安装在计算机上的处理器数目(所有 CPU 的总核心数)
%OS%|系统|返回操作系统名称
%PATH%|系统|指定可执行文件的搜索路径。也就是在这些目录下的可执行文件 （不仅仅是.exe，可以用 `echo` `%PATHEXT%` 查看哪些属于可执行文件。）可以直接在开始-->运行里直接执行，当然也可以在命令提示符、批处理中直接执行。例如记事本文件位于 C:\WINDOWS\NOTEPAD.EXE ，那么我们点击 "开始-->运行，输入 NOTEPAD " 就可以打开记事本了。或者我们打开 CMD 窗口 ，直接输入 NOTEPAD 也可以打开记事本。
%PATHEXT%|系统|返回操作系统认为可执行的文件扩展名的列表
%PROCESSOR_ARCHITECTURE%|系统|返回处理器的芯片体系结构。返回值为 x86 或 IA64 或 RISC。这些都是常见的架构 ，或者称作指令集。Windows 操作系统都是基于 x86 架构开发的，国产CPU 不是采用 x86 指令集 ，所以无法运行 Windows。
%PROCESSOR_IDENTFIER%|系统|返回处理器说明
%PROCESSOR_LEVEL%|系统|返回计算机上安装的处理器型号
%PROCESSOR_REVISION%|系统|返回处理器版本号
%PROMPT%|本地|返回当前解释程序的命令提示符设置。由 cmd.exe 生成。
%RANDOM% |系统|返回 0 到 32767 之间的任意十进制数字。由 cmd.exe 生成。
%SYSTEMDRIVE%|系统|返回包含Windows server operation system根目录（即系统根目录）的驱动器
%SYSTEMROOT%|系统|返回 Windows server operation system 根目录位置
%TEMP% 和 %TMP%|系统-用户|返回对当前登录用户可用的应用程序所使用的默认临时目录。有些应用程序需要 TEMP，而其他应用程序则需要 TMP
%TIME%|系统|返回当前时间字符串。使用与 `time /t` 命令相同的格式
%USERDOMAIN%|本地|返回包含用户账户的域的名称
%USERNAME%|本地|返回当前登录的用户的名称
%USERPROFILE%|本地|返回当前用户的配置文件的位置
%WINDIR%|系统|返回操作系统目录的位置

### 批处理（.bat）文件的创建和编码
- 用记事本（Notepad）就可以编写代码，输入完代码后，记得检查修改文件编码，然后把记事本文件（.txt）扩展名改为批处理文件扩展名（.bat）。
- 在中文Windows中，不能把批处理文件编码设为 UTF-8，而需要修改编码为 ANSI 或设置文件编码为 GBK
- 默认文件编码为 UTF-8 将导致批处理文件显示效果为乱码。
---
**参考链接：**
1. http://dwz.date/esuZ
2. https://baike.so.com/doc/3361951-3539709.html
3. [DOS批处理前言](https://www.cnblogs.com/siwuxie095/p/6200757.html).siwuxie095
4. [批处理中的变量和参数（一）](https://www.cnblogs.com/siwuxie095/p/6351210.html).siwuxie095
5. [批处理中的变量和参数（二）](https://www.cnblogs.com/siwuxie095/p/6358173.html).siwuxie095
6. https://baike.so.com/doc/5508294-5744040.html
7. [bat文件的中文乱码](https://www.cnblogs.com/siwuxie095/p/6219673.html).siwuxie095
8. [pause和title](https://www.cnblogs.com/siwuxie095/p/6219851.html).siwuxie095
9. [echo](https://www.cnblogs.com/siwuxie095/p/6204636.html).siwuxie095

*本文章仅供个人学习、研究或者欣赏所用。*
# /bin/bash 和/bin/sh的区别

### SH：

sh就是Bourne shell
 这个是UNIX标准的默认shell，对它评价是concise简洁 compact紧凑  fast高效，由AT&T编写，属于系统管理shell

### BASH:

bash是 GNU Bourne-Again SHell  (GNU 命令解释程序 “Bourne二世”)
 是linux标准的默认shell ，它基于Bourne shell，吸收了C shell和Korn shell的一些特性。bash是Bourne shell的超集，bash完全兼容Bourne shell,也就是说用Bourne shell的脚本不加修改可以在bash中执行，反过来却不行，bash的脚本在sh上运行容易报语法错误。

```
来源https://www.jianshu.com/p/070bd0b4855f
```

# 语法

在shell脚本中,变量赋值前后不要有空格

```shell
#e.g.
time1=$(date "+%Y%m%d%H%M%S")
```

## 获取命令行参数

test.sh

```shell
#!/bin/bash

echo $1
```

调用

```
~ ./test.sh  william
william
~ 
```

## &&   ||

```
1为true才执行2
command1 &&  command2 
3为flase才执行4
command3 || command4
```

## \$PWD

和 $(pwd)等效，环境变量，表示当前工作路径

和pwd是不同的，pwd是命令
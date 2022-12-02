# About gcc

-o :

```text
生成指定的输出文件。用在生成可执行文件时。
```

-g :

```text
以操作系统本地格式生成调试信息, GNU 调试器可利用该信息。
```

-O / -O1 :

```text
优化生成的代码
```

-O0 :

```text
不进行优化处理
```

-O2 :

```text
进一步优化
```

-O3 :

```text
比 -O2 更进一步优化，包括 inline 函数
```

-I

```text
Add the directory dir to the head of the list of directories to be
searched for header files.


在你是用 #include "file" 的时候, gcc/g++ 会先在当前目录查找你所制定的头文件,
如果没有找到, 他回到默认的头文件目录找, 如果使用 -I 制定了目录,他会先在你所制定的目录查找, 
然后再按常规的顺序去找。对于 #include<file>, gcc/g++ 会到 -I 制定的目录查找, 查找不到, 然后将到系统的默认的头文件目录查找 。
```

-l :

```text
指定链接库的名称, etc: -l math, will find: libmath.so or libmath.a
```

-Wall

```text
生成所有警告信息
```

-w

```text
不生成任何警告信息
```

CFLAGS :

```text
表示用于 C 编译器的选项, etc:
```

```shell
CFLAGS = -g -O2 -Wall -I$(LUA_INC) $(MYCFLAGS)
gcc $(CFLAGS)
```

[参考资料](https://www.runoob.com/w3cnote/gcc-parameter-detail.html)

# About gcc

-g :

```text
以操作系统本地格式产生调试信息, -O2 : 默认优化级别是 O2 , -Wall : 开启调试信息
```

-I

```text
Add the directory dir to the head of the list of directories to be
searched for header files.


在你是用 #include "file" 的时候, gcc/g++ 会先在当前目录查找你所制定的头文件,
如果没有找到, 他回到默认的头文件目录找, 如果使用 -I 制定了目录,他会先在你所制定的目录查找, 
然后再按常规的顺序去找。对于 #include<file>, gcc/g++ 会到 -I 制定的目录查找, 查找不到, 然后将到系统的默认的头文件目录查找 。
```

CFLAGS :

```text
表示用于 C 编译器的选项, etc:
```

```shell
CFLAGS = -g -O2 -Wall -I$(LUA_INC) $(MYCFLAGS)
gcc $(CFLAGS)
```

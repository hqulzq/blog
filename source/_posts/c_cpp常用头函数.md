---
title: c/c++常用头函数
date: 2025-02-18 23:15:24
tags:
  - 头函数
categories:
  - C_CPP
---

## C

```C
#include <assert.h>　　　　//设定插入点
#include <ctype.h>　　　　 //字符处理
#include <errno.h>　　　　 //定义错误码
#include <float.h>　　　　 //浮点数处理
#include <iso646.h>        //对应各种运算符的宏
#include <limits.h>　　　　//定义各种数据类型最值的常量
#include <locale.h>　　　　//定义本地化C函数
#include <math.h>　　　　　//定义数学函数
#include <setjmp.h>        //异常处理支持
#include <signal.h>        //信号机制支持
#include <stdarg.h>        //不定参数列表支持
#include <stddef.h>        //常用常量
#include <stdio.h>　　　　 //定义输入／输出函数
#include <stdlib.h>　　　　//定义杂项函数及内存分配函数
#include <string.h>　　　　//字符串处理
#include <time.h>　　　　　//定义关于时间的函数
#include <wchar.h>　　　　 //宽字符处理及输入／输出
#include <wctype.h>　　　　//宽字符分类
```
<!-- more -->
### 头文件 ctype.h

字符处理函数: 本类别函数用于对单个字符进行处理，包括字符的类别测试和字符的大小写转换

```txt
字符测试是否字母和数字 isalnum
是否字母 isalpha
是否控制字符 iscntrl
是否数字 isdigit
是否可显示字符(除空格外) isgraph
是否可显示字符(包括空格) isprint
是否既不是空格，又不是字母和数字的可显示字符 ispunct
是否空格 isspace
是否大写字母 isupper
是否16进制数字(0－9，A-F)字符 isxdigit
字符大小写转换函数 转换为大写字母 toupper
转换为小写字母 tolower
```

### 头文件 local.h

地区化: 本类别的函数用于处理不同国家的语言差异

```txt
地区控制 地区设置 setlocale
数字格式约定查询 国家的货币、日期、时间等的格式转换 localeconv
```

### 头文件 math.h

数学函数: 本分类给出了各种数学计算函数，必须提醒的是ANSIC标准中的数据格式并不符合IEEE754标准，一些C语言编译器却遵循IEEE754(例如frinklin C51)

```txt
反余弦 acos
反正弦 asin
反正切 atan
反正切2 atan2
余弦 cos
正弦 sin
正切 tan
双曲余弦 cosh
双曲正弦 sinh
双曲正切 tanh
指数函数 exp
指数分解函数 frexp
乘积指数函数 fdexp
自然对数 log
以10为底的对数 log10
浮点数分解函数 modf
幂函数 pow
平方根函数 sqrt
求下限接近整数 ceil
绝对值 fabs
求上限接近整数 floor
求余数 fmod
```

### 头文件 setjmp.h io.h

本分类函数用于实现在不同底函数之间直接跳转代码

```txt
保存调用环境 setjmp
恢复调用环境 longjmp
```

### 头文件 signal.h

信号处理: 该分类函数用于处理那些在程序执行过程中发生例外的情况

```txt
指定信号处理函数 signal
发送信号 raise
```

### 头文件 stdarg.h

可变参数处理: 本类函数用于实现诸如printf,scanf等参数数量可变底函数

```txt
可变参数访问宏

可变参数开始宏 va_start
可变参数结束宏 va_end
可变参数访问宏 访问下一个可变参数宏 va_arg
```

### 头文件 stdio.h

输入输出函数:该分类用于处理包括文件、控制台等各种输入输出设备，各种函数以“流”的方式实现

```txt
删除文件 remove
修改文件名称 rename
生成临时文件名称 tmpfile
得到临时文件路径 tmpnam
文件访问 关闭文件 fclose
刷新缓冲区 fflush
打开文件 fopen
将已存在的流指针和新文件连接 freopen
设置磁盘缓冲区 setbuf
设置磁盘缓冲区 setvbuf

格式化输入与输出函数
格式输出 fprintf
格式输入 fscanf
格式输出(控制台) printf
格式输入(控制台) scanf
格式输出到缓冲区 sprintf
从缓冲区中按格式输入 sscanf
格式化输出 vfprintf
格式化输出 vprintf
格式化输出 vsprintf

字符输入输出函数
输入一个字符 fgetc
字符串输入 fgets
字符输出 fputc
字符串输出 fputs
字符输入(控制台) getc
字符输入(控制台) getchar
字符串输入(控制台) gets
字符输出(控制台) putc
字符输出(控制台) putchar
字符串输出(控制台) puts
字符输出到流的头部 ungetc

直接输入输出
直接流读操作 fread
直接流写操作 fwrite

文件定位函数
得到文件位置 fgetpos
文件位置移动 fseek
文件位置设置 fsetpos
得到文件位置 ftell
文件位置复零位 remind

错误处理函数
错误清除 clearerr
文件结尾判断 feof
文件错误检测 ferror
得到错误提示字符串 perror
```

### 头文件 stdlib.h

实用工具函数: 本分类给出了一些函数无法按以上分类，但又是编程所必须要的

```txt
字符串转换函数
字符串转换为整数 atoi
字符串转换为长整数 atol
字符串转换为浮点数 strtod
字符串转换为长整数 strtol
字符串转换为无符号长整型 strtoul

伪随机序列产生函数
产生随机数 rand
设置随机函数的起动数值 srand

存储管理函数
分配存储器 calloc
释放存储器 free
存储器分配 malloc
重新分配存储器 realloc

环境通信
中止程序 abort
退出程序执行，并清除环境变量 atexit
退出程序执行 exit
读取环境参数 getenv
程序挂起，临时执行一个其他程序 system
搜索和排序工具 二分查找(数据必须已排序) bsearch
快速排序 qsort
整数运算函数 求绝对值 abs
得到除法运算底商和余数 div
求长整形底绝对值 labs
求长整形除法的商和余数 ldiv
多字节字符函数 得到多字节字符的字节数 mblen
得到多字节字符的字节数 mbtowc
多字节字符转换 wctomb
多字节字符的字符串操作 将多字节串转换为整数数组 mbstowcs
将多字节串转换为字符数组 mcstowbs
```

### 头文件 string.h

字符串处理: 本分类的函数用于对字符串进行合并、比较等操作

```txt
字符串拷贝 块拷贝(目的和源存储区不可重叠) memcpy
块拷贝(目的和源存储区可重叠) memmove
串拷贝 strcpy
按长度的串拷贝 strncpy
字符串连接函数 串连接 strcat
按长度连接字符串 strncat
串比较函数 块比较 memcmp
字符串比较 strcmp
字符串比较(用于非英文字符) strcoll
按长度对字符串比较 strncmp
字符串转换 strxfrm
字符与字符串查找 字符查找 memchr
字符查找 strchr
字符串查找 strcspn
字符串查找 strpbrk
字符串查找 strspn
字符串查找 strstr
字符串分解 strtok
杂类函数 字符串设置 memset
错误字符串映射 strerror
求字符串长度 strlen
```

### 头文件 time.h

日期和时间函数: 本类别给出时间和日期处理函数

```txt
时间操作函数得到处理器时间 clock
得到时间差 difftime
设置时间 mktime
得到时间 time
时间转换函数 得到以ASCII码表示的时间 asctime
得到字符串表示的时间 ctime
得到指定格式的时间 strftime
```

## 传统C++

```CPP
#include <fstream.h>　　　 //改用<fstream>
#include <iomanip.h>　　　 //改用<iomainip>
#include <iostream.h>　　　//改用<iostream>
#include <strstrea.h>　　　//该类不再支持，改用<sstream>中的stringstream
```

## 标准C++

```CPP
#include <algorithm>　　　 //STL 通用算法
#include <bitset>　　　　　//STL 位集容器
#include <cctype>         //字符处理
#include <cerrno> 　　　　 //定义错误码
#include <cfloat>　　　　 //浮点数处理
#include <ciso646>         //对应各种运算符的宏
#include <climits> 　　　　//定义各种数据类型最值的常量
#include <clocale> 　　　　//定义本地化函数
#include <cmath> 　　　　　//定义数学函数
#include <complex>　　　　 //复数类
#include <csignal>         //信号机制支持
#include <csetjmp>         //异常处理支持
#include <cstdarg>         //不定参数列表支持
#include <cstddef>         //常用常量
#include <cstdio> 　　　　 //定义输入／输出函数
#include <cstdlib> 　　　　//定义杂项函数及内存分配函数
#include <cstring> 　　　　//字符串处理
#include <ctime> 　　　　　//定义关于时间的函数
#include <cwchar> 　　　　 //宽字符处理及输入／输出
#include <cwctype> 　　　　//宽字符分类
#include <deque>　　　　　 //STL 双端队列容器
#include <exception>　　　 //异常处理类
#include <fstream> 　　　 //文件输入／输出
#include <functional>　　　//STL 定义运算函数（代替运算符）
#include <limits> 　　　　 //定义各种数据类型最值常量
#include <list>　　　　　　//STL 线性列表容器
#include <locale>         //本地化特定信息
#include <map>　　　　　　 //STL 映射容器
#include <memory>         //STL通过分配器进行的内存分配
#include <new>            //动态内存分配
#include <numeric>         //STL常用的数字操作
#include <iomanip> 　　　 //参数化输入／输出
#include <ios>　　　　　　 //基本输入／输出支持
#include <iosfwd>　　　　　//输入／输出系统使用的前置声明
#include <iostream> 　　　//数据流输入／输出
#include <istream>　　　　 //基本输入流
#include <iterator>        //STL迭代器
#include <ostream>　　　　 //基本输出流
#include <queue>　　　　　 //STL 队列容器
#include <set>　　　　　　 //STL 集合容器
#include <sstream>　　　　 //基于字符串的流
#include <stack>　　　　　 //STL 堆栈容器
#include <stdexcept>　　　 //标准异常类
#include <streambuf>　　　 //底层输入／输出支持
#include <string>　　　　　//字符串类
#include <typeinfo>        //运行期间类型信息
#include <utility>　　　　 //STL 通用模板类
#include <valarray>        //对包含值的数组的操作
#include <vector>　　　　　//STL 动态数组容器

```

## C99增加的部分

``` CPP
#include <complex.h>　　 //复数处理
#include <fenv.h>　　　　//浮点环境
#include <inttypes.h>　　//整数格式转换
#include <stdbool.h>　　 //布尔环境
#include <stdint.h>　　　//整型环境
#include <tgmath.h>　　　//通用类型数学宏
```

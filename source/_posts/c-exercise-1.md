---
title: c语言编程题1
date: 2021-06-06
tags: code
---
# 1. 单词检查
【问题描述】

已知有一个正确单词索引表（保存在当前目录下的文件index.txt中，且全为小写字母，按照字典序由小到大排列，每个单词独占一行），编写程序利用该单词表对某一英文文章（保存在当前目录下的另一个文件in.txt中）进行单词正确性检查，若该英文文章中出现的单词（只有连续字母组成）没有出现在单词索引文件中（检查时大小写无关），则将该出错的单词（其中的字母全部转换为小写）输出到当前目录下的另一文件error.txt中，每个单词独占一行，并且以字典序由小到大的顺序输出。
假设：
1、in.txt中的文章有可能没有经过排版，格式有可能杂乱无章，也有可能没有写完整。
2、index.txt中的单词个数不超过1000个，每个单词的长度不超过50个字母。
3、若出错的单词多次出现，则多次输出。

【输入形式】

保存单词索引表的文件index.txt和保存英文文章的文件in.txt都位于当前目录下。

【输出形式】

将出错的单词以字典序由小到大的顺序输出到当前目录下的文件error.txt中，每个单词单独占一行，多次出错的单词多次输出。若没有出现错误单词，则什么也不输出。

【样例输入1】

假设文件in.txt内容为：

There are two verrsions of the international standards for C.
Thee first version was ratified in 1989 by the American National
Standards Institue (ANS1) C standard committee.It is often
referred as ANS1 C or C89. The secand C standard was completed
in 1999. This standard is comonly referred to as C99. C99 is a
milestone in C's evolution into a viable programing languga
for numerical and scientific computing.

文件index.txt中的单词索引表内容为：

a
american
and
ansi
are
as
by
c
committee
commonly
completed
computing
evolution
first
for
in
institue
international
into
is
it
language
milestone
national
numerical
of
often
or
programming
ratified
referred
s
scientific
secand
standard
standards
the
there
this
to
two
version
versions
viable
was

【样例输出1】

文件error.txt中出错的单词应为：

ans
ans
comonly
languga
programing
thee
verrsions

【样例1说明】

用index.txt中的单词索引表对in.txt中出现的每一个单词进行检查，检查时大小写无关，所以第一个单词There出现在索引表中，不是错误单词；单词verrsions没有出现在索引表中，拼写错误，所以作为出错单词输出；单词ANSI拼写成了ANS1，将其中字母都转换为小写后输出，并且多次出现，多次输出；其他出错单词类似。错误单词输出按照字典序由小到大输出到error.txt文件中。

【样例输入2】

假设文件in.txt内容为：

There are two versions of the international standard fo

文件index.txt中的单词索引表内容为：

are
for
international
of
standards
the
there
two
versions

【样例输出2】

文件error.txt中出错的单词应为：

fo
standard

【样例2说明】

文件in.txt中的单词standard没有出现在索引表文件index.txt中，所以作为错误单词输出。
注意：样例2中in.txt文件内容还不完整，最后的单词fo后没有任何字符，fo也没有出现在索引表中，所以也作为错误单词输出。

【评分标准】本题要求对文章的单词进行检查，提交程序文件名为words.c或words.cpp。
 # 2. 物品折旧计算器
【问题描述】

某种物品的每年折旧费的线性计算方法如下：每年折旧费=（购买价格-废品价值）/产品设计寿命（年）。而折旧价值的计算方法如下：购买价格-每年折旧费*使用年限。

请编写一个程序，当输入物品的购买价格、废品价值、产品设计寿命和使用年限后，程序能计算出该物品的每年折旧费（结果保留两位小数），以及在到达某使用年限时的折旧价值（即残余价值，结果保留两位小数）。

【输入形式】

在一行内按顺序输入4个数据，分别为购买价格、废品价值、产品设计寿命和使用年限，每两个数据之间用逗号分隔

【输出形式】

在一行内按顺序输出每年折旧费和残余价值，用逗号分隔

【样例输入】

113.56,20.81,30,7

【样例输出】

3.09,91.92

【样例说明】
【评分标准】
 # 3. 比较大小并求和
【问题描述】

输入4个整数，求其前两个数中较小的数与后两个数中较大的数之和。

【输入形式】

输入4个整数，每两个整数之间用逗号分隔

【输出形式】

输出1个整数

【样例输入】

3,2,1,4

【样例输出】

6

【样例说明】

无

【评分标准】

正确性

 # 4. 字母密码
【问题描述】

从键盘任意输入5个小写英文字母，将其加密后输出。加密规则是：用原来英文字母后面的第4个字母代替原来的字母。例如，小写字母a后面第4个字母是e，e代替a。再如，大写字母w后面第4个字母是a，a代替w。请编程实现上述加密方案。

【输入形式】

在一行内连续输入5个小写英文字母原文

【输出形式】

在一行内连续输出5个小写英文字母密文

【样例输入】

china

【样例输出】

glmre

【样例说明】

无

【评分标准】
 # 5. 商品优惠计算器
【问题描述】

使用if语句编程实现输入购货金额，输出实际付款金额。购货折扣率如下：

购货金额≤500元 不打折

500元<购货金额≤1000元 9折

1000元<购货金额 8折

【输入形式】

一个浮点数

【输出形式】

一个浮点数（保留小数点后两位）

【样例输入】

500.01

【样例输出】

450.01

【样例说明】

无
【评分标准】

正确性
 # 6. 简单的四则运算实现
【问题描述】

由键盘输入两个整数，分别计算这两个数的和、差、积、商，并输出结果。

【输入形式】

所输入的两个整数用逗号分隔

【输出形式】

输出4行数据，自上而下每行分别为两个数的和、差、积、商的结果

【样例输入】

3,-5

【样例输出】

a+b=-2

a-b=8

a*b=-15

a/b=0

【样例说明】无
【评分标准】
 # 7. 寻找完数
【问题描述】

完数是指一个整数恰好等于它的因子之和（除自身外），则称这个数为完数。从键盘先后输入两个不大于9999的正整数m和n，若m>n，则交换两数。然后求m~n（m和n均为正整数且m≤n）之间的所有完数。

【输入形式】

先后输入两个正整数m和n，用逗号分隔

【输出形式】

输出所有完数，每两个数之间用逗号分隔。若输入非法，则输出“error”

【样例输入】

1,2000

【样例输出】

6,28,496

【样例说明】

无

【评分标准】

正确性
 # 8. C编程环境
【问题描述】

编写C程序，输出“Hello World”。编辑完成后存盘、编译、连接、运行并查看结果。

【输入形式】
【输出形式】
【样例输入】

无

【样例输出】

Hello World!

【样例说明】

必须输出“Hello World!”

【评分标准】
 # 9. 猴子吃桃问题
【问题描述】

猴子第一天摘下若干个桃子，当即就吃了一半，还不过瘾，又多吃了一个。第二天早上又将剩下的桃子吃掉一半，又多吃一个。以后每天早上都吃了前一天剩下的一半多一个。到第10天早上想再吃时，发现只剩下一个桃子了。求第一天共摘多少个桃子？

【输入形式】

无

【输出形式】

输出一个整数，表示第一天所摘桃子的数量


【评分标准】

正确性

 # 10. 计算两个整数的加法
【问题描述】从键盘输入两个整数，然后求和并输出。
【输入形式】输入两个整数，以空格相隔
【输出形式】两个整数的和值
【样例输入】1 -10
【样例输出】-9
【样例说明】无
【评分标准】正确性
 # 11. 计算乘方和
【问题描述】

从键盘为整型变量a赋值，如果a的值为闭区间[3,10]之间的整数，则计算并输出a4+(a+3)4+(a+6)4+(a+9)4+(a+12)4+(a+15)4的值；否则输出“error”。

【输入形式】

按题意

【输出形式】

按题意

【样例输入】

3

【样例输出】

184275

【样例说明】

无

【评分标准】

正确性
 # 12. 电费计算器
【问题描述】

一个电表按照如下的比率计费：

前200度电：每度0.8元；

后100度电：每度0.9元；

超过300度电：每度1元。

所有用户都是按最少100元进行收费。如果总费用大于400元，还要加收总数的15%的费用。请编写程序，从键盘输入用电量，经过计算后输出显示应收电费。


【输入形式】

一个整数，为用电量

【输出形式】

一个浮点数（保留小数点后两位），为应收电费

【样例输入】

100

【样例输出】

100.00

【样例说明】

无

【评分标准】

正确性

 # 13. 数字转换单词
【问题描述】

编写一个程序，要求用户输入一个两位数，然后输出显示该数的英文单词。提示：把数分解为两个数字。用一个switch语句显示第一位数字对应的单词（“twenty”、“thirty”等），用第二个switch语句显示第二位数字对应的单词。不要忘记11~19需要特殊处理。

【输入形式】

一个十进制两位整数

【输出形式】

输入的整数所对应的英文单词（所含字母均小写）

【样例输入】

85

【样例输出】

eighty-five

【样例说明】

无

【评分标准】

正确性
 # 14. 字符串删除
【问题描述】

编写程序将一行英文中指定的字符串删除后输出。注意：查找指定字符串时，大小写无关，而且有可能多次出现。

【输入形式】

先从标准输入中输入一指定字符串（其长度不超过20，该字符串中不会出现空格），然后在下一行输入一行英文（长度不超过200），行末有回车换行。

【输出形式】

将输入的英文删除指定字符串后输出到标准输出上，末尾应有一个回车换行；若删除后英文为空，则只输出一个回车换行。

【样例1输入】

th
This second edition of "The C Programming Language" describes C as defined by the ANSI standard. Modern compilers already support most features of the standard.

【样例1输出】

is second edition of "e C Programming Language" describes C as defined by e ANSI standard. Modern compilers already support most features of e standard.

【样例2输入】

This
THIS

【样例2输出】

 

【样例说明】

样例1中输入的指定字符串为th，由于是大小写无关查找删除，所以下一行英文信息中有四个子串要删除：Th、Th、th和th，删除后其它信息原样输出。
样例2中输入的指定字符串为This，输入的英文信息为THIS，大小写无关查找删除后英文信息为空，所以只输出了一个回车换行。

【评分标准】该题要求编程实现指定字符串的大小写无关查找删除，提交程序文件名为exam2.c或exam2.cpp。
 # 15. 单词索引编排
【问题描述】

打开一英文文章（保存在一个现有文件in.txt中），为该文件生成词汇表（存到另一个文件out.txt中），要求词汇表中的单词以字典序由小到大存放（只由连续字母组成，且全为小写字母，不重复）。
假设：
1、该文章有可能没有经过排版，格式有可能杂乱无章，也有可能没有写完整。
2、文章中的单词个数不超过1000个，每个单词的长度不超过50个字母。

【输入形式】

保存英文文章的文件in.txt位于当前目录下。

【输出形式】

将生成的词汇表以字典序由小到大输出到当前目录下的文件out.txt中，每个单词单独占一行。

【样例输入1】

假设文件in.txt内容为：

There are two versions of the international standards for C.
The first version was ratified in 1989 by the American National
Standards Institue (ANSI) C standard committee.It is often
referred as ANSI C or C89. The secand C standard was completed
in 1999. This standard is commonly referred to as C99. C99 is a
milestone in C's evolution into a viable programming language
for numerical and scientific computing.

【样例输出1】
文件out.txt中的词汇表应为：

a
american
and
ansi
are
as
by
c
committee
commonly
completed
computing
evolution
first
for
in
institue
international
into
is
it
language
milestone
national
numerical
of
often
or
programming
ratified
referred
s
scientific
secand
standard
standards
the
there
this
to
two
version
versions
viable
was

【样例输入2】

假设文件in.txt内容为：

There are two versions of the international standards for

【样例输出2】
文件out.txt中的词汇表应为：

are
for
international
of
standards
the
there
two
versions

【样例说明】

将in.txt中出现的所有由字母组成的单词（出现的单个字母也作为单词）全部转换成小写后，按照字典序输出到文件out.txt中（每个单词独占一行，重复出现的只输出一次）。
注意：样例2中in.txt文件内容还不完整，单词for后没有任何字符。

【评分标准】本题要求为指定的文件编写单词索引，提交程序文件名为words.c或words.cpp。
 # 
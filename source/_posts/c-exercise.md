---
title: c语言编程题
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
  # 16. 单词索引编排（非文件）
【问题描述】

输入一篇英文文章，为该文章生成词汇表并输出，要求词汇表中的单词以字典序由小到大存放（只由连续字母组成，且全为小写字母，不重复）。
假设：
1、该文章有可能没有经过排版，格式有可能杂乱无章，也有可能没有写完整。
2、文章中的单词个数不超过1000个，每个单词的长度不超过50个字母。

【输入形式】

从标准输入中读取一篇英文文章，该文章可能包含多行。文章输入结束时，在新的一行输入<ctrl>+z打回车表示输入结束。

【输出形式】

将生成的词汇表以字典序由小到大输出到屏幕上，每个单词单独占一行。

【样例输入1】

There are two versions of the international standards for C.
The first version was ratified in 1989 by the American National
Standards Institue (ANSI) C standard committee.It is often
referred as ANSI C or C89. The secand C standard was completed
in 1999. This standard is commonly referred to as C99. C99 is a
milestone in C's evolution into a viable programming language
for numerical and scientific computing.

【样例输出1】

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

There are two versions of the international standards for

【样例输出2】

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

将文章中出现的所有由字母组成的单词（出现的单个字母也作为单词）全部转换成小写后，按照字典序输出到屏幕上（每个单词独占一行，重复出现的只输出一次）。
注意：样例2中文章内容还不完整，单词for后没有任何字符。

【评分标准】本题要求为文章编写单词索引，提交程序文件名为words.c或words.cpp。
 # 17. 判断两数据集是否相同
【问题描述】

从标准输入中读入两个整数集，整数集中数据无序，且可能有重复数据。当两个数据集中数据完全相同（去掉重复数据，顺序不一定相同），则两个数据集相同。编写一程序判断输入的两数据集是否相同：用1表示相同，用0表示不同。

【输入形式】

先输入第一组整数集的个数（大于等于1，小于等于20），然后输入第一组整数（以一个空格分隔）；再输入第二组整数集的个数（大于等于1，小于等于20），并输入第二组整数（以一个空格分隔）。

【输出形式】

若两数据集相同，则输出1，否则输出0，然后在下一行按照从小到大的顺序输出第一个数据集中的数据（去掉重复数据，以一个空格分隔数据）。

【样例输入1】

10
100 56 7 89 -12 100 7 -1298 100 56
12
-12 7 7 56 100 -12 100 56 89 100 56 -1298

【样例输出1】

1
-1298 -12 7 56 89 100

【样例输入2】

10
56 70 -12 100 7 89 -12 100 56 1001
9
100 56 70 89 -12 100 7 12 100

【样例输出2】

0
-12 7 56 70 89 100 1001

【样例说明】

样例1中输入的两个数据集的数据去掉重复数据后完全相同（不考虑顺序），所以输出1，然后按从小到大的顺序输出第一个数据集中的数据。样例2中输入的两个数据集中的数据不相同，第一个数据集中的1001在第二个数据集中不存在，并且第二个数据集中的12在第一个数据集中也没有出现，所以先输出0，然后按从小到大的顺序输出第一个数据集中的数据。

【评分标准】

该题要求判断两数据集是否相同。上传C语言文件名为same.c。

  # 18. 模式字符串查找替换
 

【问题描述】

输入一篇文章，从中查找给定的字符串，并将其替换为指定字符串后输出。要求：

1）从键盘输入给定的待查找字符串，该字符串中只包含大小写字母、数字字符、中括号字符‘[’和‘]’。字符串的长度不超过20。
2）在给定待查找字符串中，中括号最多出现一次（也可以没有），中括号中至少包含一个以上的字母或数字。表示该位置上的字符只要与中括号内的任一字符相同，则匹配成功。
3）查找字符串时大小写无关。
4）查找到给定字符串后，将其替换为指定字符串（其中不含空格，不超过20个字符）输出，其它字符原样输出。

【输入形式】

首先从标准输入（键盘）读入待查找字符串和替换后的字符串，两字符串分行输入。
然后从新的一行开始输入一篇文章。

【输出形式】

将替换后的文章输出到标准输出（屏幕）。

【样例输入1】

zh[Ao]ng
wang
Zhang ying ju zhu zai ZhongGuo.
Ta zheng zai du gao zhong.
Bie ren dou jia ta xiao zhang.

【样例输出1】

wang ying ju zhu zai wangGuo.
Ta zheng zai du gao wang.
Bie ren dou jia ta xiao wang.

【样例1说明】

给定字符串中有中括号，表示第三个字符可以是A也可以是o，且大小写无关，因此文章中第一行的Zhang和Zhong与给定字符串匹配，故将该行中这两个字符串替换成wang后输出。其它类推。

【样例输入2】

a[anb]a
Yes
Do you like banana?
ABA is the abbreviation of American Bankers Association.

【样例输出2】

Do you like bYesna?
Yes is the abbreviation of American Bankers Association.

【样例2说明】

给定字符串中括号内有中括号，表示第一个和第三个字符都为a，第二个字符可以为a、n或b，因此文章中第一行的banana内有一个字符串ana与给定字符串匹配，将其替换为Yes后输出，然后再从ana后的字符n开始查找匹配。

【评分标准】

共有5个测试点。提交程序名为find.c或find.cpp。

  # 19. 折叠方阵
【问题描述】
 
给定一个起始数（大于等于1，小于等于20）和方阵的阶数（大于等于1，小于等于20），编程求得并输出该折叠方阵。一个起始数为10，4阶折叠方阵为：
 
  10  11  14  19
  13  12  15  20
  18  17  16  21
  25  24  23  22
 
【输入形式】
 
从标准输入中输入两个正整数分别表示起始数和方阵的阶数，以一个空格分隔这两个数字。
 
【输出形式】
 
将生成的折叠方阵按行输出到标准输出上，每个数字占4个字符的宽度，靠右对齐，各数字之间不再有空格分隔，每行末尾有回车换行。
 
【样例输入】
 
3 5
 
【样例输出】
 ![](/img/1622555594000.png)
【样例说明】
 
样例输入的起始数为3，方阵的阶数为5，按行输出生成的折叠方阵，每个数字占4个字符的宽度。
 
提示：输出时为了使每个数字占4个字符宽度，c程序可以使用：printf("%4d",......)进行控制输出。
 
【评分标准】该题要求输出折叠方阵，提交程序文件名为exam1.c或exam1.cpp。
 # 20. 模拟浮点数的格式控制输出
【问题描述】

编写程序，读入一无符号浮点数（也可以是整数）和格式控制字符串，按照格式控制要求输出该浮点数。要求：
1、格式控制字符串的形式为：%[-][width][.precision]f，其中必有字符%和f；字符“-”表示输出时左对齐，若没有该字符表示默认右对齐；width和precision为大于等于1的整数，分别表示输出所占字段宽度和精度，若无width或width小于数据的实际宽度时，输出以实际宽度为准；precision若小于实际小数位数，则对小数部分直接截断（不进行四舍五入），若省略，则默认小数点后保留10位，若实际位数不够，则补0。
2、上述格式控制字符串中只有字符“%”、“-”、“.”、“f”和数字字符，不会出现其它字符。
3、width和precision最大为50。
4、输入的浮点数最多不超过100个字符，若有小数点，则小数点前后都有数字。
5、输出时，为了表示左对齐或右对齐，当width大于输出数据的实际宽度时，用英文字符“#”填充空白处。
6、输出格式控制时，小数点本身占一个字符宽度。

【输入形式】

从标准输入分行输入浮点数和格式控制字符串。

【输出形式】

按照格式控制字符串的要求，输出浮点数，注意要用英文字符“#”填充空白处

【样例1输入】

56899038.288095460049505699495
%30.19f

【样例1输出】

##56899038.2880954600495056994

【样例2输入】

0.45467920885612566661763656716236726743
%-20.5f

【样例2输出】

0.45467#############

【样例3输入】

586489909807989969
%5.3f

【样例3输出】

586489909807989969.000

【样例说明】

样例1中输入的浮点数有21位，只截取前19位，输出的浮点数共占28个字符宽度，并且是右对齐，所以前面添加了两个#字符。
样例2要求按照左对齐输出，所以字符#添加到数据后面。
样例3输入数据没有小数部分，输出时末尾添加0输出。

提示：由于数据表示范围的限制，不能直接用C语言中的浮点格式输入输出进行处理。

【评分标准】该题要求编程模拟实现浮点数的格式输出控制，提交程序文件名为print.c或print.cpp。
 # 21. 五子棋危险判断
【问题描述】

已知两人分别执白棋和黑棋在一个围棋棋盘上下五子棋，若同一颜色的棋子在同一条横行、纵行或斜线上连成5个棋子，则执该颜色棋子的人获胜。编写程序读入某一时刻下棋的状态，并判断是否有人即将获胜，即：同一颜色的棋子在同一条横行、纵列或斜线上连成4个棋子，且该4个棋子的两端至少有一端为空位置。
输入的棋盘大小是19×19，用数字0表示空位置（即没有棋子），用数字1表示该位置下了一白色棋子，用数字2表示该位置下了一黑色棋子。假设同一颜色的棋子在同一条横行、纵列或斜线上连成的棋子个数不会超过4个，并且最多有一人连成线的棋子个数为4。

【输入形式】

从控制台输入用来表示棋盘状态的数字0、1或2；每行输入19个数字，各数字之间以一个空格分隔，每行最后一个数字后没有空格；共输入19行表示棋盘状态的数字。

【输出形式】

若有人即将获胜，则先输出即将获胜人的棋子颜色（1表示白色棋子，2表示黑色棋子），然后输出英文冒号:，最后输出连成4个棋子连线的起始位置（棋盘横行自上往下、纵列自左往右从1开始计数，横行最小的棋子在棋盘上的横行数和纵列数作为连线的起始位置，若在同一行上，则纵列数最小的棋子位置作为起始位置，两数字之间以一个英文逗号,作为分隔符）。
若没有人获胜，则输出英文字符串：No。
无论输出什么结果，最后都要有回车换行符。

【输入样例1】

0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 2 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 2 0 1 1 2 0 0 0 0 0 0 0
0 0 0 0 0 2 1 1 1 1 2 2 0 0 0 0 0 0 0
0 0 0 0 0 0 0 1 2 1 2 0 0 0 0 0 0 0 0
0 0 0 0 0 0 1 1 0 2 2 0 0 0 0 0 0 0 0
0 0 0 0 0 2 0 1 0 0 2 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 1 2 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0

【输出样例1】

1:9,8

【输入样例2】

0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 1 2 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 1 2 2 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0

【输出样例2】

No


【样例说明】

在输入的样例1中，执白棋（数字1表示）的人即将获胜，连成4个棋子且有一端为空的起始位置在第9行第8列，所以输出1:9,8。
在输入的样例2中，还没有同一颜色的棋子连成4个，所以无人即将获胜，直接输出No。

【评分标准】

该题要求判断五子棋的棋盘状态，提交程序文件名为chess.c或chess.cpp。
 # 22. Vigenere加密算法
【问题描述】
单一字母替换密码很容易通过字母频率分析而破解。而一种被称为Vigenere的密码克服了这一缺点，其方法是对于待加密信息中不同位置上的字母应用不同的字母加密对应关系。首先选择一个密钥，例如TIGER，然后，对于待加密信息中的第一个字符，采用如下的字母对应关系加密：
ABCDEFGHIJKLMNOPQRSTUVWXYZ
TUVWXYZABCDEFGHIJKLMNOPQRS
上述加密字母表是经过固定移位的字母表，其首字母是T（TIGER的首字母，先是T～Z，然后是A～S）。例如：字母A加密转换成T，字母Q转换成J，不在A～Z之间的字符，不进行转换。
对待加密信息中的第二个字符，采用如下的字母对应关系加密：
ABCDEFGHIJKLMNOPQRSTUVWXYZ
IJKLMNOPQRSTUVWXYZABCDEFGH
对于待加密信息的第3个、第4个、第5个字符，分别采用以G、E、R开头的移位字母表对其加密。因为密钥只有5个字母长，所以对于待加密信息中的第6个字符，将采用与第1个字符相同的对应关系加密，以此类推。
假定待加密信息中的字母全为大写字母，并且输入的密钥也全为大写字母；密钥长度不超过20，待加密信息不超过200个字符。
 
【输入形式】
 
从标准输入中输入密钥串，然后在下一行输入待加密信息（末尾有回车换行）。

【输出形式】
 
加密后结果输出到标准输出（末尾要有回车换行）。

【样例输入】

TIGER
C LANGUAGE IS WONDERFUL.

【样例输出】

V REEZCGKV QY NHVJIIYCR.

【样例说明】
 
按照上面的加密对应表对待加密信息进行加密即可得到加密后的信息，其中只对大写英文字母进行加密对换，例如：第一个字符C在上述第一个转换表中对应的字母为V，第二个字符为空格，应到第二个转换表中查找，因为不存在所以原样输出，依次类推。
 
【评分标准】
 
该题要求对待加密信息进行加密输出。提交程序名为exam2.c或exam2.cpp。
 # 23. 小数分数转换
【问题描述】

从标准输入中输入一个小数，编写程序将其转换成相应的分数显示，即转换为几又几分之几。
要求：
1、输入的小数包括整数部分、小数点和小数部分；整数部分和小数部分分别最多有7位数字；整数部分可以为0，若整数部分为非零整数时，则其最高位不为0；小数部分的末尾数字不为零。
2、输出的分数应为最简分数，由三部分数字组成：第一部分数字代表整数部分（若分数小于1，则为0，否则输出相应分数的整数部分，且最高位不为0），第二部分数字代表分子，第三部分数字代表分母，分子比分母小且不能再约分。

【输入形式】

从标准输入中输入一个小数后打回车。

【输出形式】

将转换后相应分数的三个部分数值输出到标准输出，并且分别以一个空格分隔，最后一个数值后没有空格，有回车换行。

【样例1输入】

0.35

【样例1输出】

0 7 20

【样例2输入】

1050.0144

【样例2输出】

1050 9 625

【样例说明】

样例1中输入的小数为0.35，相应分数整数部分为0，小数部分转换为分数为35/100，约分成最简分数为7/20。
样例2中输入的小数为1050.0144，相应分数整数部分为1050，小数部分转换为分数为144/10000，约分成最简分数为9/625。


【评分标准】该题要求编程实现小数到分数的转换，提交程序文件名为exam1.c或exam2.cpp。
 # 24. 字符串替换
【问题描述】

编写程序将一行英文中指定的字符串替换为另一字符串后输出。注意：查找指定字符串时，大小写无关，而且有可能多次出现。

【输入形式】

先从标准输入中分行输入两个英文字符串（每个字符串不为空，长度不超过20，且字符串中不会出现空格），分别表示被替换的字符串和替换成的字符串，然后在下一行输入一行英文（长度不超过200），行末有回车换行。

【输出形式】

将输入的英文按指定字符串替换后输出到标准输出上，末尾应有一个回车换行。

【样例输入】

th
Hello
This second edition of "The C Programming Language" describes C as defined by the ANSI standard. Modern compilers already support most features of the standard.

【样例输出】

Hellois second edition of "Helloe C Programming Language" describes C as defined by Helloe ANSI standard. Modern compilers already support most features of Helloe standard.

【样例说明】

样例中输入的被替换的字符串为th，由于是大小写无关查找替换，所以下一行英文信息中有四个子串要替换：Th、Th、th和th，分别替换为Hello，其它信息原样输出。

【评分标准】该题要求编程实现指定字符串的大小写无关查找替换，提交程序文件名为exam2.c或exam2.cpp。
  # 25. 偶数之和
【问题描述】

输入8个整数，求其中所有偶数的和。

【输入形式】

输入8个整数，每两个整数之间均以空格分隔

【输出形式】

输出1个整数

【样例输入】

1 -2 2 3 5 8 10 4

【样例输出】

22

【样例说明】

无

【评分标准】

正确性
 # 26. 区间合并
【问题描述】

从标准输入读入n（大于等于2，小于等于100）个闭区间[ai,bi]（ai小于bi，且ai,bi均为int范围内的整数），编写程序将这些区间合并为不相交的闭区间。例如：区间[1,2]、[2,5]、[3,8]、[9,12]可以合并为区间[1,8]和[9,12]。将合并后的闭区间按照升序排列输出。

【输入形式】

先从标准输入读入区间个数n，然后从下一行开始分行读入各个闭区间，每个闭区间包含由一个空格分隔的整数ai和bi。

【输出形式】

按照升序分行输出合并后的闭区间[xi,yi]，xi和yi之间以一个空格分隔。

【样例输入】

7
-5 6
1 3
4 8
10 100
-10 5
-2 6
-50 -30

【样例输出】

-50 -30
-10 8
10 100

【样例说明】

样例中输入了七个闭区间，其中[-5,6]、[1,3]、[4,8]、[-10,5]和[-2,6]可以合并为[-10,8]，合并后的闭区间按照升序输出。

【评分标准】该题要求编程实现区间的合并，提交程序文件名为interval.c或interval.cpp。
 # 27. 倍逆序式数
【问题描述】

对于一个整数n与其逆序数m（将整数倒过来形成的数，如123的逆序数为321），若m恰为n的整数k倍，称n*k=m为倍逆序式数。输入一个整数判断其是否存在倍逆序式。若存在则输出该逆序式；若不存在，则直接输出n和m。

【输入形式】

从标准输入中读取一大于0的十进制整数n，要求：n不会超过int数据类型的表示范围，并且最高位不为0。

【输出形式】

若存在倍逆序式数，则按照下面的格式输出：
n*k=m
其中n为输入的整数，m为其逆序数，k是m为n的倍数，*和=都是英文符号，该输出公式中不得有空格等其它任何字符。若不存在倍逆序式数，则直接输出n和m，中间以一个空格分隔两个数据。
注意：无论是否存在倍逆序式数，输出m时，m的位数应该与n相同，若m的最高位为0，也应该输出0。

【样例1输入】

1089

【样例1输出】

1089*9=9801

【样例2输入】

23200

【样例2输出】

23200 00232

【样例3输入】

1111

【样例3输出】

1111*1=1111

【样例说明】

样例1中输入的n为1089，其逆序数为9801，9801是1089的9倍，所以存在倍逆序式数，输出：1089*9=9801；
样例2中输入的n为23200，其逆序数为00232（实际值为232），逆序数不是原数的倍数，所以不存在倍逆序式数，直接输出：23200 00232；
样例3中输入的n为1111，其逆序数仍为1111，逆序数与原数相同（1倍），所以存在倍逆序式数，输出：1111*1=1111。

【评分标准】该程序要求判断是否存在倍逆序式数，提交程序文件名为exam1.c或exam1.cpp。
 # 28. 整数出现次数统计
【问题描述】

输入一组无序的整数，编写程序按照整数出现次数由多到少输出整数及其出现次数，若出现次数相同，则按照输入顺序输出。

【输入形式】

先从标准输入读入整数的个数（大于等于1，小于等于100），然后在下一行输入这些整数，各整数之间以一个空格分隔。

【输出形式】

在标准输出上按照整数出现次数由多到少输出整数及其出现次数，每行显示一个整数及其出现次数，两者以一个空格分隔，出现次数后跟一个回车；若出现次数相同，则按照输入顺序输出。

【样例输入】

10

0 -50 0 632 5813 -50 9 -50 0 632

【样例输出】

0 3

-50 3

632 2

5813 1

9 1

【样例说明】

输入了10个整数，其中0和-50出现3次，0先输入，所以先输出0及其出现次数，再输出-50及其出现次数；632出现了2次；5813和9只出现1次，5813先出现先输出。

【评分标准】

该程序要求输出整数及其出现次数，提交程序文件名为exam1.c或exam1.cpp。

 # 29. if双分支结构简单应用
【问题描述】

输入一个整数，如果输入的数是偶数或者负数，则输出其平方，否则输出其一半的值。

【输入形式】

整型数据

【输出形式】

整型数据

【样例输入】

7

【样例输出】

3

【样例说明】

无

【评分标准】

正确性
 # 30. 文件加密（环）
【问题描述】

有一种文件加密方法，其方法如下：

1、明码只由小写字母组成，明码长度不超过26个字符；

2、先将明码中的重复字母去掉，即：只保留最先出现的字母，其后出现的相同字母都去掉；

3、将不含重复字母的明码和其它不在明码中的小写字母（按字母升序）连成一个由26个小写字母组成的环，明码在前，明码的头字母为环的起始位置；

4、设原明码的第一个字母（即环的起始位置）作为环的开始位置标识，先从环中删除第一个字母（位置标识则移至下一个字母），再沿着环从下一个字母开始顺时针以第一个字母的ASCII码值移动该位置标识至某个字母，则该字母成为第一个字母的密文字符；然后从环中删除该字母，再从下一个字母开始顺时针以该字母的ASCII码值移动位置标识至某个字母，找到该字母的密文字符；依次按照同样方法找到其它字母的密文字符。当环中只剩一个字母时，则该剩下的最后一个字母的密文为原明码的第一个字母。

例如：如果明码为：helloworld，将明码中重复字母去掉后为：helowrd，将不在明码中的小写字母按照升序添加在明码后，即形成字符串：helowrdabcfgijkmnpqstuvxyz，该字符串形成的环如下图所示：

![](/img/1622556227000.png)

明码的第一个字母为h，h也是环的起始位置。h的ASCII码制为104，先把h从环中删除，再从下一个字母e开始顺时针沿着环按其ASCII值移动位置标识（即移动位置标识104次）至字母w，则h的密文字符为w。w的ASCII码制为119，然后将w从环中删除，再从下一个字母r开始顺时针沿着环移动位置标识119次至字母为l，则w的密文字符为l。依次按照同样方法找到其它字母的密文字符。环中剩下的最后一个字母为x，则x的密文字符为明码的第一个字母h。按照这种方法形成的密文转换字符表为：

![](/img/1622556279000.png)

上方为原文字符，下方为对应的密文字符。

编写程序实现上述文件加密方法。明码和待加密的文件都从标准输入读取，加密后的生成的文件输出到标准输出上。加密时将小写字母按照上述加密方法进行密文转换，其它字符保持不变。

【输入形式】

明码和待加密的文件都从标准输入读取：第一行输入的是明码，然后从第二行开始输入的是待加密的文件。

【输出形式】

加密后的文件内容输出到标准输出。

【样例输入】

helloworld

welcome to 

Bei Hang University!

【样例输出】

ldskmfd vm 

Bdx Hqio Uixjdayxvp!

【样例说明】

输入的明码为helloworld，按照上述的密码转换表将第二行开始的文件内容转换为对应字符输出，其它字符如空格符、回车换行符、大写字母B、H和U等字符原样输出。

【评分标准】

该题要求对指定的文件进行加密，提交的文件名为：encode.c或encode.cpp
 # 31. n的阶乘
【问题描述】

输入一个正整数n（大于等于1，小于100），编程计算并输出n的阶乘。

【输入形式】

从标准输入读入一个正整数n（大于等于1，小于100）。

【输出形式】

在标准输出上输出计算出的n的阶乘。

【样例输入】

30

【样例输出】

265252859812191058636308480000000

【样例说明】

输入正整数n为30，30的阶乘为265252859812191058636308480000000。

【评分标准】该程序要求输出正整数的阶乘，提交程序文件名为exam2.c或exam2.cpp。
 # 32. 最长连续升序整数序列
【问题描述】

输入一组无序的整数（整数都大于等于0），编程求出其中最长的连续升序子序列（该序列中后一个整数比前一个整数多1，序列的长度是指序列中整数的个数，长度应大于等于2）。例如输入13个整数：3520 0 3 89 56 88 3521 9 90 1 99 2 87，其中连续升序子序列有3个：3520 3521，0 1 2 3和87 88 89 90，长度分别为2、4、4，所以后两个子序列都是最长的连续升序子序列。

【输入形式】

先从标准输入读入整数的个数（大于等于1，小于等于100），然后在下一行输入这些整数，各整数之间以一个空格分隔。

【输出形式】

先向标准输出输出最长连续升序子序列的长度，然后从下一行开始按升序分行输出最长连续升序子序列，各整数之间以一个空格分隔，每行最后一个整数后也要有一个空格。

若没有连续升序子序列，直接输出数字0。

【样例输入】

13

3520 0 3 89 56 88 3521 9 90 1 99 2 87

【样例输出】

4

0 1 2 3 

87 88 89 90 

【样例说明】

输入的整数个数为13，其中最长连续升序子序列的长度为4，有两个最长连续升序子序列，分别按升序分行输出。

【评分标准】该程序要求输出最长连续升序子序列，提交程序文件名为exam1.c或exam1.cpp。
 # 33. 枚举量值
【问题描述】

按照C语言语法，每个枚举量都有一个值，如果没有指定，则按隐含规则生成。从标准输入中读入一合法的枚举类型定义语句，识别计算并输出其中定义的每个枚举量的值。要求：
1、枚举类型定义语句中每个枚举量的名字长度不超过32；枚举量的个数不超过50个；
2、枚举类型定义语句中指定的数值是大于等于0的十进制整数。

【输入形式】

从标准输入读入一行符合C语言语法的枚举类型定义语句，末尾有回车换行。

【输出形式】

按照定义的先后顺序分行输出每个枚举量的名字和其值，两者之间以一个空格分隔。

【样例1输入】

enum BOOL{FALSE,TRUE};

【样例1输出】

FALSE 0
TRUE 1

【样例2输入】

enum { JAN=1  , FEB,   MAR    , APR ,MAY, JUN, JUL, AUG , SEP, OCT , NOV , DEC,MON=1,TUES,WED, THUR , FRI,SET,SUN,   FOUNDING   =   1949      };

【样例2输出】

JAN 1
FEB 2
MAR 3
APR 4
MAY 5
JUN 6
JUL 7
AUG 8
SEP 9
OCT 10
NOV 11
DEC 12
MON 1
TUES 2
WED 3
THUR 4
FRI 5
SET 6
SUN 7
FOUNDING 1949

【样例说明】

样例1中定义的枚举量有两个，分别为FALSE和TRUE，都没有指定值，所以采用默认值，分别为0和1；
样例2中定义的枚举量有20个，其中JAN指定值为1，其后的11个枚举量没有指定值，所以它们的值依次增1；MON指定值为1，其后的6个枚举量的值也依次增1；最后一个枚举量的值指定为1949。

【评分标准】该程序要求识别并输出定义的枚举量的值，提交程序文件名为exam2.c或exam2.cpp。
 # 34. 计算器（表达式计算-表达式树实现）
【问题描述】

从标准输入中读入一个整数算术运算表达式，如24 / ( 1 + 2 + 36 / 6 / 2 - 2) * ( 12 / 2 / 2 )= ，计算表达式结果，并输出。

要求：
1、表达式运算符只有+、-、*、/，表达式末尾的=字符表示表达式输入结束，表达式中可能会出现空格；
2、表达式中会出现圆括号，括号可能嵌套，不会出现错误的表达式；
3、出现除号/时，以整数相除进行运算，结果仍为整数，例如：5/3结果应为1。

4、要求采用表达式树来实现表达式计算。

表达式树（expression tree）：

我们已经知道了在计算机中用后缀表达式和栈来计算中缀表达式的值。在计算机中还有一种方式是利用表达式树来计算表达式的值。表达式树是这样一种树，其根节点为操作符，非根节点为操作数，对其进行中序遍历将计算表达式的值。由后缀表达式生成表达式树的方法如下：

l  读入一个符号：

l  如果是操作数，则建立一个单节点树并将指向他的指针推入栈中；

l  如果是运算符，就从栈中弹出指向两棵树T1和T2的指针（T1先弹出）并形成一棵新树，树根为该运算符，它的左、右子树分别指向T2和T1，然后将新树的指针压入栈中。

例如输入的后缀表达式为：


    ab+cde+**

则生成的表达式树为：

![](/img/1622556643000.png)

【输入形式】

从键盘输入一个以=结尾的整数算术运算表达式。操作符和操作数之间可以有空格分隔。


【输出形式】

首先在屏幕上输出表达式树根、左子节点及右子节点上的运算符或操作数，中间由一个空格分隔，最后有一个回车（如果无某节点，则该项不输出）。然后输出表达式计算结果。
【样例输入】

24 / ( 1 + 2 + 36 / 6 / 2 - 2) * ( 12 / 2 / 2 )     =

【样例输出】

* / /

18


【样例说明】

按照运算符及括号优先级依次计算表达式的值。在生成的表达树中，*是根节点的运算符，/ 是根节点的左子节点上运算符，/是根节点的右子节点上运算符，按题目要求要输出。


【评分标准】

该题要求按照表达式树计算表达式的值，提交文件名为exam2.c或exam2.cpp。
 # 35. 寻找回文数
【问题描述】

所谓回文数就是将一个数从左向右读与从右向左读是一样的，例如，121和1331都是回文数。编写一个函数实现求正整数n以内的回文数。

【源文件名】

ex403.c

【输入形式】

输入一个正整数，为n的值

【输出形式】

每行输出10个回文数，每两个回文数之间用逗号分隔

【样例输入】

150

【样例输出】

0,1,2,3,4,5,6,7,8,9,

11,22,33,44,55,66,77,88,99,101,

111,121,131,141,

【样例说明】

无

【评分标准】
 # 36. 寻找双质数
【问题描述】

所谓“双质数”是指对于两个质数p和q，如果满足p = q + 2，则p和q为双质数。请编程实现利用函数求解闭区间[m, n]之间的双质数，其中m和n均为正整数且m < n。

【源文件名】

ex402.c

【输入形式】

从键盘先后输入两个正整数（分别为m和n），用逗号分隔

【输出形式】

每行输出一对双质数，用逗号分隔。若有多对双质数，则分多行输出

【样例输入】

3,100

【样例输出】

3,5

5,7

11,13

17,19

29,31

41,43

59,61

71,73

【样例说明】

无

【评分标准】
 # 37. 数列前n项和
【问题描述】
写一个函数，求解以下数列前n项之和并输出，其中n（正整数）应从键盘输入。
![](/img/1622556752000.png)

【源文件名】

ex401.c

【输入形式】

输入一个正整数（int型），表示数列的项数

【输出形式】

输出一个实数（float型），保留小数点后两位

【样例输入】

3

【样例输出】

5.17

【样例说明】

无

【评分标准】
 # 38. 水仙花数
【问题描述】

打印出所有“水仙花数”，所谓“水仙花数”是指一个三位数，其各位数字立方和等于该数本身。例如：153是一个水仙花数，因为153=13+53+33。

【输入形式】

无

【输出形式】

每行输出一个水仙花数，有多少个水仙花数，就输出多少行


【评分标准】

正确性

 # 39. 闰年问题
【问题描述】

定义一个带参数的宏，以判别某个年份是否为闰年。其中年份year应从键盘输入。

【源文件名】

ex406.c

【输入形式】

输入一个整数，为年份

【输出形式】

输出所输入的年份是或不是闰年，请参见样例输出

【样例输入】

1990

【样例输出】

1990 is not a leap year

【样例说明】

无



【样例输入】


2000

【样例输出】


2000 is a leap year

【样例说明】

无

【评分标准】

 # 40. 求解勒让德多项式
【问题描述】

使用递归方法求n阶勒让德多项式的值，递归公式为：


![](/img/1622556860000.png)
其中：n和x为int型；Pn(x)为float型。


【源文件名】

ex405.c

【输入形式】

先后从键盘输入n和x，用逗号分隔

【输出形式】

若n小于0，则输出“error”。若n大于等于0，则输出Pn(x)，保留小数点后两位

【样例输入】

-1,3

【样例输出】

error

【样例说明】

无



【样例输入】

2,-3

【样例输出】

-3.50

【样例说明】

无
 # 41. 储蓄账户余额计算器
【问题描述】

假设你每月在储蓄账户上存100元，年利率是5%，则每月的利率是0.05/12=0.00417。

第一个月后，账户上的值变成100×(1+0.00417)=100.417；

第二个月后，账户上的值变成(100+100.417)×(1+0.00417)=201.252；

第三个月后，账户上的值变成(100+201.252)×(1+0.00417)=302.507；

以此类推。

写一个函数，根据用户输入的每月存款数、年利率和月份数，计算给定月份后账户上的钱数并输出。


【源文件名】

ex404.c

【输入形式】

输入每月存款数、年利率、月份数，每两个数据之间用逗号分隔

【输出形式】

月末账户本息余额（保留小数点后两位）

【样例输入】

100,0.05,3

【样例输出】

302.51

【样例说明】

无

【评分标准】

 # 42. 消除游戏
【问题描述】

消除类游戏是深受大众欢迎的一种游戏，游戏在一个包含有n行m列的游戏棋盘上进行，棋盘的每一行每一列的方格上放着一个有颜色的棋子，当一行或一列上有连续三个或更多的相同颜色的棋子时，这些棋子都被消除。当有多处可以被消除时，这些地方的棋子将同时被消除。

现在给定一个n行m列的棋盘，棋盘中的每一个方格上有一个棋子（用数字1-9表示各种颜色的棋子），请给出经过消除后的棋盘。

请注意：一个棋子可能在某一行和某一列同时被消除。

【输入形式】

从标准输入读取数据，第一行包含两个整数n和m，分别表示棋盘的行数和列数（行数和列数都大于等于3，小于等于9），以一个空格分隔这两个整数。

接下来输入n行，每行m个整数，用一个空格分隔各个整数，这些整数分别表示每一个方格中棋子的颜色（大于等于1，小于等于9）。

【输出形式】

向标准输出上输出n行，每行m个整数，相邻整数之间以一个空格分隔，表示经过消除后的棋盘。如果一个方格中的棋子被消除，则对应的方格输出数字0，否则输出代表原棋子颜色的整数。每行最后一个整数后也要有一个空格。

【样例1输入】

4 5

2 2 3 1 2

3 4 5 1 4

2 3 2 1 3

2 2 2 4 4

【样例1输出】

2 2 3 0 2 

3 4 5 0 4 

2 3 2 0 3 

0 0 0 4 4 

【样例1说明】

棋盘中第4列的1和第4行的2可以被消除，其它方格中的棋子均被保留。

【样例2输入】

4 5

2 2 3 1 2

3 1 1 1 1

2 3 2 1 3

2 2 3 3 3

【样例2输出】

2 2 3 0 2 

3 0 0 0 0 

2 3 2 0 3 

2 2 0 0 0 

【样例2说明】

棋盘中第4列的1，第二行的1和第4行的3可以被消除，其它方格中的棋子均被保留。

【评分标准】该程序要求输出消除后的棋盘状态，提交程序文件名为exam1.c或exam1.cpp。
 # 43. 整数出现次数
【问题描述】

输入一组无序的整数，编程输出其中出现次数最多的整数及其出现次数。

【输入形式】

先从标准输入读入整数的个数（大于等于1，小于等于100），然后在下一行输入这些整数，各整数之间以一个空格分隔。

【输出形式】

在标准输出上输出出现次数最多的整数及其出现次数，两者以一个空格分隔；若出现次数最多的整数有多个，则按照整数升序分行输出。

【样例输入】

10

0 -50 0 632 5813 -50 9 -50 0 632

【样例输出】

-50 3

0 3

【样例说明】

输入了10个整数，其中出现次数最多的是-50和0，都是出现3次。

【评分标准】该程序要求输出出现次数最多的整数和出现次数，提交程序文件名为exam1.c或exam1.cpp。
 # 44. Huffman文件解码
【问题描述】

给定一组字符的Huffman编码表（从标准输入读取），以及一个用该编码表进行编码的Huffman编码文件（从标准输入读取），编写程序实现对Huffman编码文件的解码，并按照前序遍历序列输出解码过程中Huffman树（规定树中左分支表示0，右分支表示1）中各结点的访问次数。

例如给定的一组字符的Huffman编码表为：

6

1:111

2:0

+:110

*:1010

=:1011

8:100

第一行的6表示要对6个不同的字符进行编码，后面每行中冒号（:）左边的字符为待编码的字符，右边为其Huffman编码，冒号两边无空格。对于该编码表，对应的Huffman树（树中左分支表示0，右分支表示1）应为：

![](/img/1622557028000.jpg)

假如Huffman编码文件的内容（由0和1字符组成的序列）为：

111011001010011001011111100

则遍历上述Huffman树即可对该文件进行解码，解码后的文件内容为：

12+2*2+2=18

解码过程中，经过Huffman树中各结点的遍历次数见下图中结点中的数字：

![](/img/1622557052000.jpg)

对该Huffman树中各结点的访问次数按照前序遍历序列输出应为：

11 4 7 3 1 2 1 1 4 2 2 

【输入形式】

先从标准输入读入待编码的字符个数（大于等于2，小于等于50），然后分行输入各字符的Huffman编码（先输入字符，再输入其编码，字符和编码中间以一个英文字符冒号:分隔），编码只由0和1组成。

Huffman编码文件在最后一行输入，其中只有0和1字符，末尾有一个回车换行符。

【输出形式】

先将解码后的文件内容输出到标准输出上（独占一行）；然后以前序遍历序列输出解码过程中Huffman树中各结点的访问次数，各数据间以一个空格分隔，最后一个数据后也有一个空格。

【样例输入】

6

1:111

2:0

+:110

*:1010

=:1011

8:100

111011001010011001011111100

【样例输出】

12+2*2+2=18

11 4 7 3 1 2 1 1 4 2 2 

【样例说明】

从标准输入读取了6个字符的Huffman编码，因为规定Huffman树中左分支表示0，右分支表示1，所以利用该编码表可构造上述Huffman树（见图1）。遍历该Huffman树对最后一行输入的编码文件进行解码，即可得到解码后的原文件内容，遍历过程中各树中结点的最终访问次数要按照前序遍历序列输出。

【评分标准】

该题要求根据字符的Huffman编码表对编码文件进行解码，提交的文件名为：exam2.c或exam2.cpp。
 # 45. 计算器（表达式计算）
【问题描述】

从标准输入中读入一个整数算术运算表达式，如24 / ( 1 + 2 + 36 / 6 / 2 - 2) * ( 12 / 2 / 2 )= ，计算表达式结果，并输出。

要求：

1、表达式运算符只有+、-、*、/，表达式末尾的=字符表示表达式输入结束，表达式中可能会出现空格；表达式中出现的字符都是英文字符；
2、表达式中会出现圆括号，括号可能嵌套，不会出现错误的表达式；

3、出现除号/时，以整数相除进行运算，结果仍为整数，例如：5/3结果应为1。

【输入形式】

从键盘输入一个以=结尾的整数算术运算表达式。操作符和操作数之间可以有空格分隔。

【输出形式】

在屏幕上输出计算结果（为整数，即在计算过程中除法为整除）。

【样例输入】

24 / ( 1 + 2 + 36 / 6 / 2 - 2) * ( 12 / 2 / 2 )     =


【样例输出】

18
【样例说明】

按照运算符及括号优先级依次计算表达式的值。

【评分标准】

该题要求计算表达式的值，提交程序名为exam2.c或exam2.cpp。
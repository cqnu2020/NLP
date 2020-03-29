# python  
&emsp;&emsp;下载地址：https://www.python.org/downloads/  
&emsp;&emsp;运行Python程序有两种方式：交互式和文件式。交互式指Python解释器即时响应用户输入的每条代码，给出输出结果。文件式，也称为批量式，指用户将Python程序写在一个或多个文件中，然后启动Python解释器批量执行文件中的代码。下面以Windows操作系统中运行Hello程序为例具体说明两种方式的启动和执行方法。  
1.  交互式启动和运行方法  
&emsp;&emsp;交互式有两种启动和运行方法。  
&emsp;&emsp;第一种方法，启动Windows操作系统命令行工具( <Windows系统安装目录>\system32\cmd.exe)，在控制台中输入“Python”，在命令提示符>>>后输入如下程序代码：  
&emsp;&emsp;print("Hello World")  
&emsp;&emsp;按Enter键后显示输出结果"Hello World”。  
![1](https://github.com/cqnu2020/NLP/blob/hemiaohui/beginner/python/pictures/1.png?raw=true)  
&emsp;&emsp;在>>>提示符后输入exit()或者quit()可 以退出Python 运行环境。  
&emsp;&emsp;第二种方法，通过调用安装的IDLE来启动Python 运行环境。IDLE是Python软件包自带的集成开发环境，可以在Windows“开始”菜单中搜索关键词“IDLE"找到IDLE的快捷方式。如图展示了IDLE环境中运行Hello World程序的效果。  
![2](https://github.com/cqnu2020/NLP/blob/hemiaohui/beginner/python/pictures/2.png?raw=true)  
2. 文件式启动和运行方法  
&emsp;&emsp;文件式也有两种运行方法，与交互式相对应。  
&emsp;&emsp;第一种方法， 按照Pyhon的语法格式编写代码，并保存为.py 形式的文件(以Hello World程序为例，将代码保存成文件hello.py)。Python 代码可以在任意编辑器中编写，对于百行以内规模的代码建议使用Python安装包中的IDLE编辑器。然后，打开Windows的命令行(cmd.exe)，进入hello.py,文件所在目录，运行Pyhon程序文件获得输出，如图：  
![3](https://github.com/cqnu2020/NLP/blob/hemiaohui/beginner/python/pictures/3.png?raw=true)  
&emsp;&emsp;第二种方法，打开IDLE，按快捷键Ctrl+N打开一个新窗口，或在菜单中选择File→New File选项。这个新窗口不是交互模式，它是一个具备Python 语法高亮辅助的编辑器，可以进行代码编辑。在其中输入Python代码，例如，输入Hello World程序并保存为hello.py文件，如图所示。按快捷键F5,或在菜单中选择Run→Run Module选项运行该文件。    
![4](https://github.com/cqnu2020/NLP/blob/hemiaohui/beginner/python/pictures/4.png?raw=true)  
3. 启动和运行方法推荐  
&emsp;&emsp;交互式和文件式共有4种Python程序运行方法，其中，最常用且最重要的是采用IDLE的文件式方法。IDLE是一个简单有效的集成开发环境，无论交互式或文件式，它都有助于快23速编写和调试代码，它是小规模Python 软件项目的主要编写工具。  
## 基本数据类型  
### 数字类型  
#### 整数类型   
&emsp;&emsp;整数类型共有4种进制表示：十进制、二进制、八进制和十六进制。默认情况整数采用十进制，其他进制需要增加引导符号。   
| 进制种类 | 引导符号 | 描述                                  |
| :------: | -------- | ------------------------------------- |
|  十进制  | 无       | 默认情况，例如1010                    |
|  二进制  | 0b或0B   | 由字符0和1组成，例如0b101,0B101       |
|  八进制  | 0o或0O   | 由字符0到7组成，例如0o711,0O711       |
| 十六进制 | 0x或0X   | 由字符0到9、a到f、A到F组成，例如0xABC |
#### 浮点数类型     
&emsp;&emsp;Python语言要求所有浮点数必须带有小数部分，小数部分可以是0，这种设计可以区分浮点数和整数类型。浮点数有两种表示方法：十进制表示和科学技术法表示。  
&emsp;&emsp;浮点数类型例子：0.0，-2.7，4.3e-3，9.6E5  
&emsp;&emsp;科学计数法使用字母e或E作为幂的符号，以十为基数，含义如下：  
&emsp;&emsp;\<a>e\<b> = a\*10<sub>b<sub>    
&emsp;&emsp;上例中4.3e-3值为0.0043.  
#### 复数类型   
&emsp;&emsp;Python语言中，复数的虚数部分通过后缀“J”或“j”来表示，例如：12.3+4j，-5.6-7j，1.23e-4+5.67e+89j   
&emsp;&emsp;复数类型中实数部分和虚数部分的数值都是浮点类型。对于复数z，可以用z.real和z.imag分别获得它的实属部分和叙述部分，例如：   
```python
>>>(1.23e-4+5.67e+89j).real
0.000123
>>>(1.23e-4+5.67e+89j).imag
5.67e+89
```
### 数字类型的操作   
#### 内置的数值运算操作符    
| 操作符 | 描述                                     |
| ------ | ---------------------------------------- |
| x+y    | x与y之和                                 |
| x-y    | x与y之差                                 |
| x*y    | x与y之积                                 |
| x/y    | x与y之商                                 |
| x//y   | x与y之整数商，即不大于x与y之商的最大整数 |
| x%y    | x与y之商的余数，也成为模运算             |
| -x     | x的负值，即x*(-1)                        |
| +x     | x本身                                    |
| x\*\*y   | x的y次幂，即x<sup>y<sup>                 |

&emsp;&emsp;操作符运算的结果可能改变数字类型，3种数字类型之间存在一种捉逐渐展的关系，具体如下   
&emsp;&emsp;整数->浮点数->复数    
&emsp;&emsp;基于上述扩展关系，数字类型之间相互运算所生成的结果是“更宽“的类型。   
```python
>>>100/3
33.333333333333336
>>>100//3
33
>>>123+4.0
127.0
>>>10.0-1+2j #等价于(10.0-1)+2j
(9+2j)
```
&emsp;&emsp;表中所有二元操作符（+、-、\*、/、//、%、\*\*）都有与之对应的增强赋值操作符（+=、-=、\*=、/=、//=、%=、\*\*=）.    
```python
>>>x=3
>>>x**=2   #等价于x=x**2
>>>x
6
```
#### 内置的数值运算函数   
| 函数                                            | 描述                                                         |
| ----------------------------------------------- | ------------------------------------------------------------ |
| abs(x)                                          | x的绝对值                                                    |
| divmod(x,y)                                     | (x//y,x%y)，输出为二元组形式（也成为元组类型）               |
| pow(x,y[,z])                                    | (x\*\*y)%z，[..]表示该参数可以省略，即pow(x,y)，它与x\*\*y相同 |
| round(x[,ndigits])                              | 对x四舍五入，保留ndigits小数。round(x)返回四舍五入的整数值   |
| max(x<sub>1<sub>,x<sub>2<sub>,...,x<sub>n<sub>) | x<sub>1<sub>,x<sub>2<sub>,...,x<sub>n<sub>的最大值，n没有限定 |
| min(x<sub>1<sub>,x<sub>2<sub>,...,x<sub>n<sub>) | x<sub>1<sub>,x<sub>2<sub>,...,x<sub>n<sub>的最小值，n没有限定 |
```python
>>>abs(-3+4j)
5.0
>>>pow(3,pow(3,999),1000)    #幂运算和模运算同时进行，速度快
587
```
#### 内置的数字类型转换函数   
| 函数             | 描述                                                         |
| ---------------- | ------------------------------------------------------------ |
| int(x)           | 将x转化为整数，x可以是浮点数或字符串                         |
| float(x)         | 返回浮点数x或者字符串x所对应的整数类型                       |
| complex(re[,im]) | 生成一个复数，实部为re，虚部为im，re可以是整数、浮点数或字符串，im可以是整数或浮点数但不能是字符串 |
```python
>>>int(10.99)
10
>>>complex(10.99)
(10.99+0j)
>>>float(10+99j)   #解释器会报TypeError错误，并给出该错误的基本描述
Traceback (most recent call last):
  File "<pyshell#0>", line 1, in <module>
    float(10+99j)
TypeError: can't convert complex to float
>>>float((10+99j).imag)
99.0
```
### 字符串类型及其操作  
#### 字符串类型的表示  
&emsp;&emsp;字符串是字符的序列表示，可以由一对单引号(')、双引号(") 或三引号(")构成。3种表示方式如下:  
&emsp;&emsp;单引号字符串:  '单引号表示，可以使用"双引号"作为字符串的一部分'  
&emsp;&emsp;双引号字符串: "双引号表示，可以使用'单引号作为字符串的一部分"  
&emsp;&emsp;三引号字符串:   
&emsp;&emsp;’‘’三引号表示可以使用"双引号"  
&emsp;&emsp;'单引号'  
&emsp;&emsp;也可以换行‘’‘  
&emsp;&emsp;打印字符串的Python程序运行结果如下，注意其中的引号部分：  
```python
>>>print('单引号表示可以使用"双引号"作为字符串的一部分')
单引号表示可以使用"双引号"作为字符串的一部分
>>>print("双引号表示可以使用'单引号'作为字符串的一部分")
双引号表示可以使用'单引号'作为字符串的一部分
>>>print( '''三引号表示可以使用"双引号"
'单引号'
也可以使用换行''')
三引号表示可以使用"双引号"
'单引号'
也可以使用换行
```
&emsp;&emsp;input()函数将用户输入的内容当做一个字符串类型，这是获得用户输入的常用方式。print()函数可以直接打印字符串，这是输出字符串的常用方式。   
```python
>>>name=input("请输入名字:")
请输入名字:Python语言
>>>print(name)
Python语言
```
&emsp;&emsp;字符串包括两种序号体系:正向递增序号和反向递减序号。正向递增需要以最左侧字符序号为0，向右依次递增；反向递减序号以最右侧字符序号为-1，向左依次递减，这两种索引字符的方法可以在-一个表示中使用。  
&emsp;&emsp;Python字符串也提供区间访问方式，采用[N: M]格式，表示字符串中从N到M(不包含 M)的子字符串， 其中，N和M为字符串 的索引序号。如果表示中M或者N索引缺失，则表示字符串把开始或结束索引值设为默认值。  
&emsp;&emsp;字符串以Unicode编码存储，因此，字符串的英文字符和中文字符都算作1个字符。观察下面实例  
```
>>>name="Python语言程序设计"
>>>name[0]
'P'
>>>print(name[7],name[-1])
言 计
>>>print(name[:6])
Python
>>>print([6:])
语言程序设计
>>>print([:])
Python语言程序设计
```
&emsp;&emsp;反斜杠字符（\）是一个特殊字符，在字符串中表示转转义，即该字符与后面相邻的一个字符共同组成了新的含义。例如，\n表示换行、\\\\表示反斜杠、\‘表示单引号、\“表示双引号、\t表示制表符（Tab）等。     
```python
>>>print("Python\n语言\t程序\t设计")
Python
语言	程序	设计 
```
#### 基本的字符串操作符  
| 操作符     | 描述                                      |
| ---------- | ----------------------------------------- |
| x+y        | 连接两个字符串x与y                        |
| x\*n或n\*x | 复制n次字符串x                            |
| x in s     | 如果x是s的字串，返回True，否则返回F       |
| str[i]     | 索引，返回第i个字符                       |
| str[N:M]   | 切片，返回索引第N到第M的字串，其中不包含M |
```python
>>>"python 语言"+"程序设计"
'python 语言程序设计'
>>>name="python 语言"+"程序设计"+"基础"
>>>name
"python 语言程序设计基础"
>>>'GOAL!'*3
'GOAL!GOAL!GOAL!'
>>>"python 语言" in name
True
>>>'Y' in "python 语言"
False
```
#### 内置的字符串处理函数    
| 函数   | 描述                                                |
| ------ | --------------------------------------------------- |
| len(x) | 返回字符串x的长度，也可返回其他组合数据类型元素个数 |
| str(x) | 返回任意类型x所对应的字符串形式                     |
| chr(x) | 返回Unicode编码x对应的单字符                        |
| ord(x) | 返回单字符表示的Unicode编码                         |
| hex(x) | 返回整数x对应十六进制数的小写形式字符串             |
| oct(x) | 返回整数x对应八进制数的小写形式字符串               |
```python
>>>len("python")
6
>>>str(3.1415)
'3.1415'
```
&emsp;&emsp;每个字符在计算机中可以表示为一个数字，称为编码。字符串则以编码序列方式存储在计算机中。目前，计算机系统使用的一个重要编码是ASCII编码，该编码用数字0\~127表示计算机键盘上的常见字符以及一些被称为控制代码的特殊值。例如，大写字母A\~Z用65\~90表示，小写字母a\~z用97\~122表示。  
&emsp;&emsp;ASCII编码针对英语字符设计，它没有覆盖其他语言存在的更广泛字符，因此，现代计算机系统正逐步支持-个更大的编码标准Unicode,它支持 几乎所有书写语言的字符。Python字符串中每个字符都使用Unicode编码表示。  
&emsp;&emsp;chr(x)和ord(x)函数用于在单字符和Unicode 编码值之间进行转换。chr(x)函数返回Unicode编码对应的字符，其中，Unicode 编码x的取值范围是0到1 114 111(即十六进制数0x10FFFF)。ord(x)函数返回单字符x对应的Unicode编码。例如：  
```python
>>>"1+1-2"+chr(10004)
'1+1-2✔'
>>>"金牛座字符♉的Unicode值是："+str(ord("♉"))
'金牛座字符♉的Unicode值是：9801'
>>>hex(255)
'0xff'
>>>oct(-255)
'-0o377'
```
#### 内置的字符串处理方法  
| 方法                                 | 描述                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| str.lower()                          | 返回字符串str的副本，全部字符小写                            |
| str.upper()                          | 返回字符串str的副本，全部字符大写                            |
| str.islower()                        | 当str所有字符都是小写时，返回True，否则返回False             |
| str.isprintable()                    | 当str所有字符都是可打印的，返回True，否则返回False           |
| str.isnumeric()                      | 当str所有字符都是数字时，返回True，否则返回False             |
| str.isspace()                        | 当str所有字符都是空格时，返回True，否则返回False             |
| str.endswith(suffix[,start[,end]])   | str[start:end]以suffix结尾返回True，否则返回False            |
| str.startswith(prefix[,start[,end]]) | str[start:end]以prefix开始返回True，否则返回False            |
| sre.split(sep=None,maxsplit=-1)      | 返回一个列表，由str根据sep被分隔的部分构成                   |
| str.count(sub[,start[,end]])         | 返回str[start:end]中sub字串出现的次数                        |
| str.replace(old,new[,count])         | 返回字符串str的副本，所有old字串被替换为new，如果count给出，则前count次old出现被替换 |
| str.center(width[,fillchar])         | 字符串居中函数，详见函数定义                                 |
| str.strip([chars])                   | 返回字符串str的副本，在其左侧和右侧去掉chars中列出的字符     |
| str.zfill(width)                     | 返回字符串str的副本，长度为width，不足部分在左侧添0          |
| str.format()                         | 返回字符串str的一种排版格式                                  |
| str.join(iterable)                   | 返回一个新字符串，由组合数据类型iterable变量的每个元素组成，元素间用str分隔 |
```python
>>>"Python is an excellent language.".split()   '''返回一个列表，分隔str的标识符是sep，默认分隔符                                                    为空格，maxsplit参数为最大参数'''

['Python', 'is', 'an', 'excellent', 'language.']
>>>"python".center(40,'=')
'=================python================='
>>>"123".zfill(40)
'0000000000000000000000000000000000000123'
>>>"-123".zfill(40)
'-000000000000000000000000000000000000123'
```
### 字符串类型的格式化  
#### format（）方法的基本使用  
&emsp;&emsp;字符串format(方法的基本使用格式如下:      
&emsp;&emsp;<模板字符串>. format (<逗号分隔的参数>)     
&emsp;&emsp;模板字符串由一系 列槽组成，用来控制修改字符串中嵌入值出现的位置，其基本思想是将format(方法中逗号分隔的参数按照序号关系替换到模板字符串的槽中。槽用大括号({}) 表示，如果大括号中没有序号，则按照出现顺序替换，如图所示。    
&emsp;&emsp;printf()函数是C语言中向控制台输出信息的主要函数，类似Python语言中的print()函数。如果大括号中指定了使用参数的序号，按照序号对应参数替换，如图所示，参数从0开始编号。调用format(方法后会返回一个新的字符串。例如：   

```
>>>"{}:计算机{}的cpu占用率为{}%。".format("2016-12-31","PYTHON",10)
'2016-12-31:计算机PYTHON的cpu占用率为10%。'
```
<img src="https://github.com/cqnu2020/NLP/blob/hemiaohui/beginner/python/pictures/5.jpg?raw=true" alt="5" style="zoom: 33%;" />      
```python
>>>"{}{}{}".format("圆周率是",3.1415926,"...")
'圆周率是3.1415926...'
>>> "圆周率{{{1}{2}}}是{0}".format("无理数",3.1415926,"...")
'圆周率{3.1415926...}是无理数'
>>> s="圆周率{{{1}{2}}}是{0}"           #大括号本身是字符串的一部分
>>> s
'圆周率{{{1}{2}}}是{0}'
>>> s.format("无理数",3.1415926,"...")     #当调用format()时解析大括号
'圆周率{3.1415926...}是无理数'
```
#### format（）方法的格式控制   
&emsp;&emsp;format()方法中模板字符串的槽除了包括参数序号，还可以包括格式控制信息。此时，槽的内部样式如下:  
&emsp;&emsp;{<参数序号>: <格式控制标记>}    
&emsp;&emsp;其中，格式控制标记用来控制参数显示时的格式，格式内容如图所示。   

| ：       | <填充>                      | <对齐>                                                 | <宽度>                       | <， >                              | <.精度>                                    | <类型>                               |
| -------- | --------------------------- | ------------------------------------------------------ | :--------------------------- | ---------------------------------- | ------------------------------------------ | ------------------------------------ |
| 引导符号 | 用于填充         的单个字符 | \<左对齐 >右对齐;                            ^居中对齐 | 槽的设定            输出宽度 | 数字的千位分隔符适用于整数和浮点数 | 浮点数小数部分的精度或字符串的最大输出长度 | 整数类型b,c,d,o,x,X浮点数类型e,E,f,% |
```python
>>> s="python"  
>>> "{0:30}".format(s)                    #默认左对齐
'python                        '
>>> "{0:>30}".format(s)                   #右对齐
'                        python'
>>> "{0:*^30}".format(s)                  #居中且使用*填充
'************python************'
>>> "{0:-^30}".format(s)                  #居中且使用-填充
'------------python------------'
>>> "{0:3}".format(s)
'python'

>>> "{0:-^20}".format(1234567890)
'-----1234567890-----'
>>> "{0:-^20,}".format(1234567890)         
'---1,234,567,890----'
>>> "{0:-^20}".format(12345.67890)
'-----12345.6789-----'
>>> "{0:-^20,}".format(12345.67890)
'----12,345.6789-----'

>>> "{0:.2f}".format(12345.67890)
'12345.68'
>>> "{0:H^20.3f}".format(12345.67890)
'HHHHH12345.679HHHHHH'
>>> "{0:.4}".format("python")
'pyth'
```
&emsp;&emsp;<类型>表示输出整数和浮点数类型的格式规则。对于整数类型，输出格式包括以下6种。  
&emsp;&emsp;(1) b:输出整数的二进制方式。   
&emsp;&emsp;(2)c:输出整数对应的Unicode字符。    
&emsp;&emsp;(3) d: 输出整数的十进制方式。      
&emsp;&emsp;(4) O:输出整数的八进制方式。       
&emsp;&emsp;(5) x:输出整数的小写十六进制方式。         
&emsp;&emsp;(6) X:输出整数的大写十六进制方式。    
```python
>>> "{0:b},{0:c},{0:d},{0:o},{0:x},{0:X}".format(425)
'110101001,Ʃ,425,651,1a9,1A9'
```
&emsp;&emsp;对于浮点数类型，输出格式包括以下4种。   
&emsp;&emsp;(1) e:输出浮点数对应的小写字母e的指数形式。   
&emsp;&emsp;(2) E:输出浮点数对应的大写字母E的指数形式。   
&emsp;&emsp;(3) f: 输出浮点数的标准浮点形式。  
&emsp;&emsp;(4) %:输出浮点数的百分形式。   
&emsp;&emsp;浮点数输出时尽量使用<.精度>表示小数部分的宽度，有助于更好控制输出格式。   
```python
>>> "{0:e},{0:E},{0:f},{0:%}".format(3.14)
'3.140000e+00,3.140000E+00,3.140000,314.000000%'
>>> "{0:.2e},{0:.2E},{0:.2f},{0:.2%}".format(3.14)
'3.14e+00,3.14E+00,3.14,314.00%'
```
## 程序的控制结构  
### 程序的分支结构  
#### 单分支结构：if语句  
| 操作符 | 数学符号 | 操作符含义 |
| ------ | -------- | ---------- |
| <      | <        | 小于       |
| <=     | ≤        | 小于或等于 |
| \>=    | ≥        | 大于或等于 |
| >      | >        | 大于       |
| ==     | =        | 等于       |
| ！=    | ≠        | 不等于     |

&emsp;&emsp;if语句的语法格式如下：  
&emsp;&emsp;if \<条件>:  
&emsp;&emsp;&emsp;&emsp; \<语句块>  
```python
PM=eval(input("请输入PM2.5数值："))
if 0<=PM<35:
    print("空气优质，快去户外运动！")
if 35<=PM<75:
    print("空气良好，适度户外运动！")
if 75<=PM:
    print("空气污染，请小心！")
```
#### 二分支结构：if-else语句  
&emsp;&emsp;if-else语句用来形成二分支结构，语法格式如下：   
&emsp;&emsp;if \<条件>:  
&emsp;&emsp;&emsp;&emsp; \<语句块1>  
&emsp;&emsp;else :  
&emsp;&emsp;&emsp;&emsp;\<语句块2>  
```python
PM=eval(input("请输入PM2.5数值："))
if PM>=75:
    print("空气存在污染，请小心！")
else:
    print("空气没有污染，可以开展户外运动！")
```
&emsp;&emsp;二分支结构还有一种更简洁的表达方式，适合通过判断返回特定值，语法格式如下:  
&emsp;&emsp;<表达式1>  if  <条件>  else  <表达式2>  
&emsp;&emsp;其中，表达式1/2一般是数学类型或字符串类型的一个值， 上述可以改造为  
```python
PM=eval(input("请输入PM2.5数值："))
print("空气{}污染！".format("存在" if PM>=75 else "没有"))
```
```python
>>> count=2
>>> count if count!=0 else "不存在"
2
>>> count=0
>>> count if count!=0 else "不存在"
'不存在'
```
#### 多分支结构：if-elif-else语句  
&emsp;&emsp;if-elif-else描述多分支结构，语句格式如下：  
&emsp;&emsp;if \<条件1>:  
&emsp;&emsp;&emsp;&emsp;\<语句块1>  
&emsp;&emsp;elif \<条件2>:  
&emsp;&emsp;&emsp;&emsp;\<语句块2>  
&emsp;&emsp;...  
&emsp;&emsp;else:  
&emsp;&emsp;&emsp;&emsp;\<语句块N>  
```python
PM=eval(input("请输入PM2.5数值："))
if 0<=PM<35:
    print("空气优质，快去户外运动！")
else 35<=PM<75:
    print("空气良好，适度户外运动！")
else:
    print("空气污染，请小心！")
```
### 程序的循环结构  
#### 遍历循环：for语句  
&emsp;&emsp;python通过保留字for实现”遍历循环“，基本使用方法如下：  
&emsp;&emsp;for \<循环变量> in \<遍历结构>:  
&emsp;&emsp;&emsp;&emsp;\<语句块>  
&emsp;&emsp;遍历结构可以是字符串、文件、组合数据类型或rangeO函数等，常用的使用方式如下:  
&emsp;&emsp;循环N次  
&emsp;&emsp;for i in range (N) :  
&emsp;&emsp;&emsp;&emsp;<语句块>  
&emsp;&emsp;遍历文件fi的每一行  
&emsp;&emsp;for line in fi :  
&emsp;&emsp;&emsp;&emsp;<语句块>  
&emsp;&emsp;遍历字符串s  
&emsp;&emsp;for c in s:  
&emsp;&emsp;&emsp;&emsp;<语句块>  
&emsp;&emsp;遍历列表ls  
&emsp;&emsp;for item in ls:  
&emsp;&emsp;&emsp;&emsp;<语句块>  
&emsp;&emsp;遍历循环还有一种扩 展模式，使用方法如下:  
&emsp;&emsp;for  <循环变量>  in  <遍历结构>:  
&emsp;&emsp;&emsp;&emsp;<语句块1>  
&emsp;&emsp;else:  
&emsp;&emsp;&emsp;&emsp;<语句块2>  
```
for s in "BIT":
    print("循环进行中:"+ s)     
else:
    s = "循环正常结束"
print(s)
```
&emsp;&emsp;程序执行后的结果如下:  
```
>>> 
循环进行中:B
循环进行中:I
循环进行中:T
循环正常结束
```
#### 无限循环：while语句      
&emsp;&emsp;python通过保留字while实现无限循环，基本使用方法如下：  
&emsp;&emsp;while \<条件>:  
&emsp;&emsp;&emsp;&emsp;\<语句块>  
&emsp;&emsp;无限循环也有一种使用保留字elsede扩 展模式，使用方法如下:  
&emsp;&emsp;while  <条件>:  
&emsp;&emsp;&emsp;&emsp;<语句块1>  
&emsp;&emsp;else:  
&emsp;&emsp;&emsp;&emsp;<语句块2>  
```
s,idx = "BIT",0
while idx < len(s):
    print("循环进行中："+s[idx])
    idx += 1
else:
    s = "循环正常结束"
print(s)
```
&emsp;&emsp;程序执行后的结果如下：  
```
>>> 
循环进行中：B
循环进行中：I
循环进行中：T
循环正常结束
```
#### 循环保留字：break和continue  
&emsp;&emsp;循环结构有两个保留字：break和continue，他们用来辅助控制循环执行。  
&emsp;&emsp;break用来跳出最内层for或while循环，脱离该循环后程序从循环代码后继续执行， 例如：  
```python
for s in "BIT":     
    for i in range(10):
        print(s,end="")
        if s=="I":
            break
```
&emsp;&emsp;程序执行后的结果如下:  
```python
>>> 
BBBBBBBBBBITTTTTTTTTT
```
&emsp;&emsp;Contine 用来结束当前当次循环，即跳出循环体中下面尚未执行的语句，但不跳出当前循环。对于while循环，继续求解循环条件。而对于for循环，程序流程接着遍历循环列表。对比continue和break语句，如下:  
```
for s in"PYTHON":
    if s=="T":
        continue
    print(s, end="")
```
&emsp;&emsp;执行结果：  
```
>>> 
PYHON
```
```
for s in"PYTHON":
    if s=="T":
        break
    print(s, end="")
```
&emsp;&emsp;执行结果：  
```
>>> 
PY
```
&emsp;&emsp;continue语句和break语句的区别是，continue 语句只结束本次循环，而不终止整个循环的执行:而break 语句则是结束整个循环过程，不再判断执行循环的条件是否成立。  
&emsp;&emsp;for循环和while循环中都存在一个 else 扩展用法。else 中的语句块只在一种条件下执行，即循环正常遍历了所有内容或由于条件不成立而结束循环，没有因为break或return (函数返回中使用的保留字)而退出。continue 保留字对else没有影响。看下面两个例子:  
```python
for s in "PYTHON" :
    if s=="T":
        continue
    print(s, end="")
else:
    print ("正常退出")
    
for s in "PYTHON" :
    if s=="T":
        break
    print(s, end="")
else:
    print ("正常退出")
```
&emsp;&emsp;两个程序执行后的结果分别如下:  
```python
>>> 
PYHON正常退出
PY
```
## 函数和代码复用  
### 函数的基本使用  
#### 函数的定义  
&emsp;&emsp;函数是一-段具有特定功能的、可重用的语句组，用函数名来表示并通过函数名进行功能调用。函数也可以看作是一段具有 名字的子程序，可以在需要的地方调用执行，不需要在每个执行的地方重复编写这些语句。每次使用函数可以提供不同的参数作为输入，以实现对不同数据的处理:函数执行后，还可以反馈相应的处理结果。函数能够完成特定功能，与黑盒类似，对函数的使用不需要了解函数内部实现原理，只要了解函数的输入输出方式即可。严格地说，函数是一 种功能抽象。  
&emsp;&emsp;有些函数是用户自己编写的，称为自定义函数: Python 安装包也自带了一些函数和方法，包括Python内置的函数(如abs()、eval()、 Python标准库中的函数(如math库中的sqrt()等。
&emsp;&emsp;Python使用def保留字定义一个函数， 语法形式如下:  
&emsp;&emsp;def <函数名>(<参数列表>):  
&emsp;&emsp;<函数体>  
&emsp;&emsp;return <返回值列表>  
&emsp;&emsp;对比下面两个代码：  
```python
print ("Happy birthday to you!")
print ("Happy birthday to you!")
print ("HapPy birthday, dear Mike!")
print("Happy birthday to you!")
```
&emsp;&emsp;结果如下：  

```python
>>> 
Happy birthday to you!
Happy birthday to you!
HapPy birthday, dear Mike!
Happy birthday to you!
```
```python
def happy():
    print("Happy birthday to you!")
def happyB (name) :
    happy ()
    happy ()
    print("Happy birthday, dear {}!". format (name))
    happy()
happyB("Mike")
happyB("Lily")
```
&emsp;&emsp;结果如下：  
```python
>>> 
Happy birthday to you!
Happy birthday to you!
Happy birthday, dear Mike!
Happy birthday to you!
Happy birthday to you!
Happy birthday to you!
Happy birthday, dear Lily!
Happy birthday to you!
```
&emsp;&emsp;实例代码中第3行定义了一个函数happyB()，括号中的name是形参，用来指代要输入函数的实际变量，并参与完成函数内部功能。第8和第10行调用两次happyB0函数，输入的"Mike"和"Lily"是实参，替换name,用于函数执行。  
#### 函数的调用过程  
&emsp;&emsp;程序调用一个函数需要执行以下 4个步骤。  
&emsp;&emsp;(1)调用程序在调用处暂停执行。  
&emsp;&emsp;(2)在调用时将实参复制给函数的形参。  
&emsp;&emsp;(3)执行函数体语句。  
&emsp;&emsp;(4)函数调用结束给出返回值，程序回到调用前的暂停处继续执行。  
#### lambda  
&emsp;&emsp;Python 的33个保留字，其中一个是 lambda,该保留字用于定义.种特殊的函数一- 匿名函数，又称lamnbda函数。器名函数并非没有名字，而是将函数名作为函数结果返回，语法格式如下:  
&emsp;&emsp;<函数名> = lambda <参数列表>: <表达式>  
&emsp;&emsp;lambda函数与正常函数一样， 等价于下面形式:  
&emsp;&emsp;def <函数名>(<参数列表>) :  
&emsp;&emsp;return <表达式>  
&emsp;&emsp;简单地说，lambda函数用于定义简单的、能够在一行内表示的函数， 返回一个函数类型，实例如下:  
```python
>>> f=lambda x,y:x+y	      
>>> type(f)	      
<class 'function'>
>>> f(10,12)	      
22
```
### 函数的参数传递  
#### 可选参数和可变数量参数  
&emsp;&emsp;在定义函数时，如果有些参数存在默认值，即部分参数不一定需要调用程序输入，可以在定义函数时直接为这些参数指定默认值。当函数被调用时，如果没有传入对应的参数值，则使用丽数定义时的默认值替代，例如:  
```python
>>> def dup(str, times = 2):
	      print (str* times)      
>>> dup ("knock~")      
knock~knock~
>>> dup ("knock~",4)	      
knock~knock~knock~knock~
>>> dup (times=4,str="knock~")      
knock~knock~knock~knock~
```
&emsp;&emsp;在函数定义时，也可以设计可变数量参数，通过在参数前增加星号(\*) 实现。带有星号的可变参数只能出现在参数列表的最后。调用时，这些参数被当作元组类型传递到函数中，实例如下:  
```python
>>> def vfunc(a,*b):         
	print(type(b))
	for n in b:
	      a+=n
	return a	     
>>> vfunc(1,2,3,4,5)	      #函数定义了可变参数b，输入的（2,3,4,5）当做元组传递给b
<class 'tuple'>
15
```
#### 参数的位置和名称传递  
#### 函数的返回值  
&emsp;&emsp;return语句用来退出函数并将程序返回到函数被调用的位置继续执行。return语句可以同时将0个、1个或多个函数运算后的结果返回给函数被调用处的变量，例如：  
```python
>>> def func(a,b):         
	return a*b	      
>>> s=func("knock~",2)      
>>> print(s)	      
knock~knock~
   
```
&emsp;&emsp;函数可以没有return，此时函数并不返回值，如之前的happy()函数。函数也可以用return返回多个值，多个值以元组类型保存，例如：  
```python
>>> def func(a,b):         
	return b,a	      
>>> s=func("knock~",2)	      
>>> print(s,type(s))      
(2, 'knock~') <class 'tuple'>
```
#### 函数对变量的作用  
&emsp;&emsp;一个程序中的变量包括两类:全局变量和局部变量。全局变量指在函数之外定义的变量，般没有绵进， 在程序执行全过程有效。局部变量指在函数内部使用的变量，仅在函数内部有效，当函数退出时变量将不存在。例如:  
```python
>>>n = 1                      #n是全局变量
>>> def func(a,b):         
	c=a*b                     #c是局部变量，a和b作为函数参数也是局部变量
	return c	      
>>> s=func("knock~",2)	      
>>> print(c)	      
Traceback (most recent call last):
  File "<pyshell#141>", line 1, in <module>
    print(c)
NameError: name 'c' is not defined
```
&emsp;&emsp;这个例子说明，当函数执行完退出后，其内部变量将被释放。  
&emsp;&emsp;如果函数内部使用了全局变量呢?例如:  
```python
>>> n = 1   #n是全局变量	      
>>> def func(a,b):         
	n=b           #这个n是在函数内存中新生成的局部变量，不是全局变量
	return a*b	      
>>> s=func("knock~",2)	      
>>> print(s,n)    #测试一下n的值是否改变	      
knock~knock~ 1
```
&emsp;&emsp;如果希望让func()函数将n当成全局变量，需要在变量n使用前显示声明该变量为全局变量，代码如下：  
```python
>>> n = 1              #n是全局变量	      
>>> def func(a,b):         
	global n   
	n=b                #将局部变量b赋值给全局变量n
	return a*b	      
>>> s=func("knock~",2)	      
>>> print(s,n)          #测试一下n的值是否改变	      
knock~knock~ 2
```
&emsp;&emsp;对比下面两个代码：  
```python
>>> ls=[]                   #ls是全局列表变量
>>> def func(a,b):
	ls.append(b)            #将局部变量b增加到全局列表变量ls中
	return a*b
>>> s=func("knock~",2)
>>> print(s,ls)           #测试一下ls值是否改变
knock~knock~ [2]
```
&emsp;&emsp;列表等组合数据类型由于操作多个数据，所以它们在使用中有创建和引用的分别。当列表变量被方括号([], 无论是否为空)赋值时，这个列表才被真实创建，否则只是对之前创建列表的一次引用。  
&emsp;&emsp;上述代码func()函数的ls.append(b)语句执行时需要-一个真实创建过的列表，此时func(函数专属的内存空间中没有已经创建过且名称为ls 的列表，因此，func()函数进一步去寻找全局内存空间，自动关联全局1s列表，并修改其内容。当func()函数退出后，全局Is列表中的内容被修改。简单地说，对于列表类型，函数可以直接使用全局列表而不需要采用global进行声明。  
&emsp;&emsp;如果func()函数内部存在一一个真实 创建过且名称为Is 的列表，则func0函数将操作该列表而不会修改全局变量，例如:  
```python
>>> ls=[]                   #ls是全局列表变量
>>> def func(a,b):
	ls=[]                   #创建了名称为ls的局部列表变量
	ls.append(b)            #将局部变量b增加到全局列表变量ls中
	return a*b
>>> s=func("knock~",2)
>>> print(s,ls)           #测试一下ls值是否改变
knock~knock~ []
```
### python内置函数  
&emsp;&emsp;Python解释器提供了68个内置函数，这些函数不需要引用库直接使用，如表所示。 其中一部分已经在之前的内容中出现，需要读者掌握。  
|           |            |               |              |                  |
| --------- | ---------- | ------------- | ------------ | ---------------- |
| abs()     | id()       | round()       | compile()    | locals()         |
| all()     | input()    | set()         | dir()        | map()            |
| any()     | int()      | sorted()      | exec()       | memoryview()     |
| asci()    | len()      | str()         | enumerate()  | next()           |
| bin()     | list()     | tuple()       | filter()     | object()         |
| bool()    | max()      | type()        | format()     | property()       |
| chr()     | min()      | zip           | frozenset()  | repr()           |
| complex() | oct()      |               | getattr()    | setattr()        |
| dict()    | open()     |               | globals()    | slice()          |
| divmod()  | ord()      | bytes()       | hasattr()    | staticmethod()   |
| eval()    | pow()      | delattr()     | help()       | sum()            |
| float()   | print()    | bytearray()   | isinstance() | super()          |
| hash()    | range()    | callable()    | issubclass() | vars()           |
| hex()     | reversed() | classmethod() | iter()       | \_\_import()\_\_ |

&emsp;&emsp;all()函数一般针对组合数据类型，如果其中每个元素都是True,则返回True,否则返回False。需要注意的是，整数0、空字符串""、空列表[]等都被当作False。  
&emsp;&emsp;any()函数与all()函数相反，只要组合数据类型中任何一个是True, 则返回True,全部元素都是False时返回False。  
&emsp;&emsp;hash()函数对于能够计算哈希的类型返回哈希值。  
&emsp;&emsp;id()函数对每一个数据返回唯一编号，数据不同编号不同，可以通过比较两个变量编号是否相同判断数据是否一致。Python将数据存储在内存中的地址作为其唯一编号。  
&emsp;&emsp;reversed()函数返回输入组合数据类型的逆序形式。  
&emsp;&emsp;sorted()函数对一个序列进行排序，默认从小到大排序。  
&emsp;&emsp;type()函数返回每个数据对应的类型。  
&emsp;&emsp;上述函数的一些实例如下:  
```python
>>> ls=[1,2,5,0]
>>> all(ls)
False
>>> any(ls)
True
>>> hash("中国，你好")
913584788464011166
>>> id(ls)
47574600
>>> id("中国，你好")
49997384
>>> list(reversed(ls))
[0, 5, 2, 1]
>>> sorted(ls,reverse=True)
[5, 2, 1, 0]
>>> sorted(ls,reverse=False)
[0, 1, 2, 5]
>>> ls
[1, 2, 5, 0]
>>> type(ls)
<class 'list'>
>>> type(reversed(ls))
<class 'list_reverseiterator'>
```
## 组合数据类型  
### 组合数据类型概括  
#### 序列类型  
序列类型有12个操作符和函数，如图：  
| 操作符              | 描述                                                     |
| ------------------- | -------------------------------------------------------- |
| X inS               | 如果x是s的元素，返回True,否则返回False                   |
| XnotinS             | 如果x不是s的元素，返回True,否则返回                      |
| FalseS+t            | 连接s和t                                                 |
| s*n或n*S            | 将序列s复制n次                                           |
| s[i]                | 索引，返回序列的第i个元素                                |
| s[i:j]              | 分片，返回包含序列s第i到j个元素的子序列(不包含第j个元素) |
| s[i:j:k]            | 步骤分片，返回包含序列s第i到j个元素以k为步数的子序列     |
| len(s)              | 序列s的元素个数(长度)                                    |
| min(s)              | 序列s中的最小元素                                        |
| max(s)              | 序列s中的最大元素                                        |
| s.index(x[, i[, j]) | 序列s中从i开始到j位置中第一次出现元素x的位置             |
| s.count(x)          | 序列s中出现x的总次数                                     |

&emsp;&emsp;元组(tuple)是序列类型中比较特殊的类型，因为它且创建就不能被修改，元组类型在表达固定数据项、雨数多返回值、多变量同步赋值，循环遍历等情况下十分有用。Pyhon中元组采用逗号和圆括号(可选)来表示，例如：  
```python
>>> creature = "cat", "dog", "tiger","human"
>>> creature
('cat', 'dog', 'tiger', 'human')
>>> color = ("red",0x001100,"b1ue",creature)
>>> color
('red', 4352, 'b1ue', ('cat', 'dog', 'tiger', 'human'))
>>> color[2]
'b1ue'
>>> color[-1][2]
'tiger'
```
&emsp;&emsp;元组除了用于表达固定数据项外，还常用于如下3种情况:函数多返回值、多变量同步赋值、循环遍历，例如：  
```python
>>>def func(x): #函数多 返回值
		return x，x**3
>>>a，b = 'dog', 'tiger'    #多变量同步赋值
>>>a, b = (b, a)            #多变量同步赋值，括号可省略
>>> import math
>>>for x，y in ((1,0)， (2,5)， (3,8)):    #循环遍历
		print (math。hypot(x,y))           #求多个坐标值到原点的距离
```
#### 集合类型  
&emsp;&emsp;集合类型与数学中集合的概念一样，即包含0个或多个数据项的无序组合。集合中的元素不可重复，元素类型只能是股东数据类型，例如整数、浮点数、字符串、元组等，列表、字典和集合类型本身都是可变数据类型，不能作为集合的元素出现。由于集合是无序组合，它没有索引和位置的概念，不能分片，集合中元素可以动态增加或删除，集合用大括号（{}）表示。  
```python
>>>S = {425,"BIT",(10,"CS"),424}
>>>S
{'BIT', 425, (10, 'CS'), 424}     #集合元素是无序的，打印效果与定义顺序可以不一致
>>> T = {425,"BIT",(10,"CS"),424,425,"BIT"}
>>> T
{'BIT', 425, (10, 'CS'), 424}      #能够过滤掉重复元素
```
&emsp;&emsp;set(x)函数可以用于生成集合，输入的参数可以是任何组合数据类型，返回结果是一个无重复且排序任意的集合，例如：  
```python
>>> W = set ("apple")
>>> W
{'e', 'l', 'a', 'p'}
>>> V = set(("cat","dog","tiger","human") )
>>> V
{'tiger', 'dog', 'cat', 'human'}
```
&emsp;&emsp;集合类型有10个操作符，如表所示：  
| 操作符                                | 描述                                                         |
| ------------------------------------- | ------------------------------------------------------------ |
| S-T或S.difTerence(T)                  | 返回一个新集合，包括在集合S中但不在集合T中的元素             |
| S-=T成S.difference_update(T)          | 更新集合S，包括在集合S中但不在集合T中的元素                  |
| S&T或S.intersection(T)                | 返回一个新集合，包括同时在集合S和T中的元素                   |
| S&=T或S.intersection_update(T)        | 更新集合S，包括同时在集合S和T中的元素                        |
| S^T或s.symmetric_difference(T)        | 返回一个新集合，包括集合S和T中的元素，但不包括同时在其中的元素 |
| S^T或s.symmetric_difference_update(T) | 更新集合S，包括集合S和T中的元素，但不包括同时在其中的元素    |
| S\|T或S.union(T)                      | 返回一个新集合，包括集合S和T中的所有元素                     |
| S\|=T或S.update(T)                    | 更新集合S，包括集合S和T中的所有元素                          |
| S<=T或S.issubset(T)                   | 如果S与T相同或S是T的子集，返回True,否则返回False,可以用S<T判断S是否是T的真子集 |
| S>=T或S.issuperset(T)                 | 如果S与T相同或S是T的超集，返回True,否则返回False,可以用S>T判断S是否是T的真超集 |

&emsp;&emsp;集合类型有10个操作函数或方法，如表所示。  
| 操作函数或方法  | 描述                                                   |
| --------------- | ------------------------------------------------------ |
| S.add(x)        | 如果数据项x不在集合S中，将x增加到s                     |
| S.clear()       | 移除s中的所有数据项                                    |
| S.copy()        | 返回集合S的一个副本                                    |
| S.pop()         | 随机返回集合S中的一个元素，如果S为空，产生KeyError异常 |
| S.discard(x)    | 如果x在集合S中，移除该元素；如果x不在集合S中，不报错   |
| S.remove(x)     | 如果x在集合S中，移除该元素；不在则产生KeyError异常     |
| S.isdisjoint(T) | 如果集合S与T没有相同元素，返回True                     |
| len(S)          | 返回集合S的元素个数                                    |
| x in S          | 如果x是S的元素，返回True；否则返回False                |
| X not in S      | 如果x不是S的元素，返回True，否则返回False              |

&emsp;&emsp;集合类型主要用于3个场景:成员关系测试、元素去重和删除数据项，例如：  
```python
>>> "BIT" in ("PYTHON","BIT",123,"G0OD")      #成员关系测试
True
>>> tup=("PYTHON","BIT",123,"GOOD",123)        #元素去重
>>> set(tup)
{'BIT', 'PYTHON', 123, 'GOOD'}
>>> newtup = tuple(set(tup)-{'PYTHON'})        #去重同时删除数据项
>>> newtup
('BIT', 123, 'GOOD')
```
#### 映射类型  
&emsp;&emsp;映射类型是“键-值”数据项的组合，每个元素是一个键值对，即元素是（key，value），元素之间是无序的。键值对（key，value）是一种二元关系，属于属性和值的映射关系。在python中，映射类型主要以字典（dict）体现。  
### 列表类型和操作  
#### 列表类型的概念  
&emsp;&emsp;列表(ist)是包含0个或多个对象引用的有序序列，属于序列类型。与元组不同，列表的长度和内容都是可变的，可自由对列表中的数据项进行增加、删除或替换。列表没有长度限制，元素类型可以不同，使用非常灵活。列表用中括号([]])表示，也可以通过list()函数将元组或字符串转化成列表。直接使用list()函数会返回一个空列表，例如:  
```python
>>> ls = [425,"BIT",[10,"CS"],425]
>>> ls
[425, 'BIT', [10, 'CS'], 425]
>>> ls[2][-1][0]
'C'
>>> list((425,"BIT",[10,"CS"],425))
[425, 'BIT', [10, 'CS'], 425]
>>> list("中国是一个伟大的国家")
['中', '国', '是', '一', '个', '伟', '大', '的', '国', '家']
>>> list()
[]
```
&emsp;&emsp;与整数和字符串不同，列表要处理一组数据，因此，列表必须通过显示的数据赋值才能生成，简单将一个列表赋值给另一个列表不会生成新的列表对象，例如：  
```python
>>> ls=[425,"BIT",1024]   #用数据赋值产生列表ls
>>> lt=ls                 #lt是ls所对应数据的引用，lt并不包含真实数据
>>> ls[0] = 0
>>> lt
[0, 'BIT', 1024]
```
#### 列表类型的操作  
&emsp;&emsp;列表是序列类型，因此，序列类型的操作符和函数都可应用于列表类型。由于列表是可变的，下面给出了列表类型额外的14 个常用函数或方法。  
| 函数或方法            | 描述                                                |
| --------------------- | --------------------------------------------------- |
| ls[i]=x               | 替换列表ls第i数据项为x                              |
| Is[i:j]=lt            | 用列表lt替换列表Is中第i到第j项数据(不含第j项，下同) |
| ls[i:j:k]=lt          | 用列表lt替换列表ls中第i到第j项以k为步数的数据       |
| del Is[i:j]           | 删除列表Is第i到第j项数据，等价于Is[i:j]=[]          |
| del ls[i:j:k]         | 删除列表ls第i到第j项以k为步数的数据                 |
| Is+=lt或ls.extend(It) | 将列表lt元素增加到列表Is中                          |
| ls\*=n                 | 更新列表ls,其元素重复n次                            |
| ls.append(x)          | 在列表ls最后增加一个元素x                           |
| ls.clear()            | 删除ls中的所有元素                                  |
| ls.copy()             | 生成一个新列表，复制ls中的所有元素                  |
| ls.insert(i, x)       | 在列表ls的第i位置增加元素x                          |
| ls.pop(i)             | 将列表ls中的第i项元素取出并删除该元素               |
| Is.remove(x)          | 将列表中出现的第一个元素x删除                       |
| ls..reverse()         | 列表ls中的元素反转                                  |
```python
>>> vlist=list(range(5))
>>> vlist
[0, 1, 2, 3, 4]
>>> len(vlist[2:])    #计算从第3个位置F始到结尾的子串长度
3
>>> 2 in vlist   #判断2是否在列表vlist中
True
>>> vlist[3]="python"  #修改序号3的元素值和类型
>>> vlist
[0, 1, 2, 'python', 4]
>>> vlist[1:3]=["bit","computer"]
>>> vlist
[0, 'bit', 'computer', 'python', 4]
>>> vlist[1:3]=["new_ bit","new_ computer",123]
>>> vlist
[0, 'new_ bit', 'new_ computer', 123, 'python', 4]
>>> vlist[1:3]=["fewer"]
>>> vlist
[0, 'fewer', 123, 'python', 4]
```
&emsp;&emsp;与元组一样， 列表可以通过for-in语句对其元素进行遍历，基本语法结构如下：  
&emsp;&emsp;for <任意变量名> in <列表名>:  
&emsp;&emsp;&emsp;&emsp;<语句块>  
```python
>>> for e in vlist:
		print(e, end=" ")
0 fewer 123 python 4 
```
### 字典类型和操作  
#### 字典类型的概念  
&emsp;&emsp;通过任意键信息查找一组数据中值信息的过程叫映射，python语言中通过字典实现映射。python语言中字典可以通过大括号（{}）建立，建立模式如下：  
&emsp;&emsp;{<键1>:<值1>， <键2>:<值2>，... ，<键n>:<值n>}  
```python
>>>Dcountry={"中国":"北京","美国":"华盛顿","法国":"巴黎"}
>>>print (Dcountry)
{中国': '北京'， '法国': ，巴黎'，'美国': ，华盛顿'} #字典是集合类型的延续，所以元素没有顺序之分
>>> Dcountry["中国"]              #键值对的访问模式：<值>=<字典变量>[<键>]
'北京'
>>> Dcountry["中国"]="大北京"       
>>> print(Dcountry)
{'中国': '大北京', '美国': '华盛顿', '法国': '巴黎'}
```
#### 字典类型的操作  
&emsp;&emsp;字典可以使用大括号可以创建字典，并指定初始值，通过中括号可以增加新的元素，例如：  
```python
>>> Dcountry={"中国":"北京","美国":"华盛顿","法国":"巴黎"}
>>> Dcountry["英国"]="伦敦"
>>> print(Dcountry)
{'中国': '北京', '美国': '华盛顿', '法国': '巴黎', '英国': '伦敦'}
```
&emsp;&emsp;直接使用大括号({}) 可以创建一个空的字典，并通过中括号(0]) 向其增加元素，例如：  
```python
>>> Dp={}
>>> Dp['2^10']=1024
>>> print(Dp)
{'2^10': 1024}
```
&emsp;&emsp;需要注意的是，尽管集合类型也用大括号表示，直接使用大括号({}) 生成一个空的字典，而不是集合。生成空集合需要使用函数set()。  
&emsp;&emsp;字典在Python内部也已采用面向对象方式实现，因此也有一些对应的方法，采用\<a>.\<b>()格式，此外，还有一些函数能够用于操作字典，这些函数和方法如表所示。  
| 函数和方法                    | 描述                                                   |
| ----------------------------- | ------------------------------------------------------ |
| \<d> keys()                   | 返回所有的键信息                                       |
| \<d>.values()                 | 返回所有的值信息                                       |
| \<d>.items()                  | 返回所有的键值对                                       |
| \<d>. get(\<key>,\<default>)  | 键存在则返回相应值，否则返回默认值                     |
| \<d> .pop( \<key>,\<default>) | 键存在则返回相应值，同时删除键值对，否则返回默认值     |
| \<d>.popitem()                | 随机从字典中取出一个键值对，以元组(key, value)形式返回 |
| \<d>.clear()                  | 删除所有的键值对                                       |
| del\<d>[\<key>]               | 删除字典中某一个键值对                                 |
| \<key> in \<d>                | 如果键在字典中则返回True，否则返回False                |
```python
>>> Dcountry={"中国":"北京","美国":"华盛顿","法国":"巴黎"}	      
>>> Dcountry.keys()	      
dict_keys(['中国', '美国', '法国'])
>>> list(Dcountry.values())	      
['北京', '华盛顿', '巴黎']
>>> Dcountry.items()	      
dict_items([('中国', '北京'), ('美国', '华盛顿'), ('法国', '巴黎')])
>>> '中国' in Dcountry   #只对键进行判断	      
True
>>> Dcountry.get('美国','悉尼')  #'美国'在字典中存在	      
'华盛顿'
>>> Dcountry.get('澳大利亚','悉尼')  #'澳大利亚'在字典中不存在	      
'悉尼'
```
&emsp;&emsp;与其他组合类型样， 字典可以通过for-in 语句对其元素进行遍历， 基本语法结构如下：  
&emsp;&emsp;for <变量名> in <字典名>:  
&emsp;&emsp;&emsp;&emsp;<语句块>  
&emsp;&emsp;由于键值对中的键相当于索引，因此，for 循环返回的变量名是字典的索引值。如果需要获得键对应的值，可以在语句块中通过get()方法获得。  

```python
>>> for key in Dcountry:
	print(key)
	print(Dcountry.get(key))	      
中国
北京
美国
华盛顿
法国
巴黎
```
## 文件和数据格式化  
### 文件的使用  
#### 文件的概述  
&emsp;&emsp;文件包括两种类型:文本文件和二进制文件。   
&emsp;&emsp;文本文件一般由单一特定编码的字符组成，如UTF-8 编码，内容容易统展示和阅读。大部分文本文件都可以通过文本编辑软件或文字处理软件创建、修改和阅读。由于文本文件存在编码，因此，它也可以被看作是存储在磁盘上的长字符串，例如一个txt格式的文本文件。  
&emsp;&emsp;二进制文件直接由比特0和比特1组成，没有统一字符编码， 文件内部数据的组织格式与文件用途有关。二进制是信息按照非字符但特定格式形成的文件，例如，png格式的图片文件、avi 格式的视频文件。二进制文件和文本文件最主要的区别在于是否有统一-的字符编码。二进制文件由于没有统一字符编码， 只能当作字节流，而不能看作是字符串。   
&emsp;&emsp;理解文本文件和二进制文件的区别。  
&emsp;&emsp;首先，用文本编辑器生成一个包含“中国是个伟大的国家!”的txt格式文本文件，命名为1.txt。分别用文本文件方式和二进制文件方式读入，并打印输出效果，代码如下：  
```python
textFile=open("1.txt","rt")   #t表示文本文件方式
print(textFile.readline())
textFile.close()
binFile=open("1.txt","rb")    #b表示二进制文件方式
print(binFile.readline())
binFile.close()
```
&emsp;&emsp;输出结果：  
```python
>>> 
中国是个伟大的国家!
b'\xd6\xd0\xb9\xfa\xca\xc7\xb8\xf6\xce\xb0\xb4\xf3\xb5\xc4\xb9\xfa\xbc\xd2!'
```
#### 文件的打开关闭  
&emsp;&emsp;Python通过解释器内置的open(函数打开-一个文件，并实现该文件与一个程序变量的关联，open()函数格式如下:  
&emsp;&emsp;<变量名> = open(<文件名>，<打开模式>)  
&emsp;&emsp;open()函数有两个参数：文件名和打开模式。文件名可以是文件的实际名字，也可以是包含完整路径的名字。打开模式用于控制使用何种方式打开文件，open()函数提供7种基本的打开模式，如表所示。  
| 文件的打开模式 | 含义                                                        |
| -------------- | ----------------------------------------------------------- |
| 'r'            | 只读模式，如果文件不存在，返回异常FileNotFoundError, 默认值 |
| 'w'            | 覆盖写模式，文件不存在则创建，存在则完全覆盖                |
| 'x'            | 创建写模式，文件不存在则创建，存在则返回异常FileExistsError |
| 'a'            | 追加写模式，文件不存在则创建，存在则在文件最后追加内容      |
| 'b'            | 二进制文件模式                                              |
| 't'            | 文本文件模式，默认值                                        |
| '+'            | 与r/w/x/a一同使用，在原功能基础上增加同时读写功能           |

&emsp;&emsp;文件使用结束后要用close()方法关闭，释放文件的使用授权，该方法的使用方式如下：    
&emsp;&emsp;<变量名>.close ()    
#### 文件的读写  
&emsp;&emsp;当文件被打开后，根据打开方式不同可以对文件进行相应的读写操作。注意，当文件以文本文件方式打开时，读写按照字符串方式，采用当前计算机使用的编码或指定编码；当文件以二进制文件方式打开时，读写按照字节流方式。Python 提供4个常用的文件内容读取方法，如表所示。
| 操作方法                   | 含义                                                         |
| -------------------------- | ------------------------------------------------------------ |
| \<file>.readall()          | 读入整个文件内容，返回一个字符串或字节流\*                    |
| \<file>. read(size=-1)     | 从文件中读入整个文件内容，如果给出参数，读入前size长度的字符串或字节流 |
| \<file> .readline(size=-1) | 从文件中读入一行内容，如果给出参数，读入该行前size长度的字符串或字节流 |
| \<file>.readlines(hint=-1) | 从文件中读入所有行，以每行为元素形成一个列表，如果给出参数，读入hint行 |

&emsp;&emsp;\*：字符串或字节流取决于文件打开模式，如果是文本方式打开，返回字符串；否则返回字节流。下同。

&emsp;&emsp;用户输入文件路径，以文本文件方式读入文件内容并逐行打印，代码如下：

```python
fname=input("请输入要打开的文件：")
fo=open(fname,"r")
for line in fo.readlines()：
#文件的全部内容通过fo.readlines()方法读入到一个列表，列表的每个元素是文件一行的内容
    print(line)
fo.close()
```

&emsp;&emsp;上述代码尽管完成了要求，但存在一些缺点，当读入文件非常大时，一次性将内容读取到列表中会占用很多内存，影响程序执行速度。一个合理的方法是逐行读入内容到内存，并逐行处理。这可以通过一个简单的方法解决。Python将文件本身作为一个行序列，遍历文件的所有行可以直接这样完成:  

```python
fname=input("请输入要打开的文件：")
fo=open(fname,"r")
for line in fo:
    print(line)
fo.close()
```

&emsp;&emsp;python提供3个与文件内容写入相关的方法，如表所示。  
| 方法                      | 含义                                                         |
| ------------------------- | ------------------------------------------------------------ |
| \<file>.write(s)          | 向文件写入一个字符串或字节流                                 |
| \<file>.writelines(lines) | 将一个元素全为字符串的列表写入文件                           |
| \<file>.seek(offset)      | 改变当前文件操作指针的位置，offset的值：0——文件开头；1——当前位置；2——文件结尾 |

&emsp;&emsp;向文件写入一个列表类型，并打印输出结果，代码如下：  
```python
fname = input("请输入要写入的文件: ")
fo = open (fname, "w+")
ls = ["唐诗","宋词","元曲"]
fo. writelines (ls)
for line in fo:
    print (line)
fo.close ()
```

&emsp;&emsp;程序执行结果如下：  
```python
>>>请输入要写入的文件: test. txt
>>>
```

&emsp;&emsp;可以看到，程序并没有输出写入的列表内容。在该程序的目录中找到test.txt文件，打开可以看到其中的内容如下:  
&emsp;&emsp;唐诗宋词元曲   
&emsp;&emsp;列表ls内容被写入文件，但为何第5至第7行代码没有将这些内容打印出来呢？这是因为文件写入内容后，当前文件操作指针在写入内容的后面，第5至第7行代码从指针开始向后读入并打印内容，被写入的内容却在指针前面，因此未能被打印出来。为此，可以在写入文件后增加一条代码fo.seek(0)将文件操作指针返回到文件开始，即可显示写入的内容，代码如下：  
```python
fname = input("请输入要写入的文件: ")
fo = open (fname, "w+")
ls = ["唐诗","宋词","元曲"]
fo. writelines (ls)
fo.seek(0)
for line in fo:
    print (line)
fo.close ()
```
&emsp;&emsp;程序执行结果如下:  
```python
>>> 
请输入要写入的文件: test.txt
唐诗宋词元曲
```

&emsp;&emsp;fo. writelines (ls)方法并不在列表后面增加换行，只是将列表内容直接排列输出。  
### 一二维数据的格式化和处理     
####  数据组织的维度  
&emsp;&emsp;根据数据的关系不同，数据组织可以分为一维数据，二维数据和高维数据。  
&emsp;&emsp;一维数据由对等关系的有序或无序数据构成，采用线性方式组织，对应于数学中的数组和集合等概念。  
&emsp;&emsp;二维数据也称表格数据，由关联关系数据构成，采用表格方式组织，对应于数学中的矩阵，常见的表格都属于二维数据。如下，其中，表格说明部分 (第一行)可以看作是二维数据的一一个维度，也可以看作是数据外的说明。  
| 城市 | 环比  | 同比  | 定基  |
| ---- | ----- | ----- | ----- |
| 北京 | 101.5 | 120.7 | 121.4 |
| 上海 | 101.2 | 127.3 | 127.8 |
| 广州 | 101.3 | 119.4 | 120   |
| 深圳 | 102   | 140.9 | 145.5 |
| 沈阳 | 100.1 | 101.4 | 101.6 |

&emsp;&emsp;高维数据由键值对类型的数据构成，采用对象方式组织，属于整合度更好的数据组织方式。高维数据在网络系统中十分常用，HTML、XML、JSON等都是高维数据组织的语法结构。以描述本书作者的JSON格式为例，下 面给出了这种高维数据的表示形式，其中，"本书作者"和后续内容通过冒号(:) 形成一个键值对，每个内容中"姓氏"、"名字"和"单位"分别与后面的内容形成键值对。内容按照层级采用逗号和大括号组织起来。高维数据相比--维和二维数据能表达更加灵活和复杂的数据关系。       
```
"本书作者”: [
            {"姓氏" : "嵩"，
             "名字" : "天"，
             "单位" : "北京理工大学" }，
            {"姓氏" : "礼"，
             "名字" : "欣"，
             "单位" : "北京理工大学" }，
            {"姓氏”: "黄"，
             "名字" : "天羽"，
             "单位" : "北京理工大学"}
           ]
```
#### 一二维数据的存储格式  
&emsp;&emsp;一维 数据是最简单的数据组织类型，有多种存储格式，常用特殊字符分隔，分隔方式如下。  
&emsp;&emsp;(1)用一个或多个空格分隔  
&emsp;&emsp;(2) 用逗号分隔，注意，这里的逗号是英文输入法中的半角逗号，不是中文逗号  
&emsp;&emsp;(3)用其他符号或符号组合分隔，建议采用不出现在数据中的特殊符号  
&emsp;&emsp;二维数据由多条一维数据构成，可以看成是一维数据的组合形式。这里介绍一种国际通用的一维数据存储格式： CSV格式。这种格式十分简单， 来源于使用逗号分隔的一维数据表示方式。  
&emsp;&emsp;逗号分隔数值的存储格式叫做CSV格式(Comma-Separated Values, 逗号分隔值)，它是一种通用的、相对简单的文件格式，在商业和科学上广泛应用，尤其应用在程序之间转移表格数据。该格式的应用有如下一些基本规则。  
&emsp;&emsp;(1)纯文本格式，通过单一编码表示字符。  
&emsp;&emsp;(2)以行为单位，开头不留空行，行之间没有空行。  
&emsp;&emsp;(3)每行表示一个一维数据，多行表示二维数据。  
&emsp;&emsp;(4)以逗号(英文，半角)分隔每列数据，列数据为空也要保留逗号。  
&emsp;&emsp;(5)对于表格数据，可以包含或不包含列名，包含时列名放置在文件第一行。例如上面中的二维数据采用CSV存储后的内容如下:    
```
姓名,总成绩,排名
小红,198,1
小明,160,4
小王,188,2
小丽,178,3 
```
#### 一二维数据的表示和读写       
&emsp;&emsp;CSV文件的每一行是一维数据，可以使用Python中的列表类型表示，整个CSV文件是一个二维数据， 由表示每一行的列表类型作为元素， 组成一个二维列表。例如：  
```
[
 ['城市'，'环比'，'同比'，'定基\n'],
 ['北京'，'101.5', '120.7','121.4\n'],
 ['上海'，'101.2'，'127.3','127.8\n'],
 ['广州'，'101.3', '119.4','120\n'], 
 ['深圳，'102', '140.9','145.5\n']
 ['沈阳，'100.1','101.4','101.6\n']
]
```

&emsp;&emsp;将二维数据通过微软Office Excel 等工具录入，另存成文件city.csv，操作CSV文件的微实例代码如下:   
```python
fo = open ("city.csv", "r")
ls = []
for line in fo:
    line=line.replace("\n","")
    ls.append(line.split(","))
print(ls)
fo.close()
```

&emsp;&emsp;需要注意的是，以split(",")方法从CSV文件中获得内容时，每行最后一个元素后面包含了一个换行符("\n")。对于数据的表达和使用来说，这个换行符是多余的，可以通过使用字符串的replace()方法将其去掉，如第4行。执行结果如下：

```
>>> 
[['城市', '环比', '同比', '定基'], ['北京', '101.5', '120.7', '121.4'], ['上海', '101.2', '127.3', '127.8'], ['广州', '101.3', '119.4', '120'], ['深圳', '102', '140.9', '145.5'], ['沈阳', '100.1', '101.4', '101.6']]
```

&emsp;&emsp;以上从CSV文件中一次性读入全部数据写入列表，之后，在程序内部使用列表即可表达数据，这种一次性读入方式适合一部分应用。 另有一部分应用并不需要将数据全部读入程序再操作，可以逐行读取CSV文件，逐行运算处理，这种情况仅使用普通列表即可。  
```python
fo = open ("city.csv", "r")
ls = []
for line in fo:
    line=line.replace("\n","")
    ls=line.split(",")
    lns=""
    for s in ls:
        lns += "{}\t".format(s)
    print(lns)
fo.close()
```

&emsp;&emsp;执行结果：

```
>>> 
城市	环比	同比	定基	
北京	101.5	120.7	121.4	
上海	101.2	127.3	127.8	
广州	101.3	119.4	120	
深圳	102	140.9	145.5	
沈阳	100.1	101.4	101.6
```

&emsp;&emsp;一维数据写入csv文件：

```python
fo=open("city.csv", "w")
ls=['北京', '101.5', '120.7', '121.4']
fo.write(",".join(ls)+"\n")
fo.close()
```

&emsp;&emsp;二维数据写入csv文件：

&emsp;&emsp;读入city.csv文件，将其中的数据读出，将数字部分计算百分比后输出到cityout.csv文件。整个程序分为3个部分:首先将原始文件中的数据全部导入，用列表方式表示；第二，对列表中的元素逐行判断，对浮点数值进行百分比运算，运算结果写回列表；第三，将更新后的列表输出新的CSV文件，代码如下:

```python
fr = open ("city.csv", "r")
fw = open ("cityout.csv", "w")
ls = []
for line in fr:   #将CSV文件中的二维数据读入到列表
    line=line.replace("\n","")
    ls.append(line.split(","))
for i in range(len(ls)) :#遍历列表变量计算百分数
    for j in range(len(ls[i])):
        if ls[i][j].replace(".","").isnumeric():  
        #通过replace()方法将其中可能的小数点去掉，再通过isnumeric()方法判断其余字符是否都是数字
            ls[i][j]="{:.2}%".format(float(ls[i][j])/100)
for row in ls: #将列表 变量中的两位数据输出到CSV文件
    print (row)
    fw.write(",".join(row)+"\n")
fr.close ()
fw.close ()
```

&emsp;&emsp;执行结果：

```
>>> 
['城市', '环比', '同比', '定基']
['北京', '1.0%', '1.2%', '1.2%']
['上海', '1.0%', '1.3%', '1.3%']
['广州', '1.0%', '1.2%', '1.2%']
['深圳', '1.0%', '1.4%', '1.5%']
['沈阳', '1.0%', '1.0%', '1.0%']
# 同时在这个目录下有一个cityout.csv文件生成
```
## 练习  
**使用git合作完成**   
&emsp;&emsp;现在有两个文件，需要甲乙同学合作完成一个任务：  
&emsp;&emsp;Error data.txt是被分错的数据结果，第二列是预测类别，第三列是正确类别；  
&emsp;&emsp;test1000.txt是所有的一千条数据；  
&emsp;&emsp;首先由甲同学统计出Error data.txt中每个类错误的数量占总错误数量的百分比以及每个类错误的数量占这个类别总数量的百分比，并输出相应的两个文件；  
&emsp;&emsp;然后乙同学筛选出两个文件中百分比最多的前十五个数据，并筛选出这两组十五个数据中都有的类别；写入一个文件；  
&emsp;&emsp;甲乙再交换完成任务。  
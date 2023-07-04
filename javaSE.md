#  第一章      java语言概述

## 主要应用场景

javaEE,大数据，Android开发等







### 基础图谱

![image-20230504185146885](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230504185146885.png)







## 图形化界面操作与命令行操作

人机交互方式 ： 图形化界面 （GUI）命令行方式

## 常用命令行操作指令 和 快捷键



![image-20230504190455743](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230504190455743.png)





## 语言种类

- **第一代语言**

机器语言，指令以二进制代码形式存在

- **第二代语言**

汇编语言，使用助记符表示一条机器指令

- **第三代语言  高级语言**

C, Pascal, Fortran 面向过程的语言

C++面向过程/面向对象

Java跨平台的纯面向对象的语言

。NET跨语言的平台

python  scala...

语言排名网址：https://www.tioobe.com/tiobe-index/





## 简史节点

1991年，Green项目，开发语言最初命名为Oak（橡树）

1996年， 发布JDK1.0 ，约8.3万个网页应用java技术来制作

2004年，**发布里程碑式版本：JDK1.5 ，为突出此版本的重要性，更名为  JDK5.0**

**2014年，发布  JDK8.0,  是继  JDK5.0以来变化最大的版本**





## 语言的特点

**特点一**

​         两个基本概念：类，对象

​         三大特性：封装，继承，多态

**特点二：健壮性**

​          吸收了C/C++语言的优点，但去掉了其影响程序及健壮性的部分，提供一个相对安全的内存管理和访问机制，自动的垃圾回收机制

**特点三：跨平台性**

​            跨平台性：通过java语言编写的程序在不同的系统平台都可以运行。

​             原理：只要在需要运行的java应用程序的操作系统上，先安装一个**java虚拟机（JVM)J**即可。由JVM来负责java程序在该系统中的运行

write once run anything：一次编译，到处运行

![image-20230506154230678](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230506154230678.png)



## JVM与垃圾回收

不再使用的内存空间应回收——垃圾回收

垃圾回收在java程序运行过程中自动进行，程序员无法精确控制和干预

**java程序还会出现内存泄漏和内存溢出的问题**





## java语言的环境搭建

## JDK,JRE,JVM关系

JDK ------java开发工具包（开发工具：编译工具，打包工具）

JRE-------java运行环境 

![image-20230504205043708](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230504205043708.png) 



JDK=JRE+开发工具集     （javac.exe， java .exe，javadoc.exe）

JRE=JVM+Java SE标准类库

![image-20230504205434409](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230504205434409.png)



## 配置path环境变量的原因：

path：Windows系统执行命令时要搜寻的路径

为了在任何文件路径下，都可以执行java的开发工具（javac.exe，java.exe）

## HelloWorld

- **第一个java程序编写------伟大的helloworld**

```java
  class HelloWorld {
          public static void main(String[] args)}{
          System.out.println("Hello,World!")
      }
  }
```

**第一个Java程序的总结：**

![image-20230506154541747](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230506154541747.png)

.java程序编写-编译-运行的过程

1. ​       编写：我们将编写的java代码保存在以“.java”结尾的源文件中
   ​       编译：使用javac.exe命令编译我们的java源文件。格式：javac 源文件名.jav

   ​       运行: 使用java.exe命令解释运行我们的字节码文件。  格式：java类名

2. ​       在一个java源文件中可以声明多个class。但是只能最多有一个类声明为public的
   ​       而且要求声明为public的类名必须与源文件相同

3. ​        程序的入口是main（）方法，格式是固定的。

4. ​        输出语句：
   ​        System.out.println():先输入数据，然后换行

   ​        System.out.print():只输出数据

5. 每一行执行语句都以“；”结束

6. 编译的过程：编译以后，会生成一个或者字节码文件。字节码文件的文件名与java源文件中的类名相同

## 注释方式

**单行注释和多行注释的作用：**

​                    ①增强可读性，方便他人自己读懂自己写的代码

​                    ②调试所写的代码

#### 特点：

单行注释和多行注释，注释了的内容不参与编译，换句话说，编译以后生成的.class结尾的字节码文件中不包含注释掉的信息

**单行注释**

```java
class HelloJava {
    //单行注释：如下的main方法是程序的入口
    public static void main(String[] args){
    //单行注释；如下的语句标水输入到控制台
    System.out.println("Hello World");
    }
}
```



**多行注释 :  /*          */**

多行注释不可以嵌套使用

**文档注释 : /**         */（Java特有）**

格式：/**

​            @anthor 指定java程序的作者

​            @version 指定源文件的版本

​             */

**文档注释的使用：**

注释内容可以被JDK提供的工具Javadoc所解析，生成一套以网页文件形式体现出来的该程序的说明文档

操作方式：命令符

D：\javase\code\unite>javadoc  -d mydoc  -version HelloWorld.java

![image-20230505173241985](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230505173241985.png)





### 良好的编程风格

**正确的注释和注释风格**

使用文档注释来注释整个类或整个方法

如果注释方法中的某一个步骤，使用单行注释或者多行注释

**正确的缩进和空白**

使用一次tab操作，实现缩进

运算符两边习惯性加一个空格。比如：2+4*5

**块的风格**

javaAPI源代码选择了行尾风格

**行尾风格   次行风格**







### 常用的开发工具

<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230506160249647.png" alt="image-20230506160249647" style="zoom:50%;" /><img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230506160316589.png" alt="image-20230506160316589" style="zoom:33%;" />











# 第二章    java基本语法

## 标识符

### 关键字、保留字、标识符

**关键字 保留字**

**定义**：被Java语言赋予了特殊含义，用做专门用途的字符串                

**特点**：关键字中所有字母都为小写

具体的关键字

<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512145749269.png" alt="image-20230512145749269" style="zoom:50%;" />

保留字：

具体哪些保留字：byValue  cast  future  generic  inner  operator  outer  rest  var  goto、const

注意：自己命名标识符时要避免使用这些保留字

### 标识符的使用

**标识符**：java对于各种变量、方法和类等命名时使用的                               字符序号称为标识符

​                凡是可以自己起名字的地方都叫标识符

​      比如;类名、变量名、方法名、接口名、包名...

### 标识符的命名规则

(必须遵守)

- 由26个英文字母大小写，0-9 ，_或$组成

- 数字不可以开头 ;int 3ab = 1 ;

- 不可以使用关键字和保留字，但能包含关键字和保- 留字
- Java中严格区分大小写，长度无限制
- 标识符不能包含空格

### **3.标识符的名称命名规范** （可以不遵守）

包名：多单词组成时所有字母都小写：xxxyyyzzzz

​          eg：com.hsp.crm

类名，接口名：多单词组成时，所有单词的首字母大写;XxxYyyZzz

​           eg : TankShotGame

变量名，方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写：xxxYyyZzz

​            eg :tankShotGame

变量名：所有字母都大写，多单词时每个单词用下滑线连接：XXX_YYY_ZZZ

​             eg :TAX_RATE 

**4.注意**

​        一：在起名字时，为提高阅读性，要尽量有意义，“见名知意喽”

​        二：java采用Unicode字符集，因此字符集也可以用汉字声明，但是不建议使用



# 第三章   变量

## 变量的概念：

变量三要素

变量是程序中最基本的存储单元。

包括  变量类型、变量名和存储的值



## 变量的使用

1.java定义变量的格式，数据类型;     变量名=变量值

**说明;**

变量必须先声明后使用

变量都定义在起作用域内，在作用域内，他是有效的，换句话说，出了定义域就无效了

同一个作用域内，不可以声明两个同名的变量（不能重名）



## **变量的分类** 

对于每一种数据都定义了明确的具体数据类型，在内存中分配了不同大小的内存空间

![image-20230510143040305](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230510143040305.png)

### **一：变量按照数据类型来分**

基本数据类型：

- ​        整型：   byte（1字节=8bite） \ short（2字节） \ int （4字节） \  long（8字节）

- ​        浮点型   `float`\ double

- ​        字符型：char

- ​        布尔型:   boolean


 引用数据类型：

​         类（class）

​         接口（interface）

​         数组 （array）





### **二：变量在类中声明的位置**

成员变量VS局部变量

#### 整型变量的使用

整型类型（byte、short、int、long）

byte范围  ;  -128~127

java的整型常量默认为int型，声明 `long` 型变量需后加“L”或“l”

java程序中变量通常声明为int型，除非不足以表示较大的数，才使用long

#### 1.浮点类型：（float，double）

其有两种表示方式：十进制数形式 如：5.12  512.of

​                                    科学计数法形式 

![image-20230519111834199](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230519111834199.png)

​        java的浮点类型常量**默认为double型**，声明float型常量，须后加“f”或“F”

1. ①浮点型，表示带小数点的数值

2. ②float表示数值的范围比long还大

3. ③定义float类型变量时，变量要以“f”或“F”结尾

4. ④通常，定义浮点型变量时，使用double型

5. 尾数部分可能丢失，造成精度损失（小数都是近似值）

通常情况下，应该使用double型，因为他比float更精确

使用点：当我们对运算结果是小数的进行相等判断是，要小心  如8.1/3，用浮点类常量进行计算时，得到的是接近2.7的小数，而不是2.7

应该是以两个数的差值的绝对值，在某个精度范围类判断

#### 2.char字符型：（一字符=两字节）

![image-20230510171248408](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230510171248408.png)

①定义char型变量，**通常**使用一对'',内部只能写一个字符

②表示方式：1.声明一个字符  2.转义字符  3.直接使用Unicode 值来表示字符型常量



字符类

字符常量是用单引号（‘  ’ ）括起来的单个字符，例如：char ci = 'a';char c2 =  '中'；char c3 = ‘9’：

java中还允许使用转义字符'\\'  来将其后的字符转变为特殊字符型常量。 例如char c3 = '\n' ;  //'\n' 表示换行符

在java中，**char的本质是一个整数**，在输出时，是Unicode码对应的字符

char 的本质是一个整数，在输出时，是Unicode码对应的字符

字符和码值的对应关系是通过编码表决定的



Unicode值图表![image-20230510171622428](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230510171622428.png)



#### **4.布朗类型**

①只能取两个值之一：true,false

②常常在条件判断，循环结构中使用



## 运算符

算数运算符，赋值运算符，比较运算符，逻辑运算符，位运算符，三元运算符

运算符的优先级

上一行的运算符总优先于下一行

只有单目运算符，赋值运算符是从右向左运算的

![image-20230522083556388](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230522083556388.png)

### 算数运算符

![image-20230512161827288](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512161827288.png)

？？？？？？

![image-20230512173405091](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512173405091.png)



#### +号 和 ++号 的使用

当左右两边都是数值型时，做加法运算

当左右两边有一方为字符串，做拼接运算

++号  作为表达式使用

（前)++：先自增1，后运算

（后)++:先运算，后自 增1

#### **%号的使用**

% 取模，取余

在%的本质 看一个公式 a % b = a - a / b * b 



![image-20230512174010590](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512174010590.png)

```java
class LojicTest{
public static void main(String[] args) {
    boolean b1 = true;
    int num1 = 10;
    if (b1 & (num1++ > 0)){
        System.out.println("我现在在北京");
    }else{
        System.out.println("我现在在南京");
    }
    

    System.out.println("num1 = " + num1);
}
}

```





### 赋值运算符

`=`         +=           -=          *=        /=      %=

  当“=”两侧数据类型不一致时，可以使用自动类型转换或使用强制类型转换原则进行处理

支持连续赋值

不会改变本身的数据类型

开发中，如果希望变量实现+2的操作，有几种方法？（前提：int num = 10；）

方法一：num =  num +2

方式二：num += 2；（推荐）

##### 赋值运算符特点：

1.运算顺序从右向左 int num = a + b + c

2.赋值运算符的左边 只能是变量，右边可以是变量，表达式，常量值

int num = 20;int num2 = 78*34 -10;init num3 = a;

3.复合赋值运算符等价于下面的效果

比如 ： a += 3等价于 a= a+3

4.复合赋值运算符会进行类型转换

byte b = 2 ；b += 3；b++



<text>

`<br/>`

### 逻辑运算符

![image-20230512205147114](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512205147114.png)

逻辑运算符操作的都是Boolean类型的变量

#### **说明逻辑运算规则**

1.a&b  :  &叫逻辑与 ：规则：当a和b同时为TRUE ，则结果为true，否则为false

2.a&&b ： &&叫短路与 ： 规则  ；当a和b同时为true，则结果为true，否则为false

#### **区分& 与 &&**

相同点1： &与&&的运算结果相同

相同点2：当符号左边是true的时二者都会执行符号右边的运算

不同点：当符号左边是false时，&继续执行符号右边的运算，&&不再执行符号左边的运算

------

3.a|b : |叫逻辑或，规则： 当 a和b，有一个为true，则结果为true，否则为false

4.a||b  ：  ||叫短路或 ，规则： 当a 和b，有一个为true ，则结果为true，否则为false

#### **区分 ||  与|**

1.  || 短路或：如果第一个条件为true，则第二个条件不会判断，最终结果为true，效率高
2. | 逻辑或：不管第一个条件是否为true，第二个条件都要判断，效率低
3. 开发中，我们基本使用||



------



5. !a  : 叫取反，或者非运算。当 a为true ，则结果为false，当a为true，则结果为false，当a为false时，结果为true
6. a^b:叫逻辑异或，当a和b不同时，则结果为true否则为false

**[开发中，推荐使用&&]()**









### 比较运算符

![ ](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512213248834.png)

比较运算符的结果都是Boolean型，也就是要么是true，要么是false

比较运算符"=="不能误写成“=”

### 位运算符

![](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512214009376.png)

1.位运算符操作的都是整型的数据

2.<<  ：在一定范围内，每向左移1位，相当于*2  *

在一定范围内，每向左一位，相当于*2**



**分别是 按位与&、按位或| 、按位异或^、按位取反 ~，它们的运算规则是**

按位与&  ：  两位全为1，结果为1，否则为0

按位或|   ：  两位有一个为1，结果为1，否则为0

按位异或 ^  : 两位一个为0 ，一个为1，结果为1 ，否则为0

按位取反~ : 0—>1    1--->0

“>>”   “<<”   “>>>”三个运算符，运算规则

算数右移“>>”  ：低位溢出，符号位不变，并用符号位补溢出的高位

算数左移“<<”   ：符号位不变 ，低位补0

">>>"  ： 逻辑右移也叫无符号右移，运算规则是：低位溢出，高位补0

特别说明：没有“<<<”符号

### 三元运算符

运算规则：1.如果条件表达式为true，运算后的结果是表达式1；

​                    2.如果条件表达式为false，运算后的结果是表达式2



例题int a = 10；

​        int b= 99；

​        int result = a>b ? a++;b--;

```java
public class TernaryOperator {
    public static void main(String[] args { 
    int a = 10;
    int b = 99;
    int result = a > b ？ a++ : b--;
        System.out.println("result=" + result);//false 
        System.out.println("a=" + a);//a = 10
        System.out.println("b=" + b);//b = 99
        //所以输出结果为表达式2 =99
        
        
        
        int result = a < b ？ a++ : b--;
        System.out.println("result=" + result);//true
        System.out.println("a=" + a);//a = 10
        System.out.println("b=" + b);
       // 输出表达式为1.不用管表达式2
    }
}
```



## 键盘输入

```java
import java.util.Scanner;//表示吧java.util下的Scanner类导入
public class Input {
    //编写一个main方法
    public static void main(String[] args){
  //演示接受用户的输入
  //步骤
  //Scanner类 表示 简单文本扫描器
  //1.引入Scanner类所在的包
  //2.创建 Scanner 对象，new 创建一个对象
  //myScanner 就是Scanner类的对象
  Scanner myScanner = new Scanner(System.in);
  //3.接受用户输入了，使用 相关方法
        System.out.println("请输入名字")；
  //当程序执行到next 方法时，会等待用户的输入~
       String name = myScanner.next();//接受用户输入字符串
        System.out.println("请输入年龄");
        int age = myScanner.nextInt();//接受用户输入int
        System.out.println("请输入薪水");
        double sal = myScanner.nextDouble();//接受用户输入double
        System.out.println("人的信息如下");
        System.out.println("名字" + name + "年龄" + age + "薪水" + sal);
        
        
    }
    
}
```





## 进制

所有数字在计算机底层都以二进制形式存在

对于整数，有四种表达方式

​                二进制:0,1,满二进一，以0b或0B开头

​                十进制：0-9，满10进一

​                八进制：0-7满八进一，以数字0开头表示

​                十六进制：0-9及A-F，满十六进一，以0X或0x开头表示，此处的A-F不区分大小写，如0x21AF+1=0X21B0

#### **二进制的整数有三种形式**原码、反码、补码

1. 二进制的最高位是符号位：0表示正数，1表示负数（0--->0   ）

2. 正数的原码，反码，补码都一样（三码合一）

3. 负数的反码=它的源码符号位不变，其他位取反

4. 负数的补码= 它的反码 +1，负数的反码 = 负数的补码 - 1

5. 0的反码，补码都是0

6. java没有无符号数，换言之，java中的数都是有符号的

7. 在计算机运算的时候，都是以补码的方式来运算的

8. 当我们看运算结果的时候，要看他的原码



原码 ：直接将一个数值换成二进制，最高位是符号位

负数的反码:是对最高位取码，只是最高位（符号位）确定为1

负数的补码：其反码加1

补码可以解决正数和负数

 ![image-20230512143713395](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512143713395.png)

​                                 二进制------>十进制

计算机以二进制补码的形式保存所有的整数

正数的原码、补码、反码都相同

负数的反码是其反码+1

  









#### 进制间的转化

二进制转八进制

从低位开始，将二进制数每三位一组，转成对应的八进制数即可

二进制转换成十六进制

从低位开始，将二进制数每四位一组，转成对应的十六进制数即可









![image-20230512161233801](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230512161233801.png)

## javaAPI文档

API  （应用程序编程接口）是Java提供的基本编程接口。中文在线文档 https://www.matools.com

java 语言提供了大量的基础类

举例说明如何使用ArrayList类有哪些方法

安：包-->类-->方法

直接索引。math

char 的本质是一个整数，在输出时，是Unicode码对应的字符 



## 自动类型提升运算

基本数据类型之间的远算法则

前提：这里讨论只是七种基本数据类型变量间的运算，不包含布尔型（Boolean）

**1.自动类型提升**

当java程序在进行赋值或者运算时，精度小的类型自动转换为精度大的数据类型，这个就是自动类型转换



​         ***结论***：当容量小的数据类型的变量与容量大数据类型的变量做运算时，结果自动提升为容量大的数据类型

（此时的容量大小指的是，表示数的范围的大小，比如：float容量要大于long容量）

数据类型按照精度（容量）大小排序为（背，规则）

byte--->short---->int ---->long--->float----->double---->String

char--->int--->long--->float-->double

***特别的***;当byte，char，short三种类型的变量做运算时，结果为int型

2.**强制类型转换自动类型提升运算的逆运算**

1.需要使用强转符

2.注意点：强制类型转换，可能导致精度损失

​                 当进行数据的大小 从大 ----->小，就需要使用到强制转换

强转符号只针对于最近的操作数有效，往往会使用小括号提升优先级

```java
//int x = (int)10*3.5+6*1.5
int y =  ()
```





说明：此时的容量大小指的是，表示数的范围的大和小。比如float容量要大于long容量







## String类型变量的使用

（它不是基本数据类型，但是使用方式与基本数据类型一致）

1.String属于引用数据类型，翻译为：字符串

2.声明String类型变量时，使用一对“ ”

3.String可以和8种基本数据类型，但运算只能是连接运算：+

4.运算的结果仍然是String类型

#### 基本数据类型和String类型的转换

基本类型转String类型

语法：讲基本数据类型的值  + “”即可

String类型转基本数据类型

语法：通过基本类型的包装类调用parseXX方法即可



# 第四章  控制结构

## 顺序

### 三大流程控制语句

- 顺序控制    程序从上到下逐行执行，中间没有任何判断和跳转

  ​                    java中定义变量时采用合法的向前引用

  `public class Test{` 

  ​         int num1 = 12;

  ​         int num2 = num1 + 2;

   }`

- #### 分支控制

  - if- else 让程序有选择的执行，分支控制有三种

    - ##### 单分支 基本语法  if（条件表达式）{

      执行代码块；（可以有多条语句.）

      } 

      说明：当条件表达式为true时，就会执行{}的代码块，如果为false，就不执行

      ​           如果{}中只有一条语句，则可以不用{}，但是建议写上 

      ```java
      import java.util.Scanner;//很重要，导入一个类
      //编写一个main方法
      public class pratice004 {
          public static void main(String[] args){
              //思路分析1.把输入的年龄应该定义一个Scanner对象
              //2.把年龄保存到一个变量Scanner 对象
              //3.使用if判断，输出对应信息
              
            Scanner myScanner = new Scanner(System.in);
            System.out.println("请输入年龄");
            int age = myScanner.nextInt();
            if(age > 18) {
                System.out.println("你年龄大于18，要对自己的行为负责，送入监狱");
            }
             System.out.println("程序继续...");
          }
      }
      
      ```

      <img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230523174514867.png" alt="image-20230523174514867" style="zoom: 25%;" />

    - 双分支  基本语法  if (条件表达式){

      ​            执行代码块1;

      }

      else {

      ​            执行代码块2;

      }

      说明 ：当条件表达式成立时，及执行代码块1，否则执行代码块2 

      ​              如果执行代码块 ，只有一条语句，则{}可以省略，否则，不能省略

      ```java
      import java.util.Scanner;
      public class pratice004 {
          public static void main(String[] args) {
              Scanner myScanner = new Scanner(System.in);
              System.out.print("请输入你的年龄: ");
              int age = myScanner.nextInt();
              if (age > 18) {
                  System.out.println("你年龄大于18，要对自己的行为负责，送入监狱");
              } else {
                  System.out.println("你的年龄不大这次放过你了");
              }
              System.out.println("程序继续");
          }
      
      ```

      

      ```java
      public class pratice004 {
          public static void main(String[] args) {
              double d1 = 34.5;
              double d2 = 2.6;
              if(d1 > 10.0 && d2 < 20.0) {
                  System.out.println("两个数和为" + (d1 + d2));
              }
                 int num1 = 10;
                 int num2 = 5;
                 int sum = num1 + num2;
                 if(sum % 3 == 0 && sum % 5 == 0){
                      System.out.println("和可以被3又能被5整除");
                 }else{
                  System.out.println("和不能被3和5整除");
              }
          }
      }
      
      ```

      

    

    

    

    

    

    

    - 多分支  基本语法                    

       if (条件表达式1) { 

      执行代码块1； 

      }

      else if （条件表达式2）{ 

      执行代码块2；

      }

      ....

      else{

         执行代码块n；

      }

      特别说明：（1）多分支可以没有else，如果所有的条件表达式不成立，则一个人执行入口都没有

      ​                   （2）如果有else，如果所有的条件表达式都不成立，则默认执行else代码块

<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230523213032045.png" alt="image-20230523213032045" style="zoom:50%;" /> <img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230523213131184.png" alt="image-20230523213131184" style="zoom: 33%;" />













- 循环控制

### 分支 

####  嵌套分支

​           在一个分支结构中又完整的嵌套了另一个完整的分支结构，里面的分支结构称之为内层分支

​                   外面的分支称为结构称为外层分支。（不要超过三层，因为可读性不好）

基本语法

 ```java
       if（） {
 
 ​               if（）{
 
 ​               // if-else...
 
 }else {
 
               //if- else 
 
 }
 
 }
 ```



 

#### switch分支

1.Switch 关键字，表示switch 分支

2.表达式 对应一个值

3.case常量1 ：当表达式的值等于常量1，就执行 语块1

4.break;表示退出Switch

5.如果和case 常量1匹配，就执行语块1，如果没有匹配，就继续匹配case常量2

6.如果一个都没有匹配上，执行default

<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230524163615997.png" alt="image-20230524163615997" style="zoom:33%;" />  <img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230524170151536.png" alt="image-20230524170151536" style="zoom:33%;" />

```java
 import java.util.Scanner;
public class Switch01 {
public static void main(String[] args){
    Scanner myScanner = new Scanner(System.in);
    System.out.println("请输入一个字符（a-g）");
    char c1 = myScanner.next().charAt(0);
    switch(c1) {
        case 'a' :
           System.out.println("今天星期一");
           break;
        case 'b' :
            System.out.println("今天星期二");
            break;
        case 'c' :
            System.out.println("今天星期三");
            break;
        case 'd' :
            System.out.println("今天星期四");
            break;
        case 'e' :
            System.out.println("今天星期五");
            break;
        case 'f' :
            System.out.println("今天星期六");
            break;
        case 'g' :
            System.out.println("今天星期七");
            break;
        default:
            System.out.println("你输入的字符不正确，没有匹配的字母");
    }
System.out.println("退出了Switch，继续执行程序");
}
}

```

##### switch 注意事项和细节讨论

1.表达式数据类型，应和case后的常量类型一致，或者是可以自动转成可以转成可以相互比较的类型，比如输入的是字符，而常量是int

2.Switch中的表达式的返回值必须是：（byte、short、int、char、enum、String）

3.case 子句中的值必须是常量（1，“a”）或者是常量表达式，而不能是变量

4.default子句是可选的，当没有匹配的case时，执行default

   如果没有default子句，有没有匹配任何常量，则没有输出

5.break语句用来在执行完一个case分支后使程序跳出Switch语句块；如果没有写break，程序会顺序执行到Switch结尾，除非执行到break

##### switch和if的比较

1.如果判断的具体数值不多，而且符合byte、short、int、char、enum【枚举】、String 这六种类型，虽然两个语句都可以使用，建议使用Switch语句。

2.其他情况：对区间判断，对结果为Boolean类型判断，使用if，if的适用范围更广泛



## 循环

#### for循环控制

基本语法：

for（循环变量初始化;循环条件；循环变量迭代）{                               

​           循环操作（可以多条语句）；

}

说明：1.for关键字，表示循环控制

#####             2.for循环有四要素

（1）循环变量初始化

  (2）循环条件

（3）循环操作

（4）循环变量迭代

​            3.循环操作，这里可以有多条语句，也就是我们要循环执行的代码

​              4.如果  循环操作（语句）只有一条语句，可以省略{}，但是建议不要省略

![image-20230524204238909](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230524204238909.png)

注意事项和细节说明

- 循环条件是返回一个布尔值的表达式
- for （：循环判断条件）中的初始化和变量迭代可以下到其他地方，但是两边的分号不能省略
- 循环初始值可以有多条初始化语句，但要求类型一样，并且中间用逗号隔开

```java
 }public class forreturn2 {
        //完成 输出 1-100的值
        //在输出过程中，进行过滤，只输出9的倍数
        //统计个数 定义一个变量 int count = 0；当条件满足时 count++；
        //总和，定义一个变量 int sum = 0;当条件满足时 sum += i；
        //先死后活
        //(1)为了适应更好的需求，把范围的开始的值和结束的值，做出变量
        //(2)还可以更进一步9倍数也做成变量 int t = 9；

        public static void main(String[] args) {
            int count = 0; //统计9的倍数个数 变量
            int sum = 0;//总和
            for (int i = 1; i <= 100; i++) {
                if (i % 9 == 0) {
                    System.out.println("i=" + i);
                    count++;
                    sum += i;//积累
                }

            }
```



#### while 循环控制

基本语法

循环变量初始化；

```java
while(循环条件){

​        循环体（语句）；

​         循环变量迭代；

}
```





<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230525174334099.png" alt="image-20230525174334099" style="zoom:33%;" />

- 说明

  （1）while循环也有四要素

  （2）只要是四要素放的位置，不一样。
  
  ```java
  public class While02 {
      public static void main(String[] args){
          int i = 1;
          int endNum = 100;
          while( i <= endNum){
              if( i % 3 == 0){
                  System.out.println("i=" + i);
              }
              i++;
          }
          System.out.println("======");
          int j = 40;//变化初化
          while(j <= 200 ){
              //判断
              if( j % 2 == 0){
                  System.out.println("j=" + j);
              }
              j++;//循环变量的迭代
          }
      }
  }
  
  ```





#### do-while 循环

基本语法

循环变量初始化；

```java
do{

​          循环体（语句）；

​          循环变量迭代；

}while（循环条件）；
```



- 说明

  1.do while 是关键字

  2.也有循环四要素；只是位置不一样

  3.先执行，再判断，也就是说，一定会执行一次

  4..最后有一个分号

  5while 和 do..while 

  ![image-20230525202519358](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230525202519358.png)

  ```java
  public class DoWhile01 {
     //编写一个main方法
      public static void main(String[] args) {
          //输出10句sunflower
          int i = 1;//循环变量初始化
          do {
              //循环执行语句
              System.out.println("Sunflower");
              //循环变量迭代
              i++;
          } while (i <= 10);
          System.out.println("退}出 do..while 继续执行.." + i);
  
      }
  
  
  ```

注意事项和细节说明

（1）循环条件是返回一个布尔值的表达水

（2）do..while循环是先执行，再判断，因此它至少执行一次



#### 多重循环

1.将一个循环体放在另一个循环体内，就形成了嵌套循环，其中，for，while，do...while均可以作为外层循环和内层循环【建议一般使用两层，最多不要超过3层，否则，代码的可读性很差】

2.实质上，嵌套循环就是把内层循环当成外层循环的循环体，当只有内层循环的循环条件为false时，才会完全跳出内层循环，才可结束外层的当次循环，开始下一次的循环

```java 
//双层for
for(int i = 0;i < 2; j++){
System.out.println("i=" + i + "j=" + j);
}
}
```

i = ?   j = ？

#### ###多重循环控制老重要了！

经典的打印金字塔

使用for 循环完成下面的案例

接受一个整数，表示层数，打印金字塔（Stars.java）[ 化繁为简，先死后活]

（1.）完成思路，可以先从矩形开始打

（2.）代码实现

（3.）再用while来实现一把

## break

跳转控制语句

break语句用于终止某个语句块的执行，一般使用在Switch或者循环{ for、while、do-while}中

基本语法；

{.......

break；

.......

}

![image-20230526173026420](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230526173026420.png)

![image-20230527100945092](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230527100945092.png)





注意事项和细节说明：

1.break 语句出现在多层嵌套的语句块中时i，可以通过标签指明要终止的是哪一层的语句块 BreakDetail.java

2.标签的基本使用

  label1.{.............

label2.          {.................

label3.                   {.....................

​                                                  break label2；

​                                                  .................

​                                      }

​                              }

​                      }    

(1.)break 语句可以指定退出那层

- label1 是标签，由程序员指定  

- break后指定到那个label 就退出到那里

- 在实际的开发中，尽量不要使用标签

- 如果没有指定break，默认退出最近的循环体

```java  
import java.util.Scanner;
public class BreakWhile03 {
    //创建一个Scanner，接受用户输入
    //定义一个String name;String passwd;保存用户名和密码
    //最多循环三次，如果满足条件就提前退出
    //定义一般变量int chance  记录还有几次登陆机会
    //代码实现
    public static void main(String[] args){
        Scanner myScanner = new Scanner(System.in);//创建一个Scanner，用于接受用户输入
        String name = "";//定义一个名字
        String passwd = "";//定义一个密码：用于保存用户名和密码
        int chance = 3;//三次机会，登陆一次就少一次机会
        for (int i = 1;i <= 3;i++){
            System.out.println("请输入名字");
            name = myScanner.next();
            System.out.println("请输入密码");
            passwd = myScanner.next();
            //比较输入的名字和密码是否正确
            //补充说明字符串的内容 比较使用的方法equals
            if("丁真".equals(name) &&  "666".equals(passwd)) {
                System.out.println("恭喜你，登陆成功~~~");
            }//登陆的机会就少一次
            chance--;
            System.out.println("你还有" + chance + "次登陆机会");
            }

        }
    }
```



## continue

1. continue语句用于结束本次循环，继续执行下一次循环

2. continue语句出现在多层嵌套的循环语句体中时，可以通过**标签**指明要跳过的是那一层循环，这个和前面的**标签的使用规则一样**

3. 基本语法

```java
{
    //....

	continue；

	//...........

}
```



4. 以while使用continue为例子，示意图如下

   ![image-20230527163722965](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230527163722965.png)





continue break



```java
public class Continue01 {
    //编写一个main方法
    public static void main(String[] args){
    //代码
    int i = 1;
    while (i <= 4){
        i++;
        if (i == 2){
            continue;
        }
        System.out.println("i=" + i);
    }

    }
}
```



![image-20230527164556066](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230527164556066.png)

 ![image-20230527172545122](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230527172545122.png)



## return

return 使用在方法，表示跳出所在方法,并 返回 (携带) 所需要的值

1. `return;`
2. `return 11;`

如果return写在main方法，退出程序..



# 第五章  数组

## 数组array

### 数组的定义

数组可以存放多个同一类型的数据，数组也是一种数据类型，**是引用类型**

即：数组就是一组数据

double[  ] a = {n1,n2,n3,n4}

double[ ] 表示，是double类型的数组

{n1,n2,n3,n4}表示数组的值/元素

遍历数组得到数组的所有元素的和,使用for

1. .通过hens[下标] 来访问数组的元素

​	    下标是从开始编号的比如第一个元素是hens[ 0 ]

​	     第二个元素就是hens[0]   ,依次类推。

2.通过for就可以循环的访问，数组的元素/值

3.使用一个变量 totalweight 将各个元素累计

可以通过 数组名.length 得到数组的大小/长度

### 数组的使用

#### 使用方式

##### 方式1--动态初始化①

​           数组的定义

​             数据类型 数组名[ ]= new 数据类型[大小]

int a[ ]= new int[5];//创建了一个数组，名字为a，存放5个int  

##### 方式2--动态初始化②

先声明数组              

语法：数据类型 数组名[]；也可以 数据类型[]                                               数组名

​              int a [];或者int[] a

创建数组

语法：数组名 = new数据类型[大小]；

a = new int[10];





##### 方式3--静态初始化（知道有几个数组元素，且数组元素是有限的）



语法：数据类型 数组名 [] = {元素值，元素值...}

int a []={2,5,6,7,8,89,90,34,56} 如果知道数组有多少远元素，具体值上面的用法想当于；int a []= new int [9]

a[0]= 2   a[1]=5......



#### 数组使用注意事项和细节

- 数值是多个相同类型数据的组合，实现对这些数据的统一管理

- 数组中的元素可以是任何数据类型，包括基本类型和引用类型，但是不能混用

- 数组创建后，如果没有赋值，有默认值 

  默认为0

  int0，short0，byte0，long0，float0.0，double0.0，char\u0000. boolean false ,String null （null 无效的，空的）

- 使用数组的步骤

  - 声明数组并开辟空间
  - 给数组各个元素赋值
  - 使用数组

- 数组的下标是从0开始的

- 数组下标必须在指定范围内使用，否则报：下标越界异常，比如int [] arr = new int[5];则有效下标为0-4

  即数组的下标/索引 最小0，最大数组长度 -1

- 数据属于引用类型，数据型数据是对象（object）

### *数据赋值机制（特别重要！！！）

1.基本数据类型赋值，这个值就是具体的数据，而且互不影响

int n1 = 2；int n2 = n1；

2.数组在默认情况下是引用传递，赋的值是地址

```java 
int[] arr1 = {1,2,3};
int[] arr2 = arr1;
```



在内存里面只要分配了一个数据空间那么这个数据空间一定对应一个地址

<img src="C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230601172820333.png" alt="image-20230601172820333" style="zoom:50%;" />

就相当于 两个管理员 管理一个仓库，物品进进出出都会随着一个人的调动而改变

共享仓库哈哈哈

#### 数组拷贝

![image-20230601175646252](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230601175646252.png)

```java 
public class ArrayCopy {
    public static void main(String[] args){
        int[] arr1 = {10,20,30,40};
        int[] arr2 = new int[arr1.length];
        for(int i = 0;i < arr1.length; i++){//遍历arr1，把每个元素都拷贝到arr2中
            arr2[i] = arr1[i]
        }
arr2[0] = 100;
        System.out.println("====arr1的元素====");
        for(int i = 0; i < arr.length; i++){
            System.out.println(arr1[i]);
        }
    System.out.println("====arr2的元素====");
        for(int i = 0; i < arr2.length; i++) {
            System.out.println(arr2[i]);
        }
    }
}

```



#### 数组反转 

```java
public class ArrayInversion02 {
    public static void main(String[] args){
       //定义数组
        int[] arr = {11,22,33,44,55,66};
        //逆序赋值方式
        /*
        思路1.先创建一个新的数组arr2 ，大小 arr.length
           2.逆序遍历arr ，将每个元素都拷贝到arr2 中（顺序拷贝）
           3.增加一个循环变量 j --> 0 --> 5;
         */
        int[] arr2 = new int[arr.length];
        //逆序遍历arr
        for(int i = arr.length - 1, j = 0; i >= 0;i--,j++){
            arr2[j] = arr[i];
        }//当for 循环结束，arr2 就是一个逆序的数组{66,55,44,33,22,11}
        // 让arr指向 arr2 数据空间，此时arr 原来的数据空间就没有变量引用，会被jvm当成垃圾，销毁
        arr = arr2;
        System.out.println("====arr的元素情况====");
        //输出arr看看
        for(int i = 0; i < arr.length; i++){
            System.out.println(arr[i] + "\t");
        }
    }
}
```

#### 数组添加（扩容）

  要求：实现动态的给数组添加元素效果，实现对数组扩容

![image-20230602110554373](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230602110554373.png)







## 排序

排序是将一群数据，依照指定的顺序进行排列的过程

#### 排序的分类

1.内部排序

指定需要处理的所有数据都加载到内部存储器中进行排序。包括（交换式排序法，选择式排序法和插入式排序法）

2.外部排序法

数据量过大，无法全部加载到内存中，需要借助外部存储进行排序。包括（合并排序法和直接合并排序法）

#### 冒泡排序

冒泡排序的基本思想是：通过对待排序序列从后往前（从下标较大的元素开始），依次比较相邻元素的值，若发现逆序则交换，使值较大的元素逐渐从前移向后部，就像水底下的气泡一样逐渐向上冒 



temp（temporary）临时变量

```java 
int a = 5;
int b = 10;

// 使用临时变量交换a和b的值
int temp = a;
a = b;
b = temp;

System.out.println("a = " + a); // 输出：a = 10
System.out.println("b = " + b); // 输出：b = 5
```



## 查找

顺序查找 二分查找

## 多维数组

多维数组----二维数组

#### ***jvm的内存 二维数组的内存形式（很重要）

![image-20230603110943224](C:\Users\20612\AppData\Roaming\Typora\typora-user-images\image-20230603110943224.png)

#### 二维数组的使用

##### 使用方式1 ；动态初始化

语法：类型[][][][] [][][] []数组名 = new 类型[大小] [大小]

​         eg：`int a [][] = nw int[2][3]`

我怎么感觉有点像是在赋值

​     表示有两个一维数组 ，每个一维数组中有三个元素



##### 使用方式2 ：动态初始化

先声明   ：类型 数组名[] [] 

在定义（开辟空间）数组名 = new 类型[大小] [大小]

赋值（有默认值，比如int 类型就是0）

##### 使用方式3： 动态初始化--列数不确定 

先确定二维数组里有几个一维数组，int [][] [3] []不开空间的话，里面的值null

```java
public class TwoDArray03 {
    public static void main(String[] args) {
        int[][] arr = new int[10
                ][];//创建 二维数组，但是只是确定了一维数组的个数
        for (int i = 0; i < arr.length; i++) {//遍历arr每个一维数组
            //给每个一维数组开空间，开空间即为new
            //如果没有给一维数组new ，那么arr[i] 就是null 空的
            arr[i] = new int[i + 1];
            //遍历一维数组，并给一维数组的每个元素赋值
            for (int j = 0; j < arr[i].length; j++) {
                arr[i][j] = i + 1;//赋值
            }
        }
        System.out.println("========arr元素=========");
        //遍历arr输出
        for (int i = 0; i < arr.length; i++) {
            //输出arr的每个一维数组
            for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();//换
        }
    }
}
```



 

##### 使用方式4 ：静态初始化

1.定义 类型 数组名[] [] = {{值1，值2...}{值1，值2...} {值1，值2...}}

2.使用即可 [固定方式访问]

eg：int [] [] arr = {{1,1,1},{2,2,2},{100}};

解读 1.定义了一个二维数组arr

​         2.arr有三个元素（每个一位数组都是一维数组）

​         3.第一个一维数组有3个元素，第二个一维数组有3个元素，第三个一维数数组有一个元素





#### 二维数组的遍历

#### 二维数组的使用细节和注意事项

- 一维数组的声明方式有：int[] x 或者 int y[] []

- 二维数组的声明方式有：int[] [] y 或者 int[]y[] 或者 int y[] []

- 二维数组实际上是由多个一维数组组成的，它的各个一维数组的长度可以相同，也可以不相同。比如： map[] [] 是一个二维数组

  int map [] [] = {{1,2} {3,4,5}}

  由map [0]是一个含有两个元素的一维数组，map[1]是一个含有三个元素的一维数组构成，我们也称之为列数不等的二维数组

## 作业 

#### 作业 1写出结果 

```java
String foo = "blue";//foo 就是一个变量名

boolean[] bar = new boolean[2];

if(bar[0]){

foo = "grean";

} 

System.out.println(foo);


```

*解* ： bar[0] 默认false

​           bar[1] false所以foo不会进入到 if 语句中

直接输出foo 就是变量值blue

 insert 插入

index 指数 

### ！！1（还不会！）作业 2

已知有个升序的数组，要求插入一个元素，该数组顺序依然是升序，比如：

{10,12,45,90}，添加23后，数组为{10,，12，23,45,90}





# 第六章 面向对象编程

## 类与对象（OOP）

 ![image-20230703105012153](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230703105012153.png)

```java
public class objectCat {
    public static void main(String[] args) {//编写一个main方法
        class Cat {
            String name;//属性，成员变量，字段field
            int age;
            String color;
        }
        Cat cat1 = new Cat();
        cat1.name = "小白";
        cat1.age = 3;
        cat1.color = "白色";
        Cat cat2 = new Cat();
        cat2.name = "小花";
        cat2.age = 100;
        cat2.color = "花色";
        System.out.println("第一只猫的信息" + cat1.name + " " + cat1.age + " " + cat1.color);
        System.out.println("第二只猫的信息" + cat2.name + " " + cat2.age + " " + cat2.color);

    }
}
```





new啥玩意就是创建一个

### 对象

#### 对象在内存中存在的形式（重要的！）

   ![image-20230703142924161](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230703142924161.png)

真正的对象是 堆 里的.

Cat只是 对象引用     Cat只是指向对象

#### 如何创建对象

1.先声明再创建

Cat  cat ；//声明对象Cat

Cat = new Cat（） ；//创建

2.直接创建

Cat cat = new Cat（）；



### 属性/成员变量

1.从概念或叫法上来看：成员变量 = 属性 = field (字段)  ；

Car（ name age color ）

2.属性是类的一个组成部分，一般是基本数据类型，也可以是引用类型（对象，数组）。

比如 定义猫类的 int age 就是属性

```java
String name;//属性
duoble price;
String color;
String[] master;//属性可以是基本数据类型，也可以是引用类型（对象，数组）
```

##### 属性的注意事项 和 细节说明

- 属性的定义语法同变量，示例：访问修饰符 属性类型 属性名；

  （访问修饰符： 控制属性的访问范围,,,,,,,,有四种访问修饰符，public,procttected,默认,private）

- 属性的定义类型可以为任意类型，包含基本类型或引用类型

- 属性如果不赋值，有默认值，规则和数组一致。

数组创建后，如果没有赋值，有默认值 

默认为0

int0，short0，byte0，long0，float0.0，double0.0，char\u0000. boolean false ,String null （null 无效的，空的）



### 类和对象的内存分配机制（重要！）

#### Java内存的结构分析

- 栈：一般存放基本数据类型(局部变量)
- 堆：存 放对象
- 方法区：常量池（常量，比如字符串）类加载信息
- 示意图[Cat (name age color)]

#### Java创建对象的流程简单分析

```java
Person p = new Person();
p.name = "jack";
p.age = 10;
```

![image-20230703151718170](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230703151718170.png)

1.先加载person类信息（属性和方法信息，只会加载一次）

2.在堆中分配空间，进行默认初始化（看规则 如 0  null等）

3.把地址赋给p，p就指向对象

4.进行指定初始化，比如`p.name  = "jack "   p.age = 10 `

分析画出内存布局图（题目如下）

![](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230703154304526.png)

<img src="C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230703154217250.png" alt="image-20230703154217250" style="zoom: 25%;" />

 





## 成员方法

在某些情况下我们需要定义成员方法

#### 定义

`public` 返回数据类型 方法名（形参列表..）{//方法体语句}；

`return `返回值；

}

- 参数列表：表示成员方法输入cal (int n )
- 数据类型（返回类型） ：表示成员方法输出，void 表示没有返回值
- 方法主体，表示为了实现某一功能代码块
- return 语句不是必须的
- 要根据前面的题的示意图，来理解

#### 入门

1.添加speak 成员方法 ，输出我是好人

- 添加Speak 成员方法，输出“我是一个好人”

- 添加cal01成员方法，可以计算从 1+ ... + 1000 的结果
- 添加cal02成员方法，该方法可以接收一个数n，计算从1 + ..+n的结果
- 添加getSum成员方法，可以计算两个数的和

#### 方法调用机制

方法调用小结

1.当程序执行到方法时，就会开辟一个独立的空间（栈空间）

2.当方法执行完毕，或者执行到return语句时，就会返回

3.返回到调用方法的地方

4.返回后，继续执行方法后面的代码

5.当主方法`main`方法栈 执行完毕，整个程序退出



#### 成员方法的好处

- 提高代码的复用性

- 可以将实现的细节封装起来，然后供其他用户来调用即可

#### 注意事项和使用细节

访问修饰符

作用：控制 方法使用的范围如果不写就是默认访问（`public` `protected` 默认 `private`）

##### 返回数据类型

- 一个方法最多有一个返回值
- 返回类型可以为任意类型，包含基本类型或者引用类型（数组，对象）

- 如果方法要求有返回数据类型，则方法体中最后的执行语句必须是return 语句，或者只写return，且要求返回值类型 必须和 return 的值 类型一致或兼容
- 如果方法是`void` ，则方法体中可以没有return语句，或者只写 return；
- 方法名 ，遵循驼峰命名法，最好见名知意，表达出该功能的意思即可，比如得到两个数的和getSum ，开发中按照规范

##### 形参列表

- 一个方法可以有0个参数，也可以有多个参数，中间用逗号隔开

​      eg`getSum(int n1,int n2)`

- 参数类型可以为任意类型，包含基本类型或引用类型eg `printArr(int[][] map`)

- 调用带参数的方法时，一定对应着参数列表传入相同类型或兼容类型的参数 eg`getSum`

  比如低精度可以到高精度  ，但是高精度不能到低精度 ，因为会导致精度损失 或者数据溢出等问题

- 方法定义的参数称为形式参数，简称形参；方法调用时的参数称之为实际参数，简称实参，实参和形参的类型要一致或兼容，个数，顺序必须一致！

  方法体

  里面写完成功能的具体的语句，可以为输入，输出，变量，运算，分支，循环，方法调用，但里面不能再定义方法

  即方法不能嵌套定义



##### 方法调用细节说明

- 同一个类中的方法调用，直接调用
- 跨类中的方法A类调用B类的方法：需要通过对象名调用。比如 对象名，方法名（参数）
- 特别说明，跨类的方法调用和方法的访问修饰符相关







一旦调用方法就会出现新的栈

两个独立的空间，里面的相同变量或其他并不冲突



## 成员方法传参机制

### 基本数据类型的传参机制

![image-20230704154947134](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704154947134.png)

![image-20230704154852116](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704154852116.png) 

### 引用数据类型的传参机制

只要调用方法就会产生一个新的栈

如果有数组，栈中的数组指向堆，重新再开地址

### 



**题目**B类中编写一个方法 test100，可以接收一个数组，在方法中修改该数组，看看原来的数组怎么变化



**题目**B类中编写一个方法test200，可以接收一个Person（age，sal）对象，在方法中修改对象的属性，看看原来的对象是否变化

主方法中的p和class中的p 不是一回事，是独立的空间

![image-20230704165015389](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704165015389.png)

**结论**：引用类型传递的是地址（传递也是值，但是值也是地址），可以通过形参影响实参

（引用传递传的是地址）

Pratice：

![image-20230704194521444](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704194521444.png)



![image-20230704195003362](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704195003362.png)

## overload

## 可变参数

## 作用域

## 构造器

## this




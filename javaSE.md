# 第一章      java语言概述

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

2.数组在默认情况下是**引用传递**，赋的**值是地址**

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





# 第六章 面向对象编程（基础）

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

在某些情况下我们需要定义成员方法，让我们的类有一些行为，没可以做一些事情

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

![image-20230710104637202](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230710104637202.png)

方法调用小结

1.当程序执行到方法时，就会开辟一个独立的空间（栈空间）

2.当方法执行完毕，或者执行到return语句时，就会返回

3.返回到调用方法的地方

4.返回后，继续执行方法后面的代码

5.当主方法`main`方法栈 执行完毕，整个程序退出



#### 成员方法的好处

- 提高代码的**复用性**

- 可以将实现的细节封装起来，然后供其他用户来调用即可

#### 注意事项和使用细节

访问修饰符

作用：控制 方法使用的范围

如果不写就是默认访问（`public` `protected` 默认 `private`）

##### 返回数据类型

- 一个方法最多有一个返回值
- 返回类型可以为任意类型，包含基本类型或者引用类型（数组，对象）

- 如果方法要求有返回数据类型，则方法体中最后的执行语句必须是return 语句，或者只写return，且要求返回值类型 必须和 return 的值 类型一致或兼容
- 如果方法是`void` ，则方法体中可以没有return语句，或者只写 return；
- 方法名 ，遵循驼峰命名法，最好见名知意，表达出该功能的意思即可，比如得到两个数的和getSum ，开发中按照规范

#####      形参列表

- 一个方法可以有0个参数，也可以有多个参数，中间用逗号隔开

​      eg`getSum(int n1,int n2)`

- 参数类型可以为任意类型，包含基本类型或引用类型eg `printArr(int[][] map`)

- 调用带参数的方法时，一定对应着参数列表传入相同类型或兼容类型的参数 eg`getSum`

  比如低精度可以到高精度  ，但是高精度不能到低精度 ，因为会导致精度损失 或者数据溢出等问题

- 方法定义的参数称为形式参数，简称形参；方法调用时的参数称之为实际参数，简称实参，实参和形参的类型要一致或兼容，个数，顺序必须一致！

  **方法体**

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

都是独立的

### 引用数据类型的传参机制

**只要调用方法就会产生一个新的栈**

**如果有数组，栈中的数组指向堆，重新再开地址**

### 



**题目**B类中编写一个方法 test100，可以接收一个数组，在方法中修改该数组，看看原来的数组怎么变化

![image-20230710105126594](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230710105126594.png)

**题目**B类中编写一个方法test200，可以接收一个Person（age，sal）对象，在方法中修改对象的属性，看看原来的对象是否变化

主方法中的p和class中的p 不是一回事，是独立的空间

![image-20230704165015389](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704165015389.png)

**结论**：引用类型传递的是地址（传递也是值，但是值也是地址），可以通过形参影响实参

（引用传递传的是地址）

Pratice：

![image-20230704194521444](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704194521444.png)



![image-20230704195003362](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230704195003362.png)



### 方法逆归调用

逆归就是方法自己调用自己，每次调用时传入不同的变量，逆归有助于解决复杂的问题，使代码更简洁；

#### 打印和阶乘问题

- 打印问题：

```java
public class recursion01 
        public static void main(String[] args){
  T t1 = new T();
  t1.test(4);
    }//问题：输出什么？
}
class T{
    public void test(int n){
        if(n > 2){
            test(n - 1);
        }
    System.out.println("n=" + n);
    }
}
```

jvm的内存

方法的逆归调用分析图：

![image-20230705101709947](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230705101709947.png)

- 阶乘问题

  ```java
  public class recursion02 {
      public static void main(String[] args){
      S s1 = new S();
       int res = s1.factorial(5) ;
       System.out.println("输出的结果是=" + res);
      }
  }
  class S{
      public int factorial(int n){
          if(n == 1){
              return 1;
          } else {
              return factorial(n-1) * n;
          }
      }
  }
  ```

![](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230705105117000.png)



#### 逆归重要的规则

- 执行一个方法时，就创建一个新的受保护的独立空间（栈空间）
- 方法的局部变量是独立的，不会相互影响，比如n变量
- 如果方法中使用的是引用类型变量（比如数组），就会共享该引用类型的数据
- 逆归必须向退出逆归的条件逼近，否则就是无限逆归，出现StackOverflowError 反正就是死了
- 当一个方法执行完毕，或者遇到return，就会返回，遵守谁调用，就将结果返回给谁，同时当方法执行完毕或者返回时，该方法也就执行完毕了



#### 逆归方法练习（有意思滴！）

##### 斐波那契数 

```java
package com.byyj.ObjectOriented.ClassFollow.recursion;
//使用递归的方式求出斐波那契数1,2,3,5,8,13,21，，，给你一个整数n，求出它的值是多少
public class recursion03fibonacci {
    public static void main(String[] args){
 	 B b1 = new B();
        int n = 8;
        int res = b1.fibonacci(n);
        if (res != -1) {
  System.out.println("当n = 25时，对应的斐波那契数=" + b1.fibonacci(25) );
    }
}
}
    class B {
        //思路分析
        //1.当n =  1 斐波那契数列= 1
        //2.当n =  2 斐波那契数列= 1
        //3.当n >= 3 斐波那契数列= 前两数之和
    /*
    方法返回类型 int
    方法名字 fibonacci
    方法形参 int n
    方法体 创建一个新对象，输入n数字，根据题意条件返回一个值
     */
        public int fibonacci(int n) {
            if (n >= 1) {
                if (n == 1 || n == 2) {
                    return 1;
                } else {
                    return fibonacci(n - 1) + fibonacci(n - 2);

                }
            } else {
                System.out.println("要求输入的数字式大于等于1的，该输入有误的");
            }
            return n;
        }
    }
```



##### 猴子吃桃子喽

猴子吃桃子问题 : 有一堆桃子，猴子第一天吃了其中的一半，并再多吃了一个!以后每天猴子都吃其中的一半，然后再多吃一个。当到第10天时,想再吃时 (即还没吃) ，发现只有1个桃子了。问题 : 最初共多少个桃子 ?

```java
package com.byyj.ObjectOriented.ClassFollow.recursion;

public class recursion04MonkeyPeach {
    public static void main(String[] args){
       D d1 = new D();
       int day = 2;
       int peachNum = d1.peach(day);
       if( peachNum != -1);
    System.out.println("第" + day + "天有" + peachNum + "个桃子");
    }
}
class D{
     /*
     思路分析：
     1.第10天，桃子= 1
     2.第9 天，桃子= (day10 + 1) * 2 = 4;
     3.第8 天，桃子= (day9  + 1) * 2 = 10;

    方法返回类型 int
    方法名字 peach
    方法形参 int day
    方法体 创建一个新对象，输入n数字，根据题意条件返回一个值
     */
    public int peach(int day){
        if( day == 10){
            return 1;
        }else if( day >= 1 && day <= 9){
            return (peach(day+1) + 1 ) * 2;
        }else{
            System.out.println("day在1-10中才是有效的");
            return -1;
        }
    }
```



### 迷宫问题

![image-20230705192236035](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230705192236035.png)

```java
package com.byyj.ObjectOriented.ClassFollow.recursion;

public class MiGong {
    public static void main(String[] args) {
        int[][] map = new int[8][7];//创建一个8行7列的二维数组 ，表示迷宫地图
        for (int i = 0; i < 7; i++) {//设置迷宫地图的边界
            map[0][i] = 1;
            map[7][i] = 1;
        }
        for (int i = 0; i < 8; i++) {
            map[i][0] = 1;
            map[i][6] = 1;
            map[3][1] = 1;
            map[3][2] = 1;
        }
        System.out.println("=====输出当前地图的情况======");
        for (int i = 0; i < map.length; i++) {
            for (int j = 0; j < map[i].length; j++) {
                System.out.print(map[i][j] + " ");
            }
            System.out.println();
        }

        C c1 = new C();//创建一个C类的 实例，，，c1对
        c1.findway(map, 1, 1);//调用C类的findWay方法来找路
        System.out.println("====找路的情况如下=====");
        for (int i = 0; i < map.length; i++) {
            for (int j = 0; j < map[i].length; j++) {
                System.out.print(map[i][j] + " ");
            }
            System.out.println();
        }
    }
    }
    class C {
    /*1.findway 方法就是专门来找迷宫的路径
      2.如果找到就返回 true ，否则就返回 false
      3.map 就是一个二维数组 ，表示迷宫
      4.i， j 就是老鼠的位置，初始化的位置(1,1);
      5. 逆归的找路，要先规定map数组的各个值得含义
          0 表示可以走   1 表示有障碍物   2表示可以走  3表示走过但是 走不通是死路
      6.当map[6][5] = 2 就说明 找到路，就可以结束，否则继续找
      7.确定老鼠找路的策略  下-》右-》上-》左

     */
        public boolean findway(int[][] map, int i, int j) {
            if (map[6][5] == 2) {
                return true;
            } else {
                if (map[i][j] == 0) {
                    map[i][j] = 2;
                    if (findway(map, i + 1, j)) {//下
                        return true;
                    } else if (findway(map, i, j + 1)) {//右
                        return true;
                    } else if (findway(map, i - 1, j)) {//上
                        return true;
                    } else if (findway(map, i, j - 1)) {//左
                        return true;
                    }else {
                        map[i][j] = 3;
                        return false;
                    }
                    } else {//map[i][j] == 1,2,3
                        return false;
                    }
                }
            }
        }


```

路径和找路的上下左右有关

### 汉诺塔

```Java
package com.byyj.ObjectOriented.ClassFollow.recursion;

public class hanioTower {
    public static void main(String[] args){//编写一个main方法
        Tower tower = new Tower();
        tower.move(3,'A','B','C');
    }
}
class Tower{//方法
    //num表示要移动的个数，abc分别表示ABC塔
    public void move(int num, char a, char b,char c){
        if(num == 1){//如果只有一个盘 num = 1；
            System.out.println(a + "->" + c);
        }else{//如果有多个盘，可以看成两个，最下面的和最上面的所有盘（num = 1）
            // (1)先移动上面所有的盘到b ，借助C 
            move(num - 1,a,c,b);
            System.out.println(a + "->" + c);
            move(num - 1, b,a,c);
        }
    }
}
```

### 八皇后

## overload重载

####  基本介绍

Java中允许同一个类中，多个同名方法的存在，但是要求 形参列表不一样

eg： System.out.println() ;out是printStream类型

好：就在于 减轻了起名 ， 记名的麻烦 





快速入门案例

```java
快速入门案例  问题
OverLoad01.java案例: 类: MyCalculator 方法: calculate
    calculate(int n1.int n2)//两个整数的和
    calculate(int n1,double n2) //一个整数一个double的和
    calculate(double n2, int n1)//一个double ,个Int和
    calculate(int n1int n2,int n3)//三int的和
```



解题步骤

```java
public class overload01 {
    public static void main(String[] args){
        Mycalculate mycalculate  = new Mycalculate();
        System.out.println( mycalculate.calculate(1,4) );
        System.out.println( mycalculate.calculate(1,4.5) );
        System.out.println( mycalculate.calculate(1.8,4) );
        System.out.println( mycalculate.calculate(1,4,3) );
        

    }
}
class Mycalculate {
    public int calculate(int n1, int n2) {
        return n1 + n2;
    }
    public double calculate( int n1, double n2){
        return n1 + n2;
    }
    public double calculate(double  n1,int n2){
        return n1 + n2;
    }
    public int calculate( int n1,int n2,int n3){
        return n1 + n2 + n3;
    }
}
```

#### 注意事项和使用细节

- 方法名：必须相同
- 参数列表：必须不同（参数类型或者个数或顺序，至少有一样不同，参数名无要求）
- 返回类型：无要求





## 可变参数

### 基本概念 和语法

**基本概念**

Java 允许将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法。就可以通过可变参数实现

**基本语法**

访问修饰符 返回类型 方法名（数据类型...形参名）{}

### 注意事项和使用细节

- 可变参数的实参可以为0 个或任意多个

- 可变参数的实参可以为数组

- 可变参数的本质就是数组

- 可变参数可以和普通类型的参数一起放在形参列表，但必须保证可变参数在最后

- 一个形参列表中只能出现一个可变参数

  ![image-20230706145118101](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230706145118101.png)

  

  ```java
  package com.byyj.ObjectOriented.ClassFollow.VariableParameter;
  
  import com.sun.xml.internal.ws.api.pipe.SyncStartForAsyncFeature;
  
  public class pratice {
      public static void main(String[] args){
      HspMethed hm = new HspMethed();
          System.out.println(hm.showScore("milan",90.5,85.7) );
          }
      }
  class HspMethed{
      //方法返回类型 又有名字又有数，到最后直接返回字符串就好
      //方法名
      //方法形参（String，double...）
      //方法体
      public String showScore(String name,double...scores) {
          double totalScore = 0;
          for (int i = 0; i < scores.length; i++) {
              totalScore += scores[i];
          }
  
  
          return name +"有" +scores.length + "门课成绩总分为=" + totalScore;
  
      }
  
  }
  ```

  

## 作用域（重要）（变量使用的范围）

### 基本使用：

- 1.在java编程中，主要变量就是属性（成员变量）和局部变量
- 2.我们说的局部变量一般是指在成员方法中定义的变量
- 3.java中作用域的分类
  - 全局变量：也就是属性，作用域为整个类体 cat类：cry，eat等方法使用属性
  - 局部变量：也就是出了属性之外的其他变量，作用域为定义它的代码块中
- 全局变量（属性）可以不赋值，直接使用，因为有默认值，局部变量必须赋值后，才能使用，因为没有默认值

### 注意事项和使用细节     

- 属性和局部变量可以重名，访问时遵循就近原则

- 在同一作用域中，比如在同一个成员方法中，两个局部变量，不能重名

- 属性生命周期比较长，伴随着对象的创建而创建，伴随着对象的销毁而销毁，局部变量生命周期较短，伴随着它的代码块的执行而创建，伴随着代码块的结束而销毁。即在一次方法调用过程中

- 作用域范围不同

  - 全局变量：可以被本类使用，或其他类使用（通过对象调用）
  - 局部变量：只能在本类中对应的方法中使用

- 修饰符不同

  - 全局变量/属性可以加修饰符

  - 局部变量不可以加修饰符

    ![image-20230706162152384](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230706162152384.png)

## 构造方法/构造器

本身就是一个方法，叫法不一一样而已，肯定可以学会的

看一个需求，前面我们在创建人类的对象时，是先把一个对象创建好后，再给他的年龄和姓名赋值，如果我现在要求，在创建人类的对象的时候，就直接指定对象的姓名和年龄，这时就可以

### 基本语法和说明

```java
[修饰符] 方法名（形参列表）{

方法体；

}
```

**说明**

- 构造器的修饰符可以默认 也可以是public protected private
- 构造器***没有返回值***
- 方法名 和类名字必须一样
- 参数列表 和成员方法一样的规则
- 构造器的调用系统完成

**基本介绍**

构造方法又叫构造器(constructor)，是类的一种特殊的方法，它的主要作用是**完成对新对象的初始化**

**特点**

- 方法名和类名相同
- 没有返回值 

- 在创建对象时，系统会自动调用该类的构造器完成对对象的初始化

### 注意事项和使用细节

- 一个类可以定义多个不同的构造器，即构造器重载

- 构造器名和类名要相同

- 构造器没有返回值

- 构造器是完成对象的初始化，并不是创建对象

- 在创建对象时，系统会自动的调用该类的构造方法

- 如果程序员没有定义构造器，系统就会自动给类生成一个默认的无参构造器（也叫默认构造器）

- 一旦定义了自己的构造器，默认的构造器就被覆盖了，就不能再使用默认的无参构造器了，除非显式的定义一下，即Dog（）{}    (很重要！！)

  ```java
  public class constructorDetails {
      public static void main(String[] args){
     //创建一个包含 name 和 age 参数的 person 对象；
          Personn p1 = new Personn("king",40);
     //创建一个包含name 参数的 Person 对象；
          Personn p2 = new Personn("milan");
     //输出属性
      System.out.println(p1.name  + p1.age );
      System.out.println(p2.name );
      }
  }
  //定义一个类Person
  class Personn {
  //定义两个属性，分别为 name 和 age
      String name;
      int age;
  //定义一个带参数的构造器，参数为pName 和 pAge ，用于初始化 name 和 age 属性
      public Personn(String pName, int pAge) {
          name = pName;
          age = pAge;
      }
  //定义一个带参数的构造器，参数为怕Name，用于初始化 name 属性
      public Personn(String pName) {
          name = pName;
  
      }
  }
  ```



扩展![image-20230706203544433](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230706203544433.png)

### 对象创建的流程分析

![image-20230707092044525](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230707092044525.png)



- 加载Person类信息（Person.class）,只会加载一次     
- 在堆中分配空间（就会有一个地址） 真正的对象是在堆里面
- 完成对象初始化
  - 默认初始化 age = 0   name = null
  - 显示初始化 age = 90  name = null
  - 构造器初始化 age = 20 ，name = 小倩（在常量池的空间 ，并且有个电池）
- 在对象在堆中的地址，返回给p （p是对象名，也可以理解为对象的引用）



## this

java虚拟机会给每个对象分配 this ，代表当前对象。

### this关键字

 ![image-20230707101231365](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230707101231365.png)

```java
public class This {
    public static void main(String[] args) {
        Dog d1 = new Dog("来福", 1);
        d1.info();
    }
}
class Dog{
    String name;
    int age;
    //构造器的name 和age，是局部变量，而不是属性
public Dog(String name, int age) {
   this.name = name;
    this.age = age;
}
public void info(){
    System.out.println(name + "\t" + age + "\t");

}}
```

### 小结（重要）

哪个对象调用，this就代表哪个对象

### 注意事项和使用细节

- this关键字可以用来访问本类的属性，方法，构造器

- this用于区分当前类的属性和局部变量

- 访问成员方法的语法：this方法名（参数列表）；

- 访问构造器语法：this（参数列表）：注意只能在构造器中使用(即只能在构造器中访问另外一个构造器)

  注意：访问构造器语法：this（参数列表）：必须放置第一条语句

- this不能在类中定义的外部使用，只能在类定义的方法中使用

this是一个成员变量，在方法中使用this关键字可以引用当前对象，从而访问其属性 和 调用其方法



```java
public class thiswork {
    public static void main(String[] args){
       //创建对象
        Person p1 = new Person("黄河",18);
        Person p2 = new Person("长江",18);
        //调用p1的comepareTo方法，将p2作为参数传递，并打印返回的结果
        System.out.println(p1.compareTO(p2) );
        //p1为当前对象 this，把p2传给了compare  to的Person p
    }
}

/*定义Person类，里面有name,age属性 ，并提供compareTo比较方法；
用于判断是否和另一个人相同，体工会测试类TestPerson用于测试
名字和年龄完全一样，就返回true，否则返回false

 */



class Person {
    String name;
    int age;
//定义一个名为Person 的公共构造器，可接受name和age参数 ；
    public Person(String name, int age) {
    //将传递的参数分别赋值给当前的name 和age属性，然后结束构造器
        this.name = name;
        this.age = age;
    }
//定义一个compareTO的公共方法，接受一个Person类型的参数person
    public boolean compareTO(Person p) {
       // if (this.name.equals(p.name) && this.age == p.age) {

        //return true;
        //} else {
            //return false;
        return this.name.equals(p.name ) && this.age == p.age ;
        }
    }
```

## 章节作业

### 08分析输出

```java 
public class Test {//公有类
    int count = 9;//属性

    public void count1(){//test类的成员方法
        this.count = 10;// 这个count 就是属性,改成10
        System.out.println("count1 = " + count);
    }

    public void count2(){//test类的成员方法
        System.out.println("count1 = " + count++);
    }

    //这是test类的main方法，任何一个类，都可有main
    public static void main(String args[]){
        //1.new Test()是匿名对象，匿名对象只能使用一次，使用后就不能再使用
        //2.new Test().count1(),创建好匿名对象后，就调用count()
        new Test().count1() ;
        Test t1 = new Test();
        t1.count2();
        t1.count2();
    }
}

//输出的是 9和10  但是分析的为 10,11
//因为 是count++ ，后++ ，先输出 ，后自增
```

![image-20230708115023919](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230708115023919.png)

### 10分析输出

```java
public class Dome10 {
    //定义一个公有静态方法main ，作为程序的入口点
    public static void main(String[] args) {
    }
}

    class Dome {
        int i = 100;
        public void m() {
            int j = i++;
            System.out.println("i=" + i);//
            System.out.println("j=" + j);//
        }
    }


    class Test {
        public static void main(String[] args) {
            Dome d1 = new Dome();
            Dome d2 = d1;
            d2.m();
            System.out.println(d1.i);
            System.out.println(d2.i);
        }
    }
```

![](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230708150149108.png)

调用m方法就产生了一个新的m栈，有个局部变量j，i将自己的属性赋给了j ，自己又自增101，   i



# --------- 面向对象（中级）

## intellij IDEA

### 介绍

1.IDEA 全称 intellij IDEA

2.公认最好的java开发工具

3.该工具是jetBrains公司的产品，总部位于捷克的首都布拉格

4.除了支持java的开发，还支持HTML ，CCS，PHP，MySQL，Python等

### IDE（集成开发环境） ---Eclipse

###  常用快捷键

- 删除当前行，自己配置ctrl + d

- 复制当前行，自己配置ctrl + alt + 向下光标

- 补全代码 alt + /

- 添加注释和取消注释 ctrl +  /[第一次是添加注释，第二次是取消注释]

  ctrl  +  D 是复制这一行并且粘贴

- 导入该行需要的类，先配置auto import，然后使用alt + enter 即可

- 快速格式化代码 ctrl+ shift + L

- 快速运行程序 alt + shift + F10

- 生成构造器等   alt + insert 【提高开发效率】

- 查看一个类的层级关系 ctrl + H （学习继承后 ，会非常的有用）

- 将光标放在一个方法上，输入 ctrl + B 可以定位到方法（学习继承后，会非常有用）

- 自动的分配变量名 ，通过 在后面  +   . var

- 其他快捷键

  - ctrl  +  Y 是删除这一行

    ctrl  +  A 是全部选择

    ctrl  +  Z 是撤销上一步1

    ctrl  +  G  是转到哪一行

### IDE（集成开发环境） IDEA的使用

模版 

file --->  settings ---->editor ------>live templates（模版） ---->

查看自己有多少模版快捷键  //  可以自己增添模版

模版可以高效的完成开发，提高速度

## 包

### 作用

- 区分相同名字的类
- 当类很多时，可以很好的管理类
- 控制访问范围

### 基本语法 

package com.xxxxx

**说明**

package 关键字 表示打包

com.xxxxx;表示包名

### 包的本质分析

实质上就是创建不同的文件夹来保存类文件，示意图如下

![image-20230710171524438](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230710171524438.png)

### 包的命名

#### 命名规则

只能包含数字，字母，下划线，小圆点，但是不能用数字开头，不能是关键字或者保留字

判断  eg : demo.class.exec1   //错误,因为有关键字

​				dome.12a     //错误， 因为数字不能开头

​				demo.ab12.oa  //   正确

#### 命名规范

一般是小写字母 + 小圆点    com.公司名.项目名.业务模块名

eg ：com.syj.oa.model      com.syj.oa.controller

举例子： com.sina.crm.user  //用户模块

  			  com.sina.crm.order  // 订单模块

​				com.sina.crm.utils   //工具类

### 常用的包

一个包下 ，包含很多类 ，java中常用的包有：

java.lang   //lang包是基本包，默认引入，不需要再引入.        不用再import  

java.util      // util 包 ，系统提供的工具包，工具类  ，使用Scanner

java.net      //网络包  ，网络开发

java.awt      // 是做java 的页面开发 ，GUI

### 如何引用包

com.syj.pkg  : import01.java

语法： 

Import 包；

引入一个包的主要目的是使用该包下的类

有两种引用方式

Import java.util.Scanner    //就只是引入  java.util 包下的  Scanner   

import java.util.* //表示 将java .util 包下的所有类都引入（导入）

（ 所以说 ，我们需要使用到那个类 ，就导入哪个类即可）

### 注意事项 和 使用细节

1. package的作用是声明 当前类所在的包 ，需要放在`class`的最上面，一个类中最多只有一句 `package`
2. import 指令位置放在 package 的下面 ，在类定义前面 ，可以有多句且没有顺序要求

![image-20230710200501674](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230710200501674.png)

​    

## 访问 修饰符

#### 基本介绍

java提供了四种访问修饰符号空号控制方法 和属性（成员变量） 的访问权限 （范围）；

1. 公开级别：`public`  修饰，对外公开
2. 受保护级别 ：`protected `修饰 ，对子类和同一个包中的类公开
3. 默认级别： 没有修饰符号，向同一个包的类公开
4. 私有级别：用`private`修饰，只有类本身可以访问，不对外公开



#### 4种访问修饰符的访问范围（需要背下来！）

![image-20230710201204044](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230710201204044.png)

使用的注意事项

1. 修饰符可以用来修饰类中的属性，成员方法以及类
2. 只有默认的和public 才能修饰类 ，并且遵循上述访问权限的特点
3. 成员方法的访问规则和属性完全一样



## * 封装

### 基本介绍：

（encapsulation）

 封装就是把抽象出的数据（属性） 和 对数据的操作【方法】封装在一起，数据被保护在内部，程序的其他部分只有通过被授权的操作【方法】，才能对数据进行操作

### 封装的理解和好处

1. 隐藏实现细节    方法（连接数据库）<-----调用（传入参数....）
2. 可以对数据进行验证 ，保证安全合理

### 封装的实现步骤

1. 将属性进行私有化 【不能直接修改属性】

2. 提供一个公共（public）set 方法 ，用于对属性判断并赋值

   ```java
   public void setXxx（类型 参数名）{
   
    		// 加入数据验证的业务逻辑
   
   ​		属性 = 参数名；
   
   }
   ```

   

3. 提供一个公共的get方法 ，用于获取属性的值

   ```java
   public XX getXxx（）{ // 权限判断  Xxx某个属性
   
   ​	return xx;
   
   }
   ```

   ### 快速入门案例

   ```java
   package com.JavaSE.byyj.ObjectOrientedSecond.encap;
   //题目： 编写一个小程序，不能随便查看人的年龄和薪水等隐私，
   //      并对设置的年龄进行合理的验证，年龄合理就设置，不合理就默认，
   //      年龄必须在1-120之间，工资不能直接查看，name的长度在 2 -6 字符之间_
   public class Encapsulation01 {
       public static void main(String[] args) {
           Person person = new Person();//创建一个Person类的对象
           person.name = "yingjie";//设置Person 对象的setName方法，将名字设置为。。。
           person.setName("sun");//调用类Person对象person的 setname方法，设置名字
           person.setAge(21);//同上
           person.setSalary(12000);//同上
           System.out.println(person.info() );//打印person对象的信息
       }
   }
   class Person{
       public String name;//定义公开属性，名字公开，可以直接访问
       private int age;//将 age 私有化，私有属性 ，只能通过setAge 和 getAge 方法来访问
       private double salary; //将 salary 私有化 ，私有属性 这能通过set 和 get方法 来访问
   
       //自己写代码太慢了  ，使用快捷键，alt + ins 弹出构造函数后，
       //选择getter 和setter 按住ctrl和shift键 进行全选，输出即可
       public String getName() {//定义一个getname 方法，用于获取名字属性的值
           return name;
       }
       public void setName(String name) {//定义一个setname方法，用于设置名字属性的值
           if(name.length() >= 2 && name.length() <= 6 ){  //设置时，进行验证
               this.name = name;
           }else{
                System.out.println("你设置的名字长度哪不对，应在2-6字符之间 ，给默认名字榴莲");
                this.name = "榴莲";
           }
       }
   
   
       public int getAge() { //获取年龄属性的值
           return age;
       }
       public void setAge(int age) {// 设置年龄属性的值
           if(age >= 1 && age <= 120){
               this.age = age;
           }else{
               System.out.println("你设置的年龄不在 1-120 之间，给默认年龄18");
               this.age = 18;
           }
       }
   
       public double getSalary() {// 获取
           return salary;
       }
       public void setSalary(double salary) { //设置
           this.salary = salary;
       }
   
       public String info(){ //定义一个info方法，用于获取Person对象的信息
           return "信息为姓名= " + name + "  年龄=" + age + "  薪水=" + salary;
       }
   }
   
   //其中Person类的属性name为公开属性，可以直接访问，
   //而age和salary为私有属性，只能通过set和get方法来访问。
   //set方法中，对年龄和名字长度进行了验证，如果不符合要求，则设置为默认值
   //最后，通过info方法获取Person对象的信息，将其打印出来。
   /
   ```

   #### 将构造器与setXxx结合

   ```java
     public Person() {
       }
       // 有三个构造器的存在
       public Person(String name, int age, double salary) {
           //this.name = name;
           //this.age = age;
           //this.salary = salary;
           //这种情况我们可以将set方法写在构造器中，这样任然可以验证
           setName(name);  //就是本类的  setname = this.setnamer
           setAge(age);
           setSalary(salary);
       }
   
   ```

   

## * 继承

继承     解决代码的复用性

### 基本介绍和示意图

继承可以解决代码复用，让我们的编程更加靠近人类的思维，当多个类存在相同的属性（变量）和方法时，可以在这些类中抽象出父类，在父类中定义这些相同的属性和方法，所有的子类不需要重新定义这些属性和方法，只需要通过extend来声明继承父类即可

### 基本语法

class 子类 extends 父类{

}

1. 子类就会自动拥有父类定义的属性和方法

2. 父类又叫做 超类，基类

3. 子类又叫派生类

   ![image-20230711142418769](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711142418769.png)

### 继承的好处

- 代码的复用性提高了
- 代码的扩展性和维护性提高了

### 继承的细节问题

1. 子类继承了所有的属性和方法，非私有的属性和方法可以在子类直接访问   但是私有属性和方法不能在子类直接访问，要通过公共方法去访问![image-20230711151520186](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711151520186.png)   

2. 子类必须调用父类的构造器，完成父类的初始化      

   ![image-20230711160605282](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711160605282.png)

3. 当创建i之类对象时，不管使用子类的哪个构造器 ，默认情况下总会去调用父类的无参构造器，如果父类没有提供无参构造器，则必须在子类的构造器中使用super去指定使用父类的哪个构造器完成对父类的初始化工作，否则，编译不会通过

4. 如果希望指定去调用父类的某个构造器，则显示的调用一下：super（参数列表）

   ![image-20230711163349740](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711163349740.png)

5. super在使用时，必须放在构造器第一行 (super 关键字只能在构造器中使用)

6. super（） 和 this（）都只能放在构造器的第一行，因此这两个方法不能共存在一个构造器     （不能共存）

7.  java所有类都是Object类的子类    ctrl  + H 就可以查看层级

   ![image-20230711171113492](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711171113492.png)

8. 父类构造器的调用不限于直接父类！ 将一直往上追溯查到nObject 类（顶级父类）

   ![image-20230711171416683](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711171416683.png)

9. 子类最多只能提供一个父类（指直接继承），即java中是单继承机制

10. 不能滥用继承，子类和父类之间必须满足is -a 的逻辑关系  是一个..

     animal   cat

### 继承的本质  内存布局和分析图

```java
public class theory {
    public static void main(String[] args) {
        Son son = new Son();
        //按照查找关系来返回信息
        //(1) 首先看子类有没有该属性
        //(2) 如果子类有这个属性，并且可以访问，则返回信息
        //(3) 如果子类没有这个属性，就看父类有没有这个属性// 如果父类有该属性，并且可以访问，就返回信息..）
        //    （如果父类有该属性，并且可以访问，就返回信息..）
        //(4) 如果父类没有就按照（3）的规则，继续找上级关系，直到Object...
        System.out.println(son.name);//输出的值是大头儿子
        System.out.println(son.age);// 输出的值是39
        System.out.println(son.hobby);//输出的值是旅游


    }
}
class GrandPa{
    String name = "大头爷爷";
    String hobby = "旅游";
}
class Father extends GrandPa{
    String name = "大头爸爸";
    int age = 39;
}
class Son extends Father{
    String name = "大头儿子";
}
```

![image-20230711194148393](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711194148393.png)

   //按照查找关系来返回信息
        //(1) 首先看子类有没有该属性
        //(2) 如果子类有这个属性，并且可以访问，则返回信息
        //(3) 如果子类没有这个属性，就看父类有没有这个属性// 如果父类有该属                                                                     性，并且可以访问，就返回信息..）
        //（如果父类有该属性，并且可以访问，就返回信息..）
        //(4) 如果父类没有就按照（3）的规则，继续找上级关系，直到Object...

super();//父类的无参构造器



### T1

```java
public class exercise01 {
    public static void main(String[] args) {
        B b = new B();//求B输出是什么？   B()  说明调用B类的无参构造器
    }
}
class A {
    A() {
        System.out.println("a");
    }
}
class B extends A {
    B() {

        this("abc");//调用本类的中带字符串的构造器
        System.out.println("b");
    }
    //然后在B(string name)中显式调用了父类的无参构造器super（）

    B(String name){
        super();
        System.out.println("b name");
    }
}
```

![image-20230711205712220](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230711205712220.png)



## * 多态          

### 基本介绍

方法或对象具有多种形态，是面向对象的第三大特征，多态是建立在封装和继承基础之上的

### 多态的具体体现

- 方法的多态  （重写和重载就体现了多态）
- 对象的多态（核心 ，困难，重点）
  - 一个对象的编译类型和运行类型可以不一致
  - 编译类型在敌对对象时，就确定了，不能改变
  - 运行类型是可以变化的
  - 编译类型看定义时 = 号 的左边 ， 运行类型看 =  号的右边

eg： Animal animal = new Dog（）；[anmial编译的类型 是Animal ，运行类型是 Dog ]

​                          animal就是对象的引用，， 一个父类对象的引用可以指向子类的一个对象

​		animal = new  Cat（）；[ animal 的运行类型变成了Cat ，编译的类型依然是 Animal]



### 注意事项和使用细节

多态的前提是：两个对象（类） 存在继承关系

#### 多态的向上转型

- 本质:  :  父类的引用指向了子类的对象

- 语法 ：父类类型   引用类型 = new 子类类型（）；

- 特点：

  - 编译类型看着左边 ，运行类型看右
  - 可以调用父类中的所有成员（需要遵守访问权限）；
  - 不能调用子类中特有成员，因为在编译阶段，能调用哪些成员，是有编译类型决定的
  - 最终的运行效果看子类的具体实现，即调用方法时，按照从子类（运行类型）开始查找方法，然后调用，规则和方法调用一致

  ​		

####  多态的向下转型

- 语法：子类类型  引用名  = （子类类型）**父类引用**；
- 只能强转父类的引用，不能强转父类的对象
- 要求父类的引用必须指向的是定期那目标类型的对象
- 当向下转型后，可以调用子类类型中所有的成员 

####  属性没有重写之说！

属性的值看编译类型![image-20230713095128070](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230713095128070.png)

instance of 比较操作符，用于判断对象的运行   类型是否为 XX类型 或者 XX类型的子类型

```java
public static void main(String[] args){
BB bb = new BB ();
System.out.println(bb instandof  BB);  //true
System.out.println(bb instandog  AA);  //true
}

class AA{} // 父类
class BB extends AA {}//子类
```







#### 课堂练习

![image-20230713101108532](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230713101108532.png)

### 动态绑定机制（非常非常重要）

1. 当调用对象方法的时候，该方法会和该对象的内存地址 / 运行类型绑定
2. 当调用对象属性时，没有动态绑定机制，哪里声明，哪里使用
3. 就是说 调用方法看运行的类型，调用属性看编译类型

### ![image-20230713102711869](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230713102711869.png)

### 多态的应用

1. 多态数组

   数组的定义类型是父类类型 ，里面保存的实际元素类型为子类类型

2. 多态参数

   方法定义的形参类型为父类类型，实参类型允许为子类类型

    



## Super  

### 基本介绍

super 代表父类的引用，用于访问父类的属性，方法，构造器

### 基本语法

1. 访问父类的属性，但是不能访问父类的 private属性

   super.属性名；

2. 访问父类的方法，不能访问父类的private方法

   super.方法名（参数列表）

3. 访问父类的构造器

   super（参数列表）；只能放在构造器的第一句，而且只能出现一句

### super给编程带来的便利  /  细节

1. 调用父类构造器的好处（分工明确，父类属性由父类初始化 ，子类的属性由子类初始化）
2. 当子类中有和父类中的成员（属性和方法）重名时，为了访问父类的成员，必须通过super。如果没有重名，使用super，this，直接访问时一样效果的

找cal方法时的 （cal（）和this（）），顺序是：

（1）先找本类，如果有，就调用

（2）如果没有，就找父类（如果有，并可以调用，则调用）

（3）如果父类没有，则继续找父类的父类，直到object

提示： 如果查找方法的过程中，找到了，但是不能访问，就报错，cannot access

​			如果查找方法的过程中，没有找到，则提示方法不存在

super.cal（）// 找cal方法的顺序就是直接查找父类，其他规则都一样

属性访问规则

n1  和 this.n1 查找的规则是

（1）先找本类，如果有，就调用

（2）如果没有就找父类（如果有，就调用）

### sdper关键字

super  的访问不限于直接父类，如果爷爷类和本类中有同名的成员，也可以使super去访问爷爷类的成员，如果多个基类（上级类） 中都有同名的成员。使用super访问遵循就近原则  A--> B --->C

### super  和 this 的区别 

|  NO  |   区别点   | this                                                   | super                                  |
| :--: | :--------: | ------------------------------------------------------ | -------------------------------------- |
|  1   |  访问属性  | 访问本类中的属性，如果本类没有此属性则从父类中继续查找 | 访问父类的属性                         |
|  2   |  调用方法  | 访问本类中的方法，如果本类没有此方法就是从父类继续查找 | 直接访问父类的方法                     |
|  3   | 调用构造器 | 调用本类的构造器，必须放在构造器的第一行               | 调用父类构造器，必须放在构造器的第一行 |
|  4   |    特殊    | 表示当前对象                                           | 子类中访问父类的对象                   |





## overwrite 方法重写  /  覆盖

### 基本介绍

简单地说： 方法覆盖（重写）就是子类有的一个方法，和父类的某个方法的名字，返回类型，参数一样，那我们就说子类的这个方法覆盖了父类的那个方法

### 注意事项和使用细节

方法重写也叫方法覆盖，需要满足下面的条件

1. 子类的方法的形参列表，方法名称要个父类的形参列表 ，方法名称完全一样

2. 子类的方法的返回类型 和 父类的返回类型是一样的，或者是父类返回类型的子类  ， 比如 父类返回的类型 Object ，子类的返回类型是String

3. 子类方法不能缩小父类方法的访问权限     意思就是说，子类的权限一定要大于父类才可以 ，子类都被限制访问了，还怎么访问父类啊

   public  > protected > 默认 >private

### 比较 方法重载  overload 和  方法重写 overwrite

###  

| 名称            | 发生范围 | 方法名 | 形参列表                         | 返回类型                                                     | 修饰符                             |
| --------------- | -------- | ------ | -------------------------------- | ------------------------------------------------------------ | ---------------------------------- |
| 重载  overload  | 本类     | 本类   | 类型，个数或者顺序至少有一个不同 | 无要求                                                       | 无要求                             |
| 重写  overwrite | 父子类   | 父子类 | 相同                             | 子类重写的方法，返回的类型和父类返回的类型一致，或者是其子类 | 子类方法不能缩小父类方法的访问范围 |



## Object类详解

![image-20230713154345925](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230713154345925.png)

### equals 方法

####  == 和 equals 的对比

1. ==：既可以判断基本类型，又可以判断引用类型
2. ==：如果判断基本类型，判断的是值是否相等  eg：int i= 10；double d = 10.0；
3. == ：如果判断引用类型，判断的是地址是否相等，即判定是不是同一个对象
4. equals 是Object类中的方法，只能判断引用类型，如何看jdk源码
   - 一般来说IDEA 配置好JDK 以后，jdk的源码也就自动配置好了
   - 如果没有的话点击菜单 File ---.>ProjectStructure-->    SDK--->Sourcepath,然后点击查看 侧绿色的加号
5. 默认判断的是地址是否相等，子类中往往重写该方法，用于判断内容是否相等， eg integer，String【看看String 和 integer 的equal 源代码】

==  基本数据类型判断 **数值** 是否相同，引用类型是判断 **地址**（也就是  是否指向同一个对象）

字符的本质就是整数





#### 如何重写Equals方法

应用案例：判断两个Person对象的内容是否相同，如果两个Person对象 的属性值都一样，则返回true，反之false

### hashCode方法

![image-20230713194149340](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230713194149340.png)

1. 提高具有哈希结构的容器的效率
2. 两个引用，如果指向的是同一对象，则哈希值肯定是一样的
3. 两个引用，如果指向的是不同对象，则哈希值是不一样的
4.  哈希值主要根据地址号来的！不能将哈希值等价于地址
5. 案例演示【测试啊obj1 = new A(); A obj2 =newA()； Aobj3 = obj1】

### toString方法

基本介绍

- 默认返回：全类名 + @ + 哈希值的十六进制，【查看Object 的 toString方法】

​      子类往往抽重写toString方法，用于返回对象的属性信息

- 重写toString方法，打印对象或者拼接对象时，都会自动调用该对象的toString形式

- 当直接输出一个对象的时候，toString方法会被默认的调用

```java
//object的toString  ()源码
//getClass().getName()  类的全类名（包名 + 类名）
//Integer.toHexString (hashCode( ))  将对象的hsahCode值转换成16进制字符串
public String toString（）{
return getClass ( ).getName( ) + " @
" + Integer.toHexString (hashCode( ))；
}


```



### finalize方法

1. 当对象被收回时，系统自动调用该方法的finalize方法，子类可以重写方法，做一些释放资源的操作
2. 什么时候被收回: 当某个对象没有任何引用时，则jvm 就认为这个对象是一个垃圾对象，就会使用垃圾回收制来销毁该对象，在销毁该对象前，会先调用finalize方法
3. 垃圾回收机制的调用，是由系统来决定的，也可以是通过System.gc（）主动触发垃圾回收机制
4. 【白学】，我们在实际开发中，几乎不会使用，更对应付面试

eg：

```java
public class Finalize_{
    public static void main(String[] args){
        Car bwv = new Car("宝马");
            bmv = null;
        System.gc();//主动调用垃圾回收器
        System.out.println("程序退出了");
        //这时，car对象就是一个垃圾，垃圾回收器就会回收（销毁）对象，在销毁对象前，会遍历该对象的finalize方法
        //程序员就可以在 finalize中，写自己的业务逻辑代码（比如释放资源，数据库连接，或者打开文件...）
        //如果程序员不重写finalize，那么就会调用Object类的finalize，即默认处理
        //如果程序员重写了finalize，就可以实现自己的逻辑
    }
}

class Car{
    private String name;//属性 资源
    public Car(String name);
    	this.name = name;
}



```











## 断点调试（debug）

### 一个实际需求

1. 在开发中，新手程序员在查找错误时，这时老程序员就会温馨提示，可以用断点调试，一步一步的看源码执行的过程，从而发现错误的所在
2. 在断点调试的过程中，是运行状态，是以对象的 运行类型来执行的

### 基本介绍

1. 断点调试是指在程序的某一行设置一个断点，调试时，程序运行到这一行就会停止，然后可以一步一步往下调试，调试过程中可以看到各个变量当前的值，出错的话，调试到出错的代码行即显示错误，停下，进行分析从而找到这个Bug
2. 断点调试是程序员必须掌握的技能
3. 断点调试也能帮助我们查看java底层源代码的执行过程，提高程序员的 java水平

### 断点调试的快捷键

F7（跳入）F8(跳过)    shift + F8（跳出）F9（resume ，执行到下一个断点）

F7：跳入方法内

F8： 逐行执行代码

shift + F8：跳出方法

将光标放在某个变量上，可以看到最新的数据

#### IDea debug 如何进人  JDK源码

解决方式1

使用 froce Step into快捷键  alt + shift + F7 

解决方式2

配置  点击 Setting--->Build,Execution,Deplyment---->Debugger---->Stepping,  把Do not  into  tthe classes中的 ajva ，javax取消勾选

![image-20230714091252614](C:\Users\LUCKYKING SUN\AppData\Roaming\Typora\typora-user-images\image-20230714091252614.png)                                                                          

断点可以在debug过程中 ，动态的下断点



# 项目&学以致用

## 零钱通

代码改进

1. 用户输入4 退出时，输出提示:你确定你要退出吗  "y / n",必须输入正确的 y / n ，否原循环输入指令，直到输入  y 或者是 n
2. 在收益入账和消费时，判断金额是否合理，并给出相应的提示i
3. 将面向过程的代码修改为面向对象的方法

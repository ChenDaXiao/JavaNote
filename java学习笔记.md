### 1.JDK相关的基本概念

- JDK：
  - java Development KIT，即java开发工具包。
  - 用于开发java程序。
- JRE：
  - java Runtime Environment，即java运行环境。
  - 用于运行java程序。
- JVM：
  - java Virtual Machine，java虚拟机。
  - 将java程序翻译成机器语言，交给底层操作系统执行，并保证运行效果，实现java程序的跨平台性。



### 2.IntelliJ IDEA简介

1. 集成开发环境（IDE）

   - 全称Integrated Development Environment，是指整合了代码的编写、运行、分析、调试等一系列功能的开发软件。
   - IDE大大提高了开发效率，简化开发操作，对代码的编写和维护起到很好的帮助作用。

2. IntelliJ IDEA

   - 简称IDEA，字面意思是“智能理念”，是JetBrains公司的产品

3. IDEA的下载

   - 官网：https://www.jetbrains.com/idea/
   - 点击下载按钮：DOWNLOAD

4. IDEA的安装

   ![image-20201216183804677](.\images\image-20201216183804677.png)

   - 注意事项：
     - 安装路径中不要包含特殊字符
     - 最好不要直接安装到盘符根目录下



### 3.第一个java程序

- 第一个java程序: HelloWorld：

  ```
  /**
      这是我的第一个java程序，HelloWorld案例
   */
  
  public class HelloWorld {
      /**
          main方法是程序的主入口，它的写法是固定的
       */
      public static void main(String[] args) {
          /*
              这个是main方法的主体
              我们要实现的功能都要写到这里
           */
          // 这是一个输出语句，可以将结果打印到控制台
          System.out.println("helloworld!");
      }
  }
  ```

1. java程序的最小单位是类，一个java程序至少拥有一个类

2. java程序的入口是main方法，main方法的格式是固定的：

   ```
   public static void main(String[] args){	
   }
   ```

3. 在控制台输出内容的语句：

   ```
   System.out.println("要输出的内容");
   ```

- HelloWorld案例的目录结构：

  ![image-20201216185325032](.\images\image-20201216185325032.png)

  - **.idea目录和.imi文件：**IDEA开发工具使用的配置文件，我们不需要操作，可以隐藏

  - **src文件：**source单词的缩写，即我们编写的代码即源文件存放在这个目录下
  - **out目录：**java程序的输出目录，java程序运行的时候，生产后缀名为.class的文件存放在该目录下

  - **External Libraries:** 扩展类库，即java程序编写和运行所依赖的JDK中的类



### 4.java程序开发与运行原理

- 运行流程：

  ![image-20201216190117798](.\images\image-20201216190117798.png)

  1. 编写源文件（.java）
  2. 通过javac命令编译成字节码文件（.class）
  3. 通过java命令运行字节码文件，在控制台打印结果



### 5.IDEA基本配置

- **设置字体：**File->Settings->Editor->Font
- **设置配色方案：**File->Settings->Editor->Colors Scheme
- **设置编码：**File->Settings->Editor->File Encodings
- **隐藏不需要的文件：**File->Settings->Editor->File Types



### 6.IDEA常用快捷键

|        快捷键         | 简介                                                         |
| :-------------------: | :----------------------------------------------------------- |
|       Ctrl + B        | 进入光标所在的方法/变量的接口或是定义处，等于Ctrl + 左键点击 |
|       Ctrl + D        | 复制光标所在行或者复制选择内容，并把复制内容插入光标位置下面 |
|       Ctrl + Y        | 删除光标所在行或者删除选中的行                               |
|       Ctrl + N        | 通过类名定位文件                                             |
|       Ctrl + F        | 在当前文件下文本查找                                         |
|       Ctrl + /        | 注释光标所在行代码                                           |
|    Ctrl + Alt + L     | 格式化代码 可以对当前文件和整个包目录使用                    |
| Ctrl + Alt + 左方向键 | 退回到上一个操作的地方                                       |
| Ctrl + Alt + 右方向键 | 前进到下一个操作的地方                                       |
| Ctrl + Alt + 上下箭头 | 移动当前代码行                                               |

- 补充两个快捷方式：
  - main方法的快捷键：psvm
  - 输出语句的快捷键：sout 
- 三种导包方式： 
  - A：手动导包 
  - B：点击鼠标自动生成 
  - C：快捷键：Alt + Enter



### 7.java语言编码规范

- 大括号成对、对齐写
- 左大括号前有空格
- 代码缩进
- 方法和程序块之间空行
- 并排语句加空格
- 运算符两侧加空格



### 8.java的注释

- 注释的概念：

  - 对程序作结束、解释说明的文字

- 注释能干什么：

  - 用于介绍、解释说明
  - 帮助我们调试错误

- 注释的分类：

  - **单行注释：** 

    ```
    // 这是一个输出语句，可以将结果打印到控制台
     System.out.println("helloworld!");
    ```

  - **多行注释: ** 

    ```
    /*
        这个是main方法的主体
        我们要实现的功能都要写到这里
    */
    ```

  - **文档注释：**

    ```
    /**
        main方法是程序的主入口，它的写法是固定的
    */
    ```
  
- 代码演练：

  ```
  /**
      这是我的第一个java程序，HelloWorld案例
   */
  
  public class HelloWorld {
      /**
          main方法是程序的主入口，它的写法是固定的
       */
      public static void main(String[] args) {
          /*
              这个是main方法的主体
              我们要实现的功能都要写到这里
           */
          // 这是一个输出语句，可以将结果打印到控制台
          System.out.println("helloworld!");
      }
  }
  ```



### 9.java的关键字

- 关键字的概念：

  - 被java语言赋予特定含义的单词

- 关键字的特点：

  - 组成关键字的字母全部小写
  - 常见的代码编辑器，对关键字有特殊的颜色标记

- 常见关键字举例:

  - 用于定义数据类型的关键字：

    ```
    class、 interface、 enum、 @interface、 byte、 short、 int、 long、 char、 float、 double、  boolean、 void
    ```

  - 用于定义数据类型值得关键字：

    ```
    true、 false、 null
    ```

  - 用于定义流程控制的关键字：

    ```
    if、 else、 switch、 case、 default、 for、 while、 do、 break、 continue、 return
    ```

  - 用于定义访问权限修饰符的关键字：

    ```
    public、 protected、 private
    ```

  - 用于定义类、函数、变量修饰符的关键字：

    ```
    abstract、 final、 static、 synchronize
    ```

  - 用于定义类与类之间关系的关键字：

    ```
    extends、 implements
    ```

  - 用于定义建立实例、引用实例、判断实例的关键字：

    ```
    new、 this、 super、 instanceof
    ```

  - 用于处理异常的关键字：

    ```
    try、 catch、 finally、 throw、 throws
    ```

  - 用于包的关键字：

    ```
    package、 import
    ```

  - 其它关键字：

    ```
    native、 strictfp、 transient、 volatile、 assert
    ```

    

### 10.java的常量

- 常量的概念

  - 在程序执行的过程中，其值不可以发生改变的量 

- 常量的分类

  -  字面值常量：
    1. 字符串常量，值使用“”括起来       “HelloWorld”
    2. 整数常量                                   12，-23
    3. 浮点数常量                                12.35
    4. 字符常量，值使用’‘括起来        ’a‘，’0‘
    5. 布尔常量，值只有两个             true，false
    6. 空常量                                        null
  -  自定义常量：
    - 

- 代码演练：

  ```
  public class ConstantDemo {
      public static void main(String[] args) {
          // 字符串常量
          System.out.println("abc");
          System.out.println("123");
  
          // 字符常量
          System.out.println('a');
          System.out.println('1');
  
          // 整数常量
          System.out.println(10);
          System.out.println(-10);
  
          // 浮点数常量
          System.out.println(1.2);
          System.out.println(-1.2);
  
          // 布尔常量
          System.out.println(true);
          System.out.println(false);
      }
  }
  ```



### 11.java的变量

- 变量的概念

  - 在程序执行的过程中，其值可以在某个范围内发生改变的量。
  - 变量的本质，是内存中的一小块区域。

-  变量的定义格式：

  - 数据类型 变量名 = 初始化值；

    ```
    int number = 4;
    ```

- 各部分的含义是什么?

  - 数据类型：变量变化的范围就是数据类型。
  - 变量名：每个变量都有一个名字，方便存取。
  - 初始化值：使用变量前，需要给变量赋值。

- 定义变量的注意事项

  - 整形默认是int类型, 定义long类型变量的时候, 后边要加字母L(大小写均可)
  - 浮点型默认是double类型, 定义float类型变量的时候, 后边要加字母F(大小写均可)

- 使用 变量的注意事项

  - 变量未赋值，不能使用。
  - 变量只在它所属的范围内有效（这也是变量的 作用域）。
  - 一行上可以定义多个变量，但是不建议这样写。

- 变量的定义和使用举例:

  ![image-20201217120139957](.\images\image-20201217120139957.png)

  - 举例：定义一个变量用于描述教室中学生的个数（如上图），如何定义呢？

    - 数据类型：学生个数是一个整数，在java中通常用int表示。
    - 变量名：表示个数的英文单词是number。
    - 初始化值：教室中学生的个数为12个。

  - 变量的使用

    - 直接通过变量名来使用变量。

    - 可以直接输出，也可以进行其它运算。

      ![image-20201217120647253](.\images\image-20201217120647253.png)

- 代码演练：

  ```
  public class VariableDemo {
      public static void main(String[] args) {
          // 定义变量，记录学生个数
          // 变量的定义格式：数据类型 变量名 = 初始化值
          int number = 12;
  
          // 使用变量
          System.out.println(number);
      }
  }
  ```



### 12.java的数据类型

- 数据类型的概念
  
- 变量变化的范围就是数据类型
  
- 类型的分类

  ![image-20201217121825831](.\images\image-20201217121825831.png)

  - **一、基本数据类型（四类八种）**

    - 为什么需要八种基本数据类型？

      - 设计多种数据类型的原因是为了更充分的利用内存空间，提高内存使用的效率。

    - 计算机存储数据的形式

    - 计算机中最小的存储单元是字节（Byte，通常用B表示），每个字节包含8个位（bit，又叫“比特位”通常用b表示，值 为0或1）。 

      - 1B（字节） = 8bit 
      - 1KB = 1024B 
      - 1MB = 1024KB 
      - 1GB = 1024MB 
      - 1TB = 1024GB

      ![image-20201217122356102](.\images\image-20201217122356102.png)

  - **二、引用数据类型（对象类型）**

    - 类（class）
    - 接口（interface）
    - 数组（[]）

- 变量的作用域：只在它（定义的位置）所属的代码块内有效

  - 代码块：一对大括号范围内的代码，称为一个代码块

- 使用变量的注意事项

  - 变量未赋值，不能使用。
  - 变量只在它所属的范围内有效（这也是变量的 作用域）。
  - 一行上可以定义多个变量，但是不建议这样写。

- 代码演练：

  ```
  /*
   *  变量的定义格式:
   *      数据类型 变量名 = 初始化值;
   *  数据类型:
   *      byte, short, int, long, float, double, char, boolean
   *  定义变量的注意事项:
   *      1. 整形默认是int类型, 定义long类型变量的时候, 后边要加字母L(大小写均可)
   *      2. 浮点型默认是double类型, 定义float类型变量的时候, 后边要加字母F(大小写均可)
   *  使用变量的注意事项
   *      1.变量未赋值，不能使用。
   *      2.变量只在它所属的范围内有效（这也是变量的 作用域）。
   *      3.一行上可以定义多个变量，但是不建议这样写。
   */
  public class VariableDemo2 {
      public static void main(String[] args) {
          //byte类型的数据
          byte b = 10;
          System.out.println(b);
  
          //short类型的数据
          short s = 10;
          System.out.println(s);
  
          //int类型的数据
          int i = 10000;
          System.out.println(i);
  
          //long类型的数据	 
          //整形默认是int类型, 定义long类型变量的时候, 后边要加字母L(大小写均可)
          long l = 10000000000L;
          System.out.println(l);
  
          //float类型的数据
          //浮点型默认是double类型, 定义float类型变量的时候, 后边要加字母F(大小写均可)
          float f = 12.3F;
          System.out.println(f);
  
          //double类型的数据
          double d = 12.3;
          System.out.println(d);
  
          //char类型的数据
          char ch = 'a';
          System.out.println(ch);
  
          //boolean类型的数据
          boolean b1 = true;          //是
          boolean b2 = false;         //否
          System.out.println(b1);
          System.out.println(b2);
          System.out.println("------------------------");
  
          int a;
          a = 10;
          System.out.println(a);
  
          // 代码块：用于大括号括起来的内容就是代码块
          {
              int aa = 20;
              System.out.println(aa);
          }
  
          // 一行上可以定义多个变量，但是不建议这样写。
          int bb = 1, cc = 2, dd = 3;
          System.out.println(bb);
          System.out.println(cc);
          System.out.println(dd);
  
      }
  }
  ```



### 13.java的数据类型转换

- 类型转换

  - 不同类型的数据之间可能会进行运算，而这些数据取值范围不同，存储方式不同，直接进行运算可能会造成数据损 失，所以需要将一种类型转换成另外一种类型再进行运算。

- 类型转换的分类

  - 隐式类型转换:     小转大的关系
    - 数据类型的范围从小到大如下:
      - byte,short,char  --> int(默认的整形) --> long --> float --> double(默认的浮点型)
  - 强制类型转换:     大转小的关系
    - 目标类型 变量名 = (目标类型)要转换的值;
    - 注意: 强制类型转换在使用的时候可能会出现丢失精度的问题.

  ![image-20201217131423359](.\images\image-20201217131423359.png)

- 代码演练：

  ```
  /*
      +: 加法.
  
      类型转换:
          隐式类型转换:     小转大的关系
              数据类型的范围从小到大如下:
               byte,short,char  --> int(默认的整形) --> long --> float --> double(默认的浮点型)
          强制类型转换:     大转小的关系
              目标类型 变量名 = (目标类型)要转换的值;
  
              注意: 强制类型转换在使用的时候可能会出现丢失精度的问题.
   */
  public class ConversionDemo {
      public static void main(String[] args) {
          // 定义两个int类型的变量
          int a = 10;
          int b = 20;
          System.out.println(a+b);
  
          int c = a + b;
          System.out.println(c);
          System.out.println("--------------------------");
  
          // 定义一个int类型的数据和一个byte类型的数据
          int aa = 10;
          byte bb = 20;
          System.out.println(aa+bb);
  
          int cc = aa + bb;
          System.out.println(cc);
          // byte cc = aa + bb;
          // System.out.println(cc);
          // 思考byte cc = aa + bb;为什么保存？  byte类型和int类型计算，会先将byte类型提升为int类型在计算，结果也是int类型
          System.out.println("--------------------------");
  
          // 思考:我就想用byte类型的变量接受aa+bb，怎么办？
          // 可以通过强制类型转换实现。格式：目标类型 变量名 = (目标类型)要转换的值;
          byte dd = (byte)(aa + bb);
          System.out.println(dd);
          System.out.println("--------------------------");
  
  
          double d1 = 3.14;
          int a1 = (int)d1;
          System.out.println(a1);
          // 输出结果为：3  注意: 强制类型转换在使用的时候可能会出现丢失精度的问题.
  
      }
  }
  ```

  

### 14.java的标识符

- 标识符的概念

  - 给类、方法、变量、常量等起名字的字符序列，就是标识符。 
  - 通俗地说，标识符就是在编程中程序员给类、方法、变量、常量等起的名字。

- 标识符的组成部分 

  - 英文大小写字母、数字、下划线（ _ ） 和美元符号（ $ ） 

- 标识符的定义规则 

  - 不能以数字开头 
  - 不能是关键字 
  - 严格区分大小写 

- 标识符的命名规范 

  - **类和接口：**首字母大写，如果有多个单词，每个单词首字母大写：HelloWorld，Student 
  - **变量和方法：**首字母小写，如果有多个单词，从第二个单词开始首字母大写：getName, studyJava 
  - **常量名（自定义常量）：**所有字母都大写，多个单词用下划线隔开(_)：MAX_VALUE 
  - **包名：**全部小写，如果有多级，用点号(.)隔开，遵循域名反写的格式：cn.itcast.demo 
    - 作用: 包其实就是文件夹, 用来区分重名类的.
  - **总结：**驼峰命名，见名知意

- 代码演练：

  ```
  public class IdentifierDemo {
      public static void main(String[] args) {
          int age = 20;
          System.out.println(age);
  
          int zhangSanAge = 23;
          System.out.println(zhangSanAge);
  
          int b2 = 10;
          // 1. 不能以数字开头.
          //int 2b = 10;
          System.out.println(b2);
  
          //2. 不能和Java中的关键字重名.
          int classNumber = 20;
  
  
          // 3. 严格区分大小写. 注意：变量a 和 变量A 是不一样的
          int a = 10;
          int A = 20;
      }
  }
  ```

  

### 15.java的运算符

- 运算符的概述

  - 对常量和变量进行运算操作的符号
  - 程序对数据进行运算时要用运算符

- 常见的运算符：

  - 算术运算符、赋值运算符、关系运算符、逻辑运算符、三元运算符
  
  ![image-20201217151639553](.\images\image-20201217151639553.png)

- 表达式

  - 用运算符把常量或者变量连接起来的式子称为表达式。

- 表达式类型

  - 表达式的类型为表达式运算结果的数据类型。

    ```
    整型表达式： 1+2 10*20       布尔型表达式： 2>1 (20-10) < 15
    ```

  

#### 1.算术运算符概述

- 算术运算符

  - 用来进行算术运算符的符号

- 算术运算符的分类

  ![image-20201217152456709](.\images\image-20201217152456709.png)

- 注意事项：
  - **/ ：** 除法运算符，得到两个数据相除的商。
    - **特点：**java中整数除以整数结果还是整数
  - **% ：**取模（取余）运算，得到两个数据相除的余数。
    - **特点：**可以用来判断两个数是否能够整除。
  - **规律：**左边小于右边，结果为左边，左边大于右边，看余数

- 代码演练

  ```
  /*
      算数运算符:
          分类:
              +,-,*,/,%
  
          /和%的区别:
              /: 获取两个数据相除的商.
              %: 获取两个数据相除的余数.
  
          注意:
              整数相除结果还是整数.
              想要得到小数, 就必须有浮点数参与运算.
   */
  public class OperatorDemo1 {
      public static void main(String[] args) {
          // 定义两个int类型的变量
          int a = 5;
          int b = 3;
          
          // 整数相除结果还是整数.
          System.out.println(a + b);      // 输出8
          System.out.println(a - b);      // 输出2
          System.out.println(a * b);      // 输出15
          System.out.println(a / b);      // 输出1
          System.out.println(a % b);      // 输出2
          System.out.println("----------------------------");
  
          // 想要得到小数, 就必须有浮点数参与运算.
          System.out.println(5/4);        // 输出1
          System.out.println(5.0/4);      // 输出1.25
          System.out.println(5/4.0);      // 输出1.25
          System.out.println("----------------------------");
          
          
          // 取余（取模）有个规律就是：左边小于右边，结果为左边，左边大于右边，看余数
          System.out.println(2%5);	//  输出2
          System.out.println(7%8);	//  输出7
          System.out.println(6%8);	//  输出6
          System.out.println("----------------------------");
          System.out.println(13%5);   //  输出3
          System.out.println(8%5);	//  输出3
          System.out.println(7%5);	//  输出2
      }
  }
  ```

  

- **加法运算（+）的特点**

  - 加号两边是数值型数据时，进行加法运算

    - ‘a’、‘0’等字符型数据参与运算时，用该字符在计算机中所表示的数值进行运算。

      ![image-20201217174917712](.\images\image-20201217174917712.png)

  - 加号两边有任意一边是字符串时，进行字符串的拼接

  - 代码演练:

    ```
    /**
     * 字符参与加法运算, 其实就是拿该字符在计算机中存储所表示的数据值来运算的.
     *  'a'     97
     *  'A'     65
     *  '0'     48
     *
     * 字符串参与加法运算, 其实这里不是加法, 而是字符串的拼接.
     */
    public class OperatorDemo2 {
        public static void main(String[] args) {
            // 字符的加法运算
            // 定义两个变量， int  char
            int a = 10;
            char ch = 'a';  // a的ascll对应字符值：97
            System.out.println(a + ch);     // 输出107
    
            //字符串的加法运算
            System.out.println("hello" + "world");      // 输出："helloworld"
            System.out.println("hello" + 10);           // 输出："hello10"
            System.out.println("hello" + 10 + 20);      // 输出："hello10" + 20  --> "hello1020"
            System.out.println(10 + 20 + "hello");      // 输出：30 + "hello"    --> "30hello"
        }
    }
    ```
  

  
- **自增和自减（++和--）运算**

  -  ++ ：自增1 

  - -- ：自减1 

  - 单独使用： 

    - 放在变量前或后结果一样 

  - 参与运算： 

    - 在变量前，先自增（自减） ，再进行其它运算 
    - 在变量后，先以原值进行其它运算，再自增（自减）

  - 代码演练：

    ```
    /**
     * 自增运算符(++)演示:
     *  作用:
     *      表示自身的值 + 1
     *
     *  用法:
     *      单独使用：放在变量前或后结果一样, 都是自身+1
     *      参与运算：
     *          在变量前，先自增，再以新值进行其它运算
     *          在变量后，先以原值进行其它运算, 再自增
     */
    public class OperatorDemo3 {
        public static void main(String[] args) {
            int a = 5;
            // 单独使用
            // a++;
            a++;
            // 下述输出语句的结果是: 把字符串"a: " 和 变量a的值进行拼接
            System.out.println("a:" + a);   // 输出结果：a:6
    
             //参与运算
            //++在后
            int a1 = 5;
            int b1 = a1++;
            System.out.println("a1: " + a1);      // 输出结果：a1:6
            System.out.println("b1: " + b1);      // 输出结果：b1:5
    
            //参与运算
            //++在前
            int a2 = 5;
            int b2 = ++a2;
            System.out.println("a2: " + a2);      // 输出结果：a2:6
            System.out.println("b2: " + b2);      // 输出结果：b2:6
        }
    }
    ```
  


#### 2.赋值运算符概述

- 赋值运算符

  - 即用于给变量赋值的运算符

- 常见的赋值运算符

  - 基本赋值运算符：   =

  - 扩展赋值运算符：   +=， -=， /=， *=， %=

    - 扩展赋值运算符的好处：

      - 省略了强制类型转换的操作

    - 用法：

      ```
      int a = 10;
      a += 20;	// 相当于 a = a + 20;
      System.out.println(a);	// 输出：30
      ```

    - 好处：

      ```
      short s = 1;
      //s = s + 1;  // 报错
      s += 1;       // 相当于 s = (short)(s + 1);
      System.out.println("s= " + s);   // 输出：  s=2
      ```

- 注意：

  - = ：表示赋值操作，不是相等
  - ==：用来表示相等

- 代码演练：

  ```
  /**
   * 赋值运算符:
   *  基本的赋值运算符:
   *      =
   *  扩展的赋值运算符:
   *      +=, -=, *=, /=, %=
   */
  public class OperatorDemo4 {
      public static void main(String[] args) {
          //基本的赋值运算符
          int a = 10;     //把10赋值给变量a
          System.out.println("a: " + a);
          System.out.println("-------------------------");
  
          //扩展的赋值运算符:
          //+=的作用: 把左右两边的数据相加, 然后把结果赋值给左边: a =  a + 20;
          a += 20;
          System.out.println("a: " + a);
          System.out.println("-------------------------");
  
          //扩展赋值运算符的好处
          short s = 2;
          //s = s + 1;  //为什么报错?  因为s + 1的结果是一个int类型的数据, 你把int类型的数据赋值给short类型的变量,肯定不行.
          //怎么解决呢?
          //方案一: 强制类型转换
         /* s = (short)(s + 1);
          System.out.println("s: " + s);*/
          System.out.println("-------------------------");
  
          //方案二: 通过扩展赋值运算符实现
          s+=3;
          System.out.println("s: " + s);
  
      }
  }
  ```
  
  

#### 3.关系运算符概述

- 关系运算符的定义：

  - 顾名思义，关系运算符是用来描述两个变量值之间的关系的

- 关系运算符的特点：

  - 关系运算符的运算结果都是布尔（ boolean ）类型，要么是true，要么是false

- 常见的关系运算符

  ![image-20201218113643503](.\images\image-20201218113643503.png)



- 注意事项：
  
  - 千万不要把 == 写成了 =
  
- 代码演练：

  ```
  /**
   * 关系运算符:
   *  分类:
   *      ==, !=, >, >=, <, <=
   *
   *  运算结果:
   *      关系运算符操作完毕后的结果肯定是boolean类型.
   *
   *  注意事项:
   *      千万不要把==写成了=.
   */
  
  public class OperatorDemo5 {
      public static void main(String[] args) {
          //定义三个变量
          int a = 10;
          int b = 20;
          int c = 10;
  
          //==: 等于
          System.out.println(a == b);     //false
          System.out.println(a == c);     //true
          System.out.println("-----------------------------");
  
          //!=: 不等于
          System.out.println(a != b);     //true
          System.out.println(a != c);     //false
          System.out.println("-----------------------------");
  
          //>: 大于
          System.out.println(a > b);      //false
          System.out.println(a > c);      //false
          System.out.println("-----------------------------");
  
          //>=: 大于等于
          System.out.println(a >= b);     //false
          System.out.println(a >= c);     //true
          System.out.println("-----------------------------");
  
          //注意: ==是判断是否相等, =是赋值的意思
          System.out.println(a == b);     //判断变量a和变量b的值是否相等, false
          System.out.println(a = b);     //将变量b的值赋值给变量a, 然后打印结果, 20
      }
  }
  ```
  
   

#### 4.逻辑运算符概述

- 逻辑运算符

  - 用于判断“并且”、“或者”、“除非”等逻辑关系

- 逻辑运算符的特点

  - 逻辑运算符两端一般连接值为布尔类型的关系表达式

- 常见的逻辑运算符

  - **逻辑与:  &&**, 并且的关系, 要求所有条件都满足, 即有false则整体为false
  - **逻辑或:  ||**, 或者的关系, 要求只要满足任意一个条件即可, 即有true则整体为true
  -  **逻辑非:  !**, 取反的意思, 以前为false, 现在为true; 以前为true, 现在为false  

  ![image-20201218120146870](.\images\image-20201218120146870.png)

- 代码演练：

  ```
  /**
   *  逻辑运算符:
   *      分类:
   *          逻辑与: &&, 并且的关系, 要求所有条件都满足, 即有false则整体为false
   *          逻辑或: ||, 或者的关系, 要求只要满足任意一个条件即可, 即有true则整体为true
   *          逻辑非: !, 取反的意思, 以前为false, 现在为true; 以前为true, 现在为false.
   *
   *      注意:
   *          偶数个逻辑非, 结果不变.
   */
  public class OperatorDemo6 {
      public static void main(String[] args) {
          // 案例: 韦小宝找媳妇儿
  
          // 刚开始眼光比较高, 要求既要长得好看,还要身材好
          // 前边的true表示: 长得好看, false表示长得不好看
          // 后边的true表示: 身材好, false表示身材不好
          System.out.println(true && true);            // 长得好看  并且  身材好     输出结果: true
          System.out.println(true && false);           // 长得好看  并且  身材不好    输出结果: false
          System.out.println(false && true);           // 长得不好看 并且 身材好      输出结果: false
          System.out.println(false && false);          // 长得不好看 并且 身材不好     输出结果: false
          // 结论：逻辑与: &&, 并且的关系, 要求所有条件都满足, 即有false则整体为false
          System.out.println("------------------------");
  
          // 韦小宝发现那样的媳妇儿不好找, 于是降低了择偶标准, 只要长得好看, 或者身材好就行
          System.out.println(true || true);            // 长得好看  或者  身材好      输出结果: true
          System.out.println(true || false);           // 长得好看  或者  身材不好    输出结果: true
          System.out.println(false || true);           // 长得不好看 或者  身材好      输出结果: true
          System.out.println(false || false);          // 长得不好看 或者  身材不好    输出结果: false
          // 结论: 逻辑或: ||, 或者的关系, 要求只要满足任意一个条件即可, 即有true则整体为true
          System.out.println("------------------------");
  
          // 韦小宝发现那样的媳妇儿不好找, 于是降低了择偶标准, 只要不是男的就行
          //true: 女  false: 男
          System.out.println(!true);  // 不是女的  输出结果：false
          System.out.println(!false); // 不是男的  输出结果：true
          // 结论: 逻辑非: !, 取反的意思, 以前为false, 现在为true; 以前为true, 现在为false.
          System.out.println("---------------------");
  
          System.out.println(!!!!!!true);    // ！的个数为6个，结果是它本身      输出结果：true
          // 结论：出现这种情况，当！的个数是偶数（双数）时，结果是它本身，如果是奇数（单数）时，结果是取反
      }
  }
  
  ```



#### 5.三元运算符概述

- 三元运算符

  - 三元运算符又叫“三目运算符”，即由三部分组成，格式如下：

    ```
    (关系表达式) ? 表达式1 ： 表达式2
    ```

- 运算流程

  - 如果关系表达式结果为true，运算后的结果是表达式1
  - 如果关系表达式结果为false，运算后的结果是表达式2

- 代码演练

  ```
  /**
   *  三元运算符:
   *      概述:
   *          也叫三目运算符, 即由三部分组成的.
   *
   *      格式:
   *          关系表达式 ? 表达式1 : 表达式2 ;
   *
   *      执行流程:
   *          先判断关系表达式是否成立,
   *              成立,   执行表达式1;
   *              不成立, 执行表达式2;
   */
  public class OperatorDemo7 {
      public static void main(String[] args) {
          //需求: 求两个整数的最大值
          //1. 定义两个变量记录两个整数.
          int a = 100;
          int b = 20;
  
          //2. 通过三元运算符计算他们的最大值.
          int max = (a >= b) ? a : b ;		// a大于等于b 这个表达式成立了，执行表达式1，返回结果a
  
          //3. 将结果打印到控制台上.
          System.out.println("max: " + max);		// 输出结果：max：100
      }
  }
  ```
  
  

### 16.Scanner的基本使用

- Scanner的概念

  - 扫描器。即可以通过Scanner类扫描用户在控制台录入的数据

- 键盘录入数据的步骤

  - 第一步：导包（位置放到class定义的上面）

    ```
    import java.util.Scanner;
    ```

  - 第二步：创建对象（创建键盘录入对象）

    ```
    Scanner sc = new Scanner(System. in);
    ```

  - 第三步：接收数据（接收键盘录入的数据）

    ```
    int a = sc.nextInt();
    ```

    ![image-20201218124038520](.\images\image-20201218124038520.png)

- 代码演练：

  ```
  //1. 导包
  import java.util.Scanner;
  public class ScannerDemo2 {
      public static void main(String[] args) {
          //需求: 键盘录入两个整数, 求它们的和
          //2. 创建键盘录入对象.
          Scanner sc = new Scanner(System.in);
  
          //3. 提示用户录入数据, 并接收.
          System.out.println("请录入第一个整数: ");
          int a = sc.nextInt();
          System.out.println("请录入第二个整数: ");
          int b = sc.nextInt();
  
          //4. 计算整数和.
          int sum = a + b;
  
          //5. 打印结果.
          System.out.println("sum: " + sum);
      }
  }
  ```
  
  

### 17.流程控制之选择结构

- 流程控制结构的概念
  - 程序的结果跟代码的执行顺序紧密相关，通过使用一些特定的语句控制代码的执行顺序从而完成特定的功能，这就是 流程控制结构。
- 流程控制结构的分类
  - 顺序结构
  - 选择（判断）结构
  - 循环结构



#### 1.顺序结构的概述

- 顺序结构的概念

  - 即程序按照代码的顺序从上往下、从左往右依次执行的代码结构。

  - 顺序结构是最简单的流程控制结构，不需要特定的语句，程序的大多数代码都是这样执行的。

    ![image-20201218125602472](.\images\image-20201218125602472.png)

- 代码演练：

  ```
  public class OrderDemo {
      public static void main(String[] args) {
          //顺序结构: 代码会按照从上往下, 从左往右的顺序, 依次逐行执行
          System.out.println("程序开始执行");
          System.out.println("A");
          System.out.println("B");
          System.out.println("C");
          System.out.println(10 + 20 + "hello");  //30hello
          System.out.println("程序执行结束");
      }
  }
  ```
  
  

#### 2.选择(判断)结构的概述

- 选择结构（判断）的概念

  - 根据不同的条件选择不同的代码来执行的代码结构。

  - 选择结构要先判断条件是否成立，条件成立则执行一部分代码，不成立则执行另外一部分或结束代码，所以选择结构 也叫判断结构。

    ![image-20201218130053804](.\images\image-20201218130053804.png)

- 选择结构的分类

  - if语句（共有三种格式）：如果

    - if一般用做区间值的判断，比如 
      - 当前时间为0~8点，小黑和你说“早上好”； 
      - 当前时间为9~12点，小黑和你说“中午 好”；

  - switch语句：转换，切换

    - switch一般用做固定值的判断，比如 

      - 你说“星期一”，小黑说“Monday”； 

      - 你说“星期五”，小黑说“Friday”；

        

##### 选择结构if的第一种格式

- if语句：如果

- 语法格式：

  ```
  if(关系表达式) {
  	// 语句体
  }
  ```

- 执行流程：

  1. 如果关系表达式成立, 则执行语句体1.
  2. 如果关系表达式不成立, 则不执行语句体1.

  ![image-20201218130704385](.\images\image-20201218130704385.png)

- 代码演练：

  ```
  /*
      选择结构之if语句:
          第一种格式:
              if(关系表达式) {
                  语句体1;
              }
          执行流程:
              如果关系表达式成立, 则执行语句体1,
              如果关系表达式不成立, 则不执行语句体1.
   */
  public class IfDemo1 {
      public static void main(String[] args) {
          System.out.println("开始执行");
  
          //定义两个int类型的变量
          int a = 10;
          int b = 10;
  
          //判断两个变量是否相等
          if(a == b) {
              //如果能走这里, 说明条件成立.
              System.out.println("a和b是相等的");
          }
  
  
          System.out.println("结束执行");
      }
  }
  ```



##### 选择结构if的第二种格式

- if...else...语句：如果...否则...

- 语法格式：

  ```
  if(关系表达式) {
  	语句体1;
  } else {
  	语句体2;
  }
  ```

- 执行流程：

  1. 先判断关系表达式, 看其是否成立(true:成立, false:不成立).
  2. 如果关系表达式成立, 则执行语句体1,
  3. 如果关系表达式不成立, 则执行语句体2.

  ![image-20201218131316262](.\images\image-20201218131316262.png)

- 代码演练：

  ```
  /*
      选择结构之if语句:
          第二种格式:
              if(关系表达式) {
                  语句体1;
              } else {
                  语句体2;
              }
          执行流程:
              先判断关系表达式, 看其是否成立(true:成立, false:不成立).
              如果关系表达式成立, 则执行语句体1,
              如果关系表达式不成立, 则执行语句体2.
   */
  public class IfDemo2 {
      public static void main(String[] args) {
          System.out.println("开始执行");
          //需求: 判断两个整数是否相等, 相等则打印"相等", 不相等则打印"不相等"
          int a = 20;
          int b = 20;
  
          //调用if语句的第二种格式
          if(a == b) {        //if: 如果
              //能走这里, 说明条件成立
              System.out.println("相等");
          } else {            //else: 否则
              //能走这里, 说明条件不成立
              System.out.println("不相等");
          }
  
          System.out.println("结束执行");
      }
  }
  ```



##### 选择结构if的第三种格式

- if...else if...else...语句：如果...如果...否则...

- 语法格式：

  ```
  if(关系表达式1) {
  	语句体1;
  } else if(关系表达式2){
  	语句体2;
  } else if(关系表达式3){
  	语句体3;
  } else if(关系表达式n){   //n的意思是: 这里可以写多个else if(关系表达式) {}
  	语句体n;
  } else {
  	语句体n + 1;
  }
  ```

- 执行流程：

  1. 先判断关系表达式1, 看其是否成立(true:成立, false:不成立).

  2. 成立,   则执行语句体1,

  3. 不成立, 则判断关系表达式2, 看其是否成立.

  4. 成立, 执行语句体2,

  5. 不成立, 则判断关系表达式3, 看其是否成立.

  6. 依次类推,

  7. 如果关系表达式n成立, 则执行语句体n, 否则执行语句体n + 1

     ![image-20201218132711010](.\images\image-20201218132711010.png)

- 代码演练：

  ```
  /*
      选择结构之if语句:
          第三种格式:
              if(关系表达式1) {
                  语句体1;
              } else if(关系表达式2){
                  语句体2;
              } else if(关系表达式3){
                  语句体3;
              } else if(关系表达式n){   //n的意思是: 这里可以写多个else if(关系表达式) {}
                  语句体n;
              } else {
                  语句体n + 1;
              }
          执行流程:
              先判断关系表达式1, 看其是否成立(true:成立, false:不成立).
              成立,   则执行语句体1,
              不成立, 则判断关系表达式2, 看其是否成立.
              成立, 执行语句体2,
              不成立, 则判断关系表达式3, 看其是否成立.
              依次类推,
             如果关系表达式n成立, 则执行语句体n, 否则执行语句体n + 1
   */
  import java.util.Scanner;
  public class IfDemo3 {
      public static void main(String[] args) {
          /*
              需求: 根据你输入的两数字，让黑马智能机器人小黑和你打招呼.
              你说0~12的数字,  小黑说: 上午好.
              你说13~18的数字,小黑说: 下午好
              你说19~24的数字,小黑说: 晚上好
              你说其他数字,   小黑说: 买了否冷, 我不认识这个时间!
           */
          Scanner sc = new Scanner(System. in);
          //1. 定义变量, 记录时间.
          int time = sc.nextInt();  //正确数据, 边界值, 错误数据
  
          //2. 小黑根据你的时间和你打招呼.
          if(time >=0 && time <=12 ) {
              System.out.println("小黑和我说: 上午好");
          } else if(time >=13 && time <=18) {
              System.out.println("小黑和我说: 下午好");
          } else if(time >= 19 && time <=24) {
              System.out.println("小黑和我说: 晚上好");
          } else {
              //说明上述的三组条件都不满足.
              System.out.println("小黑和我说: 买了否冷, 我不认识这个时间!");
          }
      }
  }
  ```



##### if语句的案例

- **if语句案例之获取两个整数的较大值**

- 需求：

  - 键盘录入两个数据，获取这两个数据的较大值

- 分析：

  -  A：键盘录入的三个步骤： 
    1. 导包；
    2. 创建键盘录入对象；
    3. 获取数据； 
  - B：获取两个数据的较大值：if语句的格式2实现 
  - C：把较大的结果输出 

- 代码演练：

  ```
  import java.util.Scanner;
  
  public class IfDemo4 {
      public static void main(String[] args) {
          //需求: 键盘录入两个数据, 获取这两个数据的最大值.
          //1. 创建键盘录入对象, 以便接收用户录入的数据(包含: 导包, 创建对象)
          Scanner sc = new Scanner(System.in);
  
          //2. 提示用户录入两个整数, 并接收.
          System.out.println("请录入第一个整数: ");
          int a = sc.nextInt();
          System.out.println("请录入第二个整数: ");
          int b = sc.nextInt();
  
          //3. 定义变量, 记录最大值.
          int max;
  
          //4. 通过if语句的第二种格式, 判断两个整数的最大值.
          if(a >= b) {
              //如果走这里, 说明a大
              max = a;
          } else {
              //如果走这里, 说明b大
              max = b;
          }
  
          //5. 将结果打印到控制台上.
          System.out.println("最大值是: " + max);
      }
  }
  ```
  
  

- **if语句案例之根据学生成绩输出对应级别**

- 需求：

  - 键盘录入学生考试成绩，请根据成绩判断该学生属于哪个级别
  - 90-100 皇帝   80-90 宰相    70-80 大臣     60-70 县官     60以下 草民

- 分析：

  - A：回顾键盘录入数据的步骤 
  - B：分数段较多，该使用if语句的格式3进行判断 
  - C：根据判断结果输出对应的级别

- 小贴士：

  - 写程序的时候，做数据测试，应该测试这样的几种情况：
    -  正确数据   错误数据   边界数据

- 代码演练：

  ```
  import java.util.Scanner;
  
  public class IfDemo6 {
      public static void main(String[] args) {
            /*
              需求：键盘录入学生考试成绩，请根据成绩判断该学生属于哪个级别
                   90-100	           皇帝
                   80-90(不包含)      宰相
                   70-80(不包含) 	 大臣
                   60-70(不包含) 	 县官
                   60(不包含) 以下     草民
           */
          //1. 创建键盘录入对象.
          Scanner sc = new Scanner(System.in);
  
          //2. 提示学生录入成绩, 并接收.
          System.out.println("请录入您的成绩: ");
          int score = sc.nextInt();   //正确的数据, 错误的数据, 边界数据
  
          //3. 根据学生录入的成绩, 和题设的条件进行对比, 并按照要求进行输出即可.
          if (score >= 90 && score <= 100) {
              System.out.println("皇帝");
          } else if(score >= 80 && score < 90) {
              System.out.println("宰相");
          } else if(score >= 70 && score < 80) {
              System.out.println("大臣");
          } else if(score >= 60 && score < 70) {
              System.out.println("县官");
          } else if(score >= 0 && score < 60) {
              System.out.println("草民");
          } else {
              System.out.println("没有这样的成绩, 你是从火星来的吧?");
          }
      }
  }
  ```



#### 3.选择结构switch语句的概述

- switch语句的格式：

  ```
  switch(表达式) {
  	case 值1:
  		语句体1;
  		break;
  	case 值2:
  		语句体2;
  		break;
  	// ...
  	default:
  		语句体n+1;
  		break;
  }
  ```

- 格式含义的解释：

  ![image-20201218143609606](.\images\image-20201218143609606.png)

- 小贴士：

  - 枚举指的是一系列数目可数的数据。比如每周的星期，每年的月份。
  - String即字符串。双引号中的内容都是String类型。

- 执行流程：

  ![image-20201218143804926](.\images\image-20201218143804926.png)



##### switch语句的案例

- 需求：

  - 根据键盘录入的数字（ 1-7 ），输出对应的星期

- 分析：

  - A：使用键盘录入功能获取用户输入的数字 
  - B：switch的表达式为接收用户录入数据的变量 
  - C：分别用1-7作为case的值，并输出对应的星期 
  - D：当输入数据有误时，在default中输出提示

- 代码演练：

  ```
  import java.util.Scanner;
  
  public class SwitchDemo {
      public static void main(String[] args) {
          //需求: 键盘录入数字, 根据数字打印其对应的星期.
          //1. 创建键盘录入对象, 以便接收用户录入的数字.
          Scanner sc = new Scanner(System.in);
  
          //2. 提示用户录入数字, 并接收.
          System.out.println("请录入一个数字, 我来打印其对应的日期: ");
          int week = sc.nextInt();
  
          //3. 根据用户录入的数字, 打印对应的日期.  通过switch语句来实现.
          switch (week) {
              case 1:
                  System.out.println("星期一");
                  break;  //可以跳出(结束)switch语句
              case 2:
                  System.out.println("星期二");
                  break;
              case 3:
                  System.out.println("星期三");
                  break;
              case 4:
                  System.out.println("星期四");
                  break;
              case 5:
                  System.out.println("星期五");
                  break;
              case 6:
                  System.out.println("星期六");
                  break;
              case 7:
                  System.out.println("星期日");
                  break;
              default:
                  System.out.println("我不认识这样的时间, 你是从火星来的吧?");
                  break;
          }
      }
  }
  ```
  
  

### 18.流程控制之循环结构

- 循环结构的概念
  - 循环，即事物周而复始的变化。 
  - 循环结构，使一部分代码按照**次数**或**一定的条件**反复执行的一种代码结构。
- 循环结构的分类
  - for循环
  - while循环
  - do...while循环

#### 1.for循环

- for循环语句格式：

  ```
  for(初始化语句; 判断条件语句; 控制条件语句) {
  	// 循环体
  }
  ```

- 执行流程：

  ![image-20201218181352063](.\images\image-20201218181352063.png)

- 代码演练：

  ```
  public class ForDemo2 {
      public static void main(String[] args) {
          //需求1: 打印1~5之间的数字
          //方式一: 传统做法
          System.out.println(1);
          System.out.println(2);
          System.out.println(3);
          System.out.println(4);
          System.out.println(5);
          System.out.println("---------------");
  
          //通过观察上述的代码,我们发现: 输出语句的次数是固定的, 只有输出语句里边的内容在发生变化.
          //针对于这种情况, 就可以采用for循环来解决
          //方式二: 采用for循环
          for(int i = 1; i <= 5; i++) {
              System.out.println(i);
          }
      }
  }
  ```



##### for循环案例一

- 需求：
  
- 在控制台输出1-5/在控制台输出5-1
  
- 分析：

  - A：用原始方式实现输出1-5 
  - B：用for循环实现输出1-5 
  - C：用for循环实现输出5-1

- 代码演练：

  ```
  public class ForDemo1 {
      public static void main(String[] args) {
          //需求1: 打印1~5之间的数字
          //方式一: 传统做法
          System.out.println(1);
          System.out.println(2);
          System.out.println(3);
          System.out.println(4);
          System.out.println(5);
          System.out.println("---------------");
  
          //通过观察上述的代码,我们发现: 输出语句的次数是固定的, 只有输出语句里边的内容在发生变化.
          //针对于这种情况, 就可以采用for循环来解决
          //方式二: 采用for循环
          for(int i = 1; i <= 5; i++) {
              System.out.println(i);
          }
          System.out.println("---------------");
  
          //需求2: 打印5~1之间的数字
          for(int i = 5; i >= 1; i--) {
              System.out.println(i);
          }
      }
  }
  ```



##### for循环案例二

- 需求：

  - 输出1-5数据之和

- 分析：

  - A：定义一个求和变量sum，初始化值是0 
  - B：用for循环获取1-5的数据 
  - C：把每一次获取到的数据累加到求和变量sum 
    - sum = sum + x; 或者 sum += x; 
  - D：输出求和变量

- 代码演练：

  ```
  public class ForDemo2 {
      public static void main(String[] args) {
          //需求: 计算1~5之间的所有数据之和.
          //1. 定义求和变量sum.
          int sum = 0;
          //2. 通过for循环获取1~5之间的数据.
          for(int i = 1; i <=5; i++) {
              //i记录的就是: 1~5之间所有的数字.
  
              //3. 把获取到的数据依次累加给变量sum.
              //sum = sum + i;
              sum += i;
          }
          //4. 打印结果.
          System.out.println(sum);
      }
  }
  ```



##### for循环案例三

- 需求：

  - 求出1-100之间偶数和

- 分析：

  - A：定义一个求和变量sum，初始化值是0 
  - B：获取1-100之间的数，用for循环实现 
  - C：判断每一个数是否为偶数，是就累加，否则不做操作对2取余等于0，则为偶数： x % 2 == 0 
  - D：for循环结束，输出求和变量的值

- 代码演练：

  ```
  public class ForDemo3 {
      public static void main(String[] args) {
          //需求: 计算1~100之间的所有偶数和.
          //1. 定义一个求和变量sum.
          int sum = 0;
          //2. 获取1~100之间所有的数据.
          for(int i = 1; i <= 100; i++) {
              //循环体
              //i的值其实就是1~100之间的数字, 只要判断i是否是偶数即可.
              //3. 判断当前获取到的数据是否是偶数, 是就累加.
              if(i % 2 == 0) {
                  //能走到这里, 说明i是偶数, 累加即可.
                  sum += i;
              }
          }
          //4. 打印结果.
          System.out.println("sum: " + sum);
      }
  }
  ```



##### for循环案例四

- 需求：

  -  在控制台输出所有的”水仙花数”

- 分析：

  - 水仙花数：所谓的水仙花数是指一个三位数，其各位数字的立方和等于该数本身 
    - 举例：153是一个水仙花数： 111 + 555 + 333 = 1 + 125 + 27 = 153

- 实现步骤：

  - A：获取所有的三位数，即100-1000之间的数 
  - B：获取每一个三位数的个位，十位，百位 
    - 个位：153 % 10 = 3 
    - 十位：153/10%10 = 5 
    - 百位：153/10/10%10 = 1 
  - C：拿个位，十位，百位的立方和与该数本身进行比较，如果相等， 则在控制台打印该数

- 代码演练：

  ```
  public class ForDemo4 {
      public static void main(String[] args) {
           /*
              需求: 打印所有的水仙花数.
                  水仙花数解释: 指的是一个三位数, 其各位数字的立方和等于它本身. 例如:
                               1*1*1 + 5*5*5 + 3*3*3 = 1 + 125 + 27 = 153
           */
           //1. 通过for循环, 获取所有的三位数.
          for(int i = 100; i < 1000; i++) {
              //i表示的就是所有的三位数.
              //2. 获取该数据的个位, 十位, 百位数字.
              int ge = i % 10;
              int shi = i/10%10;
              int bai = i/10/10%10;
  
              //3. 判断该数字是否是水仙花数, 如果是, 直接打印即可.
              if(ge*ge*ge + shi*shi*shi + bai*bai*bai == i) {
                  //能走到这里, 说明i是水仙花数
                  System.out.println(i);
              }
          }
      }
  }
  ```



##### for循环案例五

- 需求：

  - 统计所有的”水仙花数”的个数

- 分析：

  - A：定义统计变量count，即计数器，初始化值为0 
  - B：获取所有的三位数，即100-1000之间的数 
  - C：判断每一个三 位数是否为水仙花数，是则count自增1 count ++; 
  - D：循环结束，输出计数器count的值

- 代码演练：

  ```
  public class ForDemo5 {
      public static void main(String[] args) {
          //需求: 打印所有的水仙花数的个数.
          //1. 定义一个计数器, 用来记录水仙花数的个数.
          int count = 0;
          //2. 获取到所有的三位数.
          for(int i = 100; i < 1000; i++) {
              //i记录的就是所有的三位数
              //3. 获取到该数字的个位, 十位, 百位数字.
              int ge = i % 10;
              int shi = i / 10 % 10;
              int bai = i / 10 / 10 % 10;
  
              //4. 判断该数字是否是水仙花数, 如果是, 计数器自增1.
              if(ge*ge*ge + shi*shi*shi + bai*bai*bai == i) {
                  //能走到这里, 说明i是一个水仙花数,
                  //count = count + 1;
                  //count++;
                  ++count;
              }
          }
          //5. 打印计数器的结果即可.
          System.out.println("水仙花数的个数是: " + count);
      }
  }
  ```



#### 2.while循环

- while循环语句格式：

  ```
  初始化语句;
  while(判断条件语句) {
  	循环体语句;
  	控制条件语句;
  }
  ```

- 注意事项：

  - 初始化语句可以省略 控制条件语句可以省略

- 执行流程：

  ![image-20201219123139179](.\images\image-20201219123139179.png)

##### while循环案例一

-  需求：

  - 使用while循环在控制台输出5次“HelloWorld”

- 分析：

  - A：用for循环实现输出“HelloWorld” 
  - B：用while循环实现输出“HelloWorld”

- 代码演练：

  ```
  /*
          while循环的格式:
              初始化语句;
              while(判断条件语句) {
                  循环体语句;
                  控制条件语句;
              }
       */
  public class WhileDemo1 {
      public static void main(String[] args) {
          //需求: 打印5次HelloWorld
          //方式一: 通过for循环实现
          //初始化语句;  判断条件语句;  控制条件语句
          for(int i = 1; i <= 5; i++) {
              //循环体语句
              System.out.println("HelloWorld");
          }
          System.out.println("---------------");
  
          //方式二: 通过while循环实现
          //初始化语句
          int i = 1;
          //判断条件语句
          while(i <= 5) {
              //循环体语句
              System.out.println("HelloWorld");
              //控制条件语句
              i++;
          }
      }
  }
  ```

##### while循环案例二

- 需求：

  - 求1-100之间的数据和

- 分析：

  - A：定义求和变量sum，初始化值为0 
  - B：使用while循环获取1-100之间的数据 
  - C：将每个数据累加到sum变量上 
  - D：循环结束，输出sum的值

- 代码演练：

  ```
  public class WhileDemo2 {
      public static void main(String[] args) {
          //需求: 计算1~100之间的所有数据之和.
          //1. 定义一个求和变量sum.
          int sum = 0;
  
          //2. 通过while循环, 获取1~100之间所有的数据.
          //初始化语句
          int a = 1;
          //判断语句
          while(a <= 100) {
              //循环体语句
              //3. 将获取到的数据累加给变量sum.
              sum += a;
              //控制条件语句
              a++;
          }
          //4. 将sum的结果打印到控制台上.
          System.out.println("sum: " + sum);
      }
  }
  ```



#### 3.do...while循环

- do...while循环语句格式：

  ```
  初始化语句;
  do {
  	循环体语句;
  	控制条件语句;
  } while(判断条件语句);
  ```

- 注意事项：

  - while小括号后的分号不可省略
  - do…while循环的循环体语句至少执行1遍

- 执行流程：

  ![image-20201219152945095](.\images\image-20201219152945095.png)



##### do...while循环案例

- 需求：

  - 用do…while循环模拟：学完一个知识，至少练习1次

- 分析：

  - A：定义int型变量count，即练习的次数，初始化值为1
  - B：定义boolean型变量isOK，作为一个标记，表示是否学会，初始化值为false
  - C：在do…while循环体中： 
    - 输出正在练习的次数 
    - 判断当练习次数不少于3时，表示已学会：isOK=true 
    - 每练习一次，次数自增1：count ++; 
  - D：while判断是否学会

- 代码演练：

  ```
  /*
      需求: 用do.while循环模拟 练习知识点的过程.
      要求:
          至少练习一次, 并且练习次数不小于3次就表示这个知识点你学会了.
   */
  public class DoWhileDemo {
      public static void main(String[] args) {
          //1. 定义一个变量, 记录练习次数.
          int count = 1;
          //2. 定义一个变量, 用来标记是否学会这个知识点. true: 学会了, false: 没学会.
          boolean isOK = false;
          //3. 在do..while循环中模拟这个动作.
          do{
              //输出练习次数
              System.out.println("正在进行第" + count + "次练习");
              //判断练习次数, 看是否不小于三, 如果条件成立, 表示学会了.
              if (count >= 3) {
                  //能进来, 说明学会了.
                  //将boolean类型变量的值改为: true
                  isOK = true;
              }
              //不管是否学会, 每练习一次, 次数要+1
              count++;
          }while(!isOK);
      }
  }
  ```

  

#### 4.三种循环的区别

- 三种循环的区别

  ![image-20201219154352014](.\images\image-20201219154352014.png)	

- 代码演练：

  ```
  public class DoWhileDemo2 {
      public static void main(String[] args) {
          //需求: 演示三种循环的区别
          /*
              1. 格式不同.
              2. 初始化语句不同
              3. 循环体的执行次数不同.
              4. 使用场景不同.
           */
          //案例: 分别通过三种循环打印1~5之间的数字
          //for循环		
          // for(int a = 10; a <= 5; a++) {  // 当a大于条件值时，不成立不会执行
          for(int a = 1; a <= 5; a++) {
              System.out.println("a: " + a);
          }
          //System.out.println(a);  这样写不行, 因为for循环执行结束后, 初始化条件就不能使用了.
          System.out.println("-------------------------");
  
          //while循环
          int b = 1;
          // int b = 10;		// 当b大于条件值时，不成立不会执行
          while(b <= 5) {
              System.out.println("b: " + b);
              b++;
          }
          //System.out.println("b::::: " + b);
          System.out.println("-------------------------");
  
          //do..while循环
         int c = 1;
         // int c = 10;	// 不管判断条件是否成立, 循环体都会先执行一次.
         do{
             System.out.println("c: " + c);
             c++;
         }while(c <= 5);
          //System.out.println("c::::: " + c);
      }
  }
  ```



#### 5.死循环

- 两种简单的死循环

  ![image-20201219155804019](.\images\image-20201219155804019.png)

- 代码演练：

  ```
  public class DeadDemo {
      public static void main(String[] args) {
          //需求: 演示死循环
          /*
              格式1: for的死循环
                  for(;;) {
                      循环体
                  }
           */
        /*  for(;;) {
              System.out.println("看看我是不是会一直执行!");
          }*/
  
        /*
          格式二: while循环的死循环
              while(true){
                  //循环体
              }
         */
        while(true) {
            System.out.println("看看我是不是会一直执行!");
        }
      }
  }
  ```



#### 6.break的概述

- break的概念

  - brea是中断的意思，用于switch语句和循环语句：
    - 在switch语句中，表示结束switch代码块 
    - 在循环语句中，表示结束循环

- break的案例：

  - 需求：

    - 查找班级编号为3的同学（假设班级中有15位同学）

  - 分析：

    - A：使用for循环先遍历班级每一个同学 
    - B：在班级循环体中，判断同学编号是否为3 
      - 若该同学编号为3，则打印该同 学编号，结束循环 
      - 若该同学编号不为3，不做任何操作

  - 代码演练：

    ```
    public class BreakDemo1 {
        public static void main(String[] args) {
            //需求: 假设班级有15名学生, 查找编号为3的学生, 找到后循环就结束了.
            //1. 通过for循环获取到每一位学生的编号.
            for(int i = 1; i <= 15; i++) {
                //为了让你更好的理解break的作用, 我加一个输出语句
                System.out.println("我是编号为:" + i + "的学生");
    
                //2. 判断该学生的编号是否为3.
                if (i == 3) {
                    //3. 如果编号为3, 则结束整个循环.
                    System.out.println("找到了编号为" + i + "的学生, 循环结束");
                    break;  //终止循环
                }
            }
    
        }
    }
    ```

    

#### 7.continue的概述

- continue的概念

  - 继续，用于循环语句，表示结束本次循环，继续下次循环

- continue案例

  - 需求：

    - 一起来玩逢7必过小游戏

  - 游戏规则：

    - 多人围坐在一起，依次快速说出从1-100的数字，所有含7或7的倍数的数不能说，否则就失败受到惩罚

  - 分析：

    - A：使用for循环遍历1-100的数 
    - B：在循环体中，判断数中是否含7或是否为7的倍数 
      - 是否含7：个位含7（模以10等 于7），十位含7（70-79） 
      - 是否为7的倍数：对7取模，余数为0 
    - C：跳过所有含7和7的倍数的数：continue 
    - D：打印 其它数

  - 代码演练：

    ```
    public class ContinueDome1 {
        public static void main(String[] args) {
            //需求: 模拟逢7必过的小游戏.
            //1. 通过for循环获取到1~100之间所有的数据.
            for(int i = 1; i <= 100; i++) {
                //2. 判断当前数字是否是合法数据.
                //包含7或者是7的倍数, 这些数据都是不合法的.
                if(i%10 == 7 || i/10%10 == 7 || i % 7 == 0) {
                    //3. 如果数据不合法, 直接跳过本次循环, 直接进行下次循环.
                    System.out.println("...");
                    continue;
                }
                //4. 如果数据合法, 直接打印即可.
                System.out.println(i);
            }
        }
    }
    ```



#### 8.循环嵌套的概述

- 循环嵌套的概念

  - 在一个循环体语句中包含另一个循环语句时，称为循环嵌套

- 循环嵌套的案例

  - 需求：

    - 按班级获取所有同学（3个班级，每班5个同学）

  - 分析：

    - A：先使用for循环遍历每一个班级 
    - B：在班级循环体中，再使用for循环遍历每个班级的同学 
    - C：打印正在获取的第 几个班级的第几位同学

  - 代码演练：

    ```
    public class ForForDemo {
        public static void main(String[] args) {
            //需求: 按照班级获取该班级所有的同学(假设一共有3个班级, 每个班级5名同学).
            //原始做法
           /* //获取第一个班级的每一位同学
            for(int i = 1; i <= 5; i++) {
                System.out.println("正在获取第1个班级的第" + i + "名同学");
            }
            System.out.println();  //作用: 换行
    
            //获取第二个班级的每一位同学
            for(int i = 1; i <= 5; i++) {
                System.out.println("正在获取第2个班级的第" + i + "名同学");
            }
            System.out.println();  //作用: 换行
    
            //获取第三个班级的每一位同学
            for(int i = 1; i <= 5; i++) {
                System.out.println("正在获取第3个班级的第" + i + "名同学");
            }
            System.out.println();  //作用: 换行*/
    
           //通过观察上述的代码, 我们发现打印每个班级学生的动作都是重复的, 所以我们可以继续通过循环优化.
            //1. 通过for循环获取每一个班级.
            for (int a = 1; a < 4; a++) {       //外循环, 用来获取每一个班级的.
                //2. 再次通过for循环获取到当前班级中的每一位同学.
                for(int i = 1; i <= 5; i++) {   //内循环, 用来获取当前班级的每一位学生的.
                    //3. 直接打印该学生的信息即可.
                    System.out.println("正在获取第"+ a +"个班级的第" + i + "名同学");
                }
                System.out.println();  //作用: 换行
            }
        }
    }
    ```

    

#### 9.标号的概述

- 标号的概念

  - 即循环的名称。给循环定义一个标号，就可以根据需要结束或跳转到指定循环，常用于多层嵌套循环中

- 语法格式：

  ```
  标号: for()｛｝ // while和do…while举例略
  break 标号; // 结束指定标号的循环
  continue 标号; // 跳转到指定标号的循环继续执行
  ```

- 标号案例：break 标号；

  - 需求：

    - 程序猿同学受邀加入A公司，现按班级查找程序猿同学。现有3个班级，每班10个同学，假设第2个班级的第10位同学 名叫程序猿，找到该同学后则停止查找。

  - 分析：

    - A：先使用for循环遍历每一个班级，定义标号： label_class: for () { } 
    - B：在班级循环体中，再使用for循环遍历每个同学
    - C：判断如果班级编号为2，同学编号为10，则停止查找：break label_class;

  - 代码演练：

    ```
    public class BreakDemo2 {
        public static void main(String[] args) {
            /*
                需求: 程序猿同学受邀加入A公司，现按班级查找程序猿同学。
                已知:
                    现有3个班级，每班10个同学，
                    假设第2个班级的第5位同学名叫程序猿，找到该同学后则停止查找。
            */
            //1. 通过for循环, 获取到每一个班级.
            label_class:for (int i = 1; i < 4; i++) {       //需求: 外循环, 是用来获取到每一个班级的.
                //2. 在班级循环中, 再次通过for循环获取到每一个学生的信息.
                for (int j = 1; j < 11; j++) {  //需求: 内循环, 是用来获取每一个学生的.
                    //3. 打印当前学生的信息.
                    System.out.println("正在查找第"+ i +"个班级的第"+ j +"个学生");
                    //4. 判断当前学生是否是 程序猿同学(第2个班级的第5位同学)
                    if(i == 2 && j == 5) {
                        //5. 如果是, 则结束整个循环.
                        System.out.println("哈哈, 找到程序猿同学了, 整个循环结束");
                        break label_class;          //结束指定的循环
                    }
    
                }
                //换行
                System.out.println();
            }
        }
    }
    ```

  

- 标号案例：continue 标号；

  - 需求：

    - 按批次检测商品的次品量。现有3个批次，每个批次有10件商品，如果某批次商品中包含任意一个次品，则该批次商 品不合格，跳过该批次剩余商品的检测并记录，继续下个批次。假设查找到第2个批次的第5件商品为次品。

  - 分析：

    - A：先使用for循环遍历每一个批次，定义标号： label_batch: for () { } 
    - B：在批次循环体中，再使用for循环遍历每 个商品 
    - C：判断如果批次编号为2，商品编号为5，则结束当前批次的检测，继续下个批次： continue label_batch;

  - 代码演练：

    ```
    public class ContinueDemo2 {
        public static void main(String[] args) {
            /*
                需求: 按批次检测商品的次品量。现有3个批次，每个批次有10件商品，
                        如果某批次商品中包含任意一个次品，则该批次商 品不合格，跳过该批次剩余商品的检测并记录，继续下个批次。
                        假设查找到第2个批次的第5件商品为次品。
            */
            //1. 通过for循环, 获取到每一个商品.
            label_class:for (int i = 1; i < 4; i++) {       //需求: 外循环, 是用来获取到每一个商品的.
                //2. 在班级循环中, 再次通过for循环获取到每一个商品的信息.
                for (int j = 1; j < 11; j++) {  //需求: 内循环, 是用来获取每一个商品的.
                    //3. 打印当前的商品.
                    System.out.println("正在查找第"+ i +"批次的第"+ j +"个商品");
                    //4. 判断当前商品是否是 次品(第2个批次的第5件商品为次品)
                    if(i == 2 && j == 5) {
                        //5. 如果是, 则跳过整个循环.
                        System.out.println("找到次品商品, 跳过循环");
                        continue label_class;          //继续指定的循环
                    }
    
                }
                //换行
                System.out.println();
            }
        }
    }
    ```

    
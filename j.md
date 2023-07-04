# 基础语法

## 程序结构

```java
public class MyFirstJavaProgram {
  /*第一个java程序，
  * 它将打印出一个字符串 Hello World
  */
  public static void main(String[] args){
    System.out.println("Hello World"); //打印 Hello World
  }
}
```

## 枚举类型

```java
class FreshJuice {
  enum FreshJuiceSizeP{SMALL, MEDIUM, LARGE}
  FreshJuiceSize size;
}

public class FreshJuiceTest{
  public static void main(String[] args){
    Freshjuice juice = new FreshJuice();
    juice.size = FreshJuice.FreshJuiceSize.MEDIUM;
  }
}
```

## 注释

```java
public MyFirstJavaProgram{
/*
这是一段注释，
这个注释表示：在代码运行时会忽略被/**/，//这个符号标记起来的内容
*/
  public static void main(String[] args){
  //这是一个单行注释，表示被//符号标记内容在代码运行时被忽略
  	System.out.println("Hello World");
	}
}
```

## 编码格式

- 保存文件时，要保存为和控制台一样的编码格式，UTF-8，有中文就保存为GBK

## 课堂练习

##### 写一个老王学习java的程序

```java
public class PrintlnLaoWangStudyJava{
  public static void LaoWangStudyJava(String[] args){
    System.out.println("老王 is studying java");//输出“老王 is studying java”
  }
}
```

## 编译

- ##### 源文件中每一个类，编译后都对应一个class

###### 举例：

```java
public class MyFistJava{
  public static void PrinlnHello(String[] args){
    System.out.println("Hello");
  }
}

//编译后会生成一个Dog.class文件
class Dog{
  
}
//编译后会生成一个Tiger.class文件
class Tiger{
  
}
//截止10:06
```

## chapter2课后作业

##### 作业1

```java
//编写一个hello world程序
public class HelloWorld01(){
  public static void main(String[] args){
    System.put.println("Hello world");
  }
}
//编译：javac HelloWorld01.java
//运行：java HelloWorld.java
```

##### 作业2

```java
//将每个人的基本信息（姓名，性别，籍贯，住址）打印到控制台上输出，每条信息分别占一行
public class HomeWork01(){
  public static void main(String[] args){
    //考察对转义符的使用
    System.out.println("姓名\t年龄\t籍贯\t住址\n顺平\t男\t四川\t北京");
  }
}
//javac HomeWorld01.java
//java HomeWorld01.class
```

##### 作业3

```java
//JDK，JRE，JVM的关系
public class HomeWorld03(){
  public static void main(String[] args){
    System.out.println("答：1、JDK = JRE + java开发工具\n2、JRE = JVM + 核心内库");
  }
}
```

##### 作业4

```java
//环境变量path配置及其作用
public class HomeWorld04(){
  public static void main(String[] args){
    System.out.println("1、环境变量的作用是为了在dos的任意目录，可以去使用java 和 javac\n2、先配置 JAVA_HOME = 指向JDK安装的主目录\n3、编辑path环境，增加 %JAVA_HOME%\bin");
  }
}
```

## 数据类型

### 基本数据类型

- ##### 整数数据类型，存放整数（byte(1),short(2),int(4),long(8)）

```java
//整数类型
public class IntDetail(){
  public static void main(String[] args){
    int n1 = 1; //4个字节
    int n2 = 1L; //编译报错，1L是long，8个字节，n2是是int类型，是4个字节，所以放不下
    long n3 = 1L；//对喽
      //定义数据类型是，尽量使用小的数据类型
      //复习：1个byte=8个bit
    System.out.println();
  }
}
```

- ##### 浮点类型，存放小数（float(4),double(8)）

```java
//浮点类型
public class FloatDetail(){
  public static void main(String[] args){
    //float 4个字节，double 8个字节
    //浮点类型常量默认是8个字节，申明float型常量，需在后加‘f’或‘F’
    //float num1 = 1.1; //编译时会报错
    float num1 = 1.1f; //正确
    double num1 = 1.1; //正确
    double num = 1.1f; //正确
    //科学计数法形势，5.12e2等价于5.12*10的2次方，5.12e-2等价于5.12除以10的2次方
    System.out.println(5.12E2); //512.0
    System.out.println(5.12E-2); //0.0512
    
    //通常情况下，应该使用double型，因为它比float型更精确
    double num9 = 2.1234567891;
    float num10 = 2.1234567891F;
    System.out.println(num9);
    System.out.println(num10);
    
    //浮点数使用陷阱：2.7和8.1/3，比较
    double num11 = 2.7;
    double num12 = 8.1 / 3;
    System.out.println(num11);//2.7
    System.out.println(num12);//接近2.7的一个小数，而不是2.7
    //注意：当对运算结果进行判断时，要小心
    //应该是以两个数的差值的绝对值，在某个进度范围内判断
    if(num11 == num12){//错误写法
       System.out.println("相等");
    }
    //正确写法
    if(Math.abs(num11 - num12) < 0.000001 ){
    }
    System.out.println(Math.abs(num11 - num12));
    //细节：如果是直接查询得到的小数或者直接赋值，是可以判断相等的
    //比如
    //double num = 2.7;
    //double num1 = 2.7;
  }
}
```

- ##### 插播：Java API文档

```java
https://www.matools.com/api
https://www.runoob.com/manual/jdk11api/index.html
//在线结构图地址
https://www.iodraw.com/diagram/
```

- ##### 字符型（char(2)）,存放单个字符，比如‘a’

```java
//小细节1
public class VarDetail(){
  public static void main(String[] args){
    char c1 = 'a';
    char c2 = '\t';
    char c3 = '韩';
    char c3 = 97;
    System.out.println(c1);
    System.out.println(c2);
    System.out.println(c3);
    System.out.println(c4);//当输出C4的时候，会输出97所代表的字符 =》编码表
  }
}
```

```java
//小细节2
public class CharDetail(){
  public static void main(String[] args){
    char c1 = 97;
    System.out.println(cl); // a
    char c2 = 'a';//输出‘a’对应的数字
    System.out.println((int)c2); //97
    char c3 = '韩';
    System.out.println((int)c3);//38889
    char c4 = 38889;
    System.out.println(c4); //韩
    
    //char 类型可以进行运算，相当于一个整数，因为它都对应有Unicode码
    System.out.println('a'+10); //107
    
    //练习
    char c5 = 'b' + 1;
    System.out.println((int)c5);//99
    System.out.println(c5);//99对应的字符 c
  }
}
```

- ##### 布尔型（boolean(1)）,存放true，false

### 引用数据类型

- ##### 类（class)

- ##### 接口（interface）

- ##### 数组（[]）


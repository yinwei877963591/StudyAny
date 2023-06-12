# 基础语法

### 程序结构

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

### 枚举类型

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

### 注释

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

### 编码格式

- 保存文件时，要保存为和控制台一样的编码格式，UTF-8，有中文就保存为GBK

### 课堂练习

##### 写一个老王学习java的程序

```java
public class PrintlnLaoWangStudyJava{
  public static void LaoWangStudyJava(String[] args){
    System.out.println("老王 is studying java");//输出“老王 is studying java”
  }
}
```

### 编译

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

#### chapter2课后作业

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


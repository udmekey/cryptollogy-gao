## 1.java开发细节

- 程序的执行入口是main方法，有固定的书写：pubilc static void main(String[] args){...}
- java严格区分大小写。
- 也可以将main方法写在非public类当中。
- 一个源文件只能有一个public类，其他类个数不限。每一个类编译后都会对应一个class文件。
- 如果源文件包含一个public类，则文件名必须一致。

## 2.变量 ##

- 变量三要素：变量=变量名+数据类型+值。

- 变量表示内存当中的一个存储区域。类型不同，占用空间大小不同。

- 变量需要先声明再使用。

- 同一区域内变量不能重名。

  

## 3.数据类型

### 基本数据类型

#### 数值型

1. 整数类型（byte[1],short[2],int[4],long[8]）
2. 浮点类型（folat[4],double[8]）

#### 字符型（char[2]）

#### 布尔型（boolean[1]true,false）

### 引用类型

1. 类class
2. 接口interface
3. 数组[]

### 使用细节

1. java各整数类型有固定的范围和字段长度，不受OS的影响，来保证java程序的可移植性。
2. java整型常量默认int类型，声明long类型常量后需加‘l'或’L'
3. java变量常声明为int类型，不足才使用long.
4. java浮点常量默认为double类型，声明folat需加‘f'或'F'.

### 浮点数使用陷阱

2.7，8.1/3=2.66666669
注意对运算结果是小数进行相等判断时要小心。应用两个数的差值的绝对值比较，在某个精度范围内判断。
Math.abs(num1-num2)

### 自动类型转换

char[2]-->int[4]-->long[8]-->folat[4]-->double[8]

byte[1]-->short[2]-->int[4]-->long[8]-->folat[4]-->double[8]

byte,short,char之间不会自动转换。三者在运算时当作int类型处理。
boolean不参与转换。

## 4.算术运算

1. byte,short,char，三者在运算时当作int类型处理。
2. 复合运算a+=3;等价于a=a+3;
3. 复合运算会进行类型转换。

#### i++与++i

int i=1;	temp=i;i=i+1;i=temp;
i=i++;
system.out.println(i);1

int i=1;	i=i+1;temp=i;i=temp;
i=++i;
system.out.println(i);2

#### 三元运算符

int c=a>b?a:b 
表达式1和2要为可以赋值给变量的类型（可以自动转换）
可以转换为if-else语句

#### 程序中加号的使用

1. 左右两边都为数值型时，+做加法运算；
2. 左右两边有一边为字符串，则做拼接运算。
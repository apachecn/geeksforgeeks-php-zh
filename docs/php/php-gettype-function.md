# PHP|gettype()函数

> Original: [https://www.geeksforgeeks.org/php-gettype-function/](https://www.geeksforgeeks.org/php-gettype-function/)

Gettype()函数是 PHP 中的一个内置函数，用于获取变量的类型。 用于检查现有变量的类型。

**语法：**

```
string gettype ( $var )

```

**参数：**此函数接受单个参数*$var*。 需要检查变量类型的变量名称。

**返回值：**此函数返回字符串类型值。 返回字符串的可能值为：

*   Boolean
*   Integer number
*   DOUBLE (for historical reasons, return "DOUBLE" if it is floating point)
*   String
*   Array
*   Object
*   Resources
*   无约束力的 / 无效的
*   Unknown type

下面的程序演示了 PHP 中的 gettype()函数：

**程序 1：**

```
<?php
// PHP program to illustrate gettype() function

$var1 = true; // boolean value 
$var2 = 3; // integer value
$var3 = 5.6; // double value
$var4 = "Abc3462"; // string value
$var5 = array(1, 2, 3); // array value
$var6 = new stdClass; // object value
$var7 = NULL; // null value
$var8 = tmpfile(); // resource value

echo gettype($var1)."\n";
echo gettype($var2)."\n";
echo gettype($var3)."\n";
echo gettype($var4)."\n";
echo gettype($var5)."\n";
echo gettype($var6)."\n";
echo gettype($var7)."\n";
echo gettype($var8)."\n";

?>
```

**输出：**

```
boolean
integer
double
string
array
object
NULL
resource

```

**程序 2：**

```
<?php

// PHP program to illustrate gettype() function

$var1 = "GfG"; 
$var2 = 10 % 7;
$var3 = pow(10, 2);
$var4 = pow(10, 0.5);
$var5 = sqrt(9);

echo gettype($var1)."\n";
echo gettype($var2)."\n";
echo gettype($var3)."\n";
echo gettype($var4)."\n";
echo gettype($var5);
?>
```

**输出：**

```
string
integer
integer
double
double

```

**引用：**[http://php.net/manual/en/function.gettype.php](http://php.net/manual/en/function.gettype.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
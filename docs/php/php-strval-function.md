# PHP|strval()函数

> Original: [https://www.geeksforgeeks.org/php-strval-function/](https://www.geeksforgeeks.org/php-strval-function/)

Strval()函数是 PHP 中的内置函数，用于将任何标量值(字符串、整数或双精度)转换为字符串。 我们不能对数组或对象使用 strval()，如果应用此函数，则此函数仅返回要转换的值的类型名称。

**语法**：

```
strval( $variable ) 
```

**参数**：此函数接受单个参数*$变量*。 此参数表示要转换为字符串的值

**返回值**：此函数返回一个字符串。 此字符串是通过对作为参数传递给它的变量的值进行类型转换而生成的。

下面的程序演示了 strval()函数。

**程序 1**：

```
<?php

$var_name = 32.360;

// prints the value of above variable 
// as a string
echo strval($var_name);

?>
```

产出：

```
32.36

```

**程序 2**：

```
<?php

class geeksforgeeks
{
    public function __toString()
    {   
        // returns the class name 
        return __CLASS__;
    }
}

// prints the name of above class as
// a string
echo strval(new geeksforgeeks);

?>
```

产出：

```
geeksforgeeks

```

**程序 3**：

```
<?php
// Program to illustrate the strval() function
// when an array is passed as parameter

// Input array
$arr = array(1,2,3,4,5);

// This will print only the type of value
// being converted i.e. 'Array'
echo strval($arr);

?>
```

**参考**：
[http://php.net/manual/en/function.strval.php](http://php.net/manual/en/function.strval.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
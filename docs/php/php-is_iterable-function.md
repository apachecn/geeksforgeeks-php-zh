# PHP|is_iterable()函数

> Original: [https://www.geeksforgeeks.org/php-is_iterable-function/](https://www.geeksforgeeks.org/php-is_iterable-function/)

**is_iterable()函数**是 PHP 中的一个内置函数，用于检查变量的内容是否为可迭代值。

**语法：**

```php
*bool* is_iterable( *mixed* $var )
```

**参数：**此函数接受单个参数，如上所述，如下所述：

*   **$var:** it contains the value of the variable to check.

**返回值：**如果变量的值是可迭代的，则返回 TRUE，否则返回 FALSE。

**程序 1：**

```php
<?php

// Declare an array
$arr = array(1, 2, 3, 4, 5);

if(is_iterable($arr)) {
    echo "Array is iterable";
}
else {
    echo "Array is not iterable";
}

// Create a class
class GFG {
}

// Create an object
$obj = new GFG();

if(is_iterable($obj)) {
    echo "\nObject is iterable";
}
else {
    echo "\nObject is not iterable";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a class
class GFG {
    public $Geek_name = "Welcome to GeeksforGeeks"; 
}

$obj = new GFG();
var_dump(is_iterable($obj));

$arr = array('G', 'e', 'e', 'k', 's');
var_dump(is_iterable($arr));

$num = 25;
var_dump(is_iterable($num));

$str = "GeeksforGeeks";
var_dump(is_iterable($str));

$bool = true;
var_dump(is_iterable($bool));
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.is-iterable.php](https://www.php.net/manual/en/function.is-iterable.php)
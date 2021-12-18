# PHP|is_object()函数

> Original: [https://www.geeksforgeeks.org/php-is_object-function/](https://www.geeksforgeeks.org/php-is_object-function/)

**is_object()函数**是 PHP 中的一个内置函数，用于检查给定值是否为对象。

**语法：**

```
*bool* is_object( *mixed* $var )
```

**参数：**此函数接受单个参数，如上所述，如下所述：

*   **$var:** it contains the value of the variable to check.

**返回值：**如果变量的值是对象，则返回 TRUE，否则返回 FALSE。

**程序 1：**

```
<?php

// Create a class
class GFG {

    public $data1; 
    public $data2; 
    public $data3; 
}

// Create an object
$obj = new GFG();

// Check the value of variable
// is an object or not
if(is_object($obj)) {
    echo "Object";
}
else {
    echo "Not Object";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a class
class GFG {
    public $Geek_name = 
          "Welcome to GeeksforGeeks"; 
} 

// Create the class name alias
class_alias('GFG', 'GeeksforGeeks');

$obj1 = new GFG();
$obj2 = new GeeksforGeeks();
$obj3 = 'GeeksforGeeks';

var_dump(is_object($obj1));
var_dump(is_object($obj2));
var_dump(is_object($obj3));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.is-object.php](https://www.php.net/manual/en/function.is-object.php)
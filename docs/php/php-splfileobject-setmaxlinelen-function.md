# PHP|SplFileObject setMaxLineLen()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-setmaxlinelen-function/](https://www.geeksforgeeks.org/php-splfileobject-setmaxlinelen-function/)

SplFileObject：：setMaxLineLen()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于设置最大行长。

**语法：**

```php
*void* SplFileObject::setMaxLineLen( $len )
```

**参数：**此函数接受单个参数*$len*，该参数用于指定行的最大长度。

**返回值：**此函数返回行的最大长度。 默认值为 0。

下面的程序演示了 PHP 中的 SplFileObject：：setMaxLineLen()函数：

**程序 1：**

```php
<?php

// Create an SplFile Object
$gfg = new SplFileObject("gfg.txt");

// Print Length
var_dump($gfg->getMaxLineLen());

// Set length 
$gfg->setMaxLineLen(20);
var_dump($gfg->getMaxLineLen());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create an Array
$GFG = array(
    "dummy.txt",
    "gfg.txt",
    "frame.txt"
    );

// Creating Spl Object
foreach ($GFG as &$arr) 
{
    // Create an SplFile Object
    $gfg = new SplFileObject($arr);

    // Print Length before
    var_dump($gfg->getMaxLineLen());

    // Set length 
    $gfg->setMaxLineLen(50);
    echo "After = ";
    // Print length after
    var_dump($gfg->getMaxLineLen());

    echo "</br>";
    }
?>
```

**输出：**

```php
int(0) After = int(50) 
int(0) After = int(50) 
int(0) After = int(50) 

```

**引用：**[http://php.net/manual/en/splfileobject.setmaxlinelen.php](http://php.net/manual/en/splfileobject.setmaxlinelen.php)
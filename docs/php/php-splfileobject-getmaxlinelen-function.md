# PHP|SplFileObject getMaxLineLen()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-getmaxlinelen-function/](https://www.geeksforgeeks.org/php-splfileobject-getmaxlinelen-function/)

SplFileObject：：getMaxLineLen()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取最大行长。

**语法：**

```
*int* SplFileObject::getMaxLineLen( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回行的最大长度。 默认值设置为 0。

下面的程序演示了 PHP 中的 SplFileObject：：getMaxLineLen()函数：

**程序 1：**

```
<?php

// Create an SplFile Object
$file = new SplFileObject("gfg.txt");

// Print Length
var_dump($file->getMaxLineLen());

// Create an SplFile Object
$file = new SplFileObject(__FILE__);

// Print Length
var_dump($file->getMaxLineLen());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
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

**输出：**

```
int(0) int(20)

```

**引用：**[http://php.net/manual/en/splfileobject.getmaxlinelen.php](http://php.net/manual/en/splfileobject.getmaxlinelen.php)
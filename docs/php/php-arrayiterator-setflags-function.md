# PHP | ArrayIterator setFlags()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-setflags-function/](https://www.geeksforgeeks.org/php-arrayiterator-setflags-function/)

**ArrayIterator::setFlags()函数**是 PHP 中的一个内置函数，用于设置标志的行为。
**语法:**

```
*void* ArrayIterator::setFlags( *string* $flags )
```

**参数:**该函数接受单个参数 **$flags** ，该参数保存新的数组运算符行为。
**返回值:**该功能不返回值。
下面的程序说明了 PHP 中的 ArrayIterator::setFlags()函数:
**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

// Set the flags
$arrItr->setFlags(ArrayIterator::STD_PROP_LIST);

// Display the result
var_dump($arrItr->getFlags());

?>
```

**Output:** 

```
int(1)
```

**节目 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => "Geeks",
        "b" => "for",
        "c" => "Geeks"
    )
);

// Append some elements
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Set the flags
$arrItr->setFlags(ArrayIterator::ARRAY_AS_PROPS);

// Get the flags
var_dump($arrItr->getFlags());

?>
```

**Output:** 

```
int(2)
```

**参考:**T2https://www.php.net/manual/en/arrayiterator.setflags.php
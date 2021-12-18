# PHP|Imagick listRegistry()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-listregistry-function/](https://www.geeksforgeeks.org/php-imagick-listregistry-function/)

**Imagick：：listRegistry()函数**是 PHP 中的一个内置函数，用于列出所有注册表设置。

**语法：**

```
*array* Imagick::listRegistry( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回注册表中所有键/值对的数组。

下面的程序演示了 PHP 中的 Imagick：：listRegistry()函数：

**程序：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Setting the ImageMagick registry
$imagick->setRegistry('key1', 'value1');
$imagick->setRegistry('key2', 'value2');

// Getting all the ImageMagick registry
$regs = $imagick->listRegistry();

// Displaying the array
foreach($regs as $key => $value) {
    echo "$key => $value";
    echo nl2br("\n");
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.listregistry.php](https://www.php.net/manual/en/imagick.listregistry.php)
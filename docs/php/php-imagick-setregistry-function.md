# PHP|Imagick setRegistry()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setregistry-function/](https://www.geeksforgeeks.org/php-imagick-setregistry-function/)

**Imagick：：setRegistry()函数**是 PHP 中的一个内置函数，用于将命名项为 value 的 ImageMagick 注册表项设置为值。 此函数可用于设置“临时路径”，该路径用于控制 ImageMagick 创建临时映像的位置。

**语法：**

```
*bool* Imagick::setRegistry( *string* $key, *string* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$key:** this parameter saves entries in the registry.
*   **$Value:** this parameter holds the value of the registry.

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的 Imagick：：setRegistry()函数：

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

**引用：**[https://www.php.net/manual/en/imagick.setregistry.php](https://www.php.net/manual/en/imagick.setregistry.php)
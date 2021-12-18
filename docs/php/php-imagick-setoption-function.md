# PHP|Imagick setOption()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setoption-function/](https://www.geeksforgeeks.org/php-imagick-setoption-function/)

**Imagick：：setOption()函数**是 PHP 中的内置函数，用于设置选项。

**语法：**

```php
*bool* Imagick::setOption( *string* $key, *string* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$key：**它指定选项的密钥。
*   **$value：**它指定与键关联的值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setOption()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imagick->setImageFormat('jpg');

// Set the option
$imagick->setOption('jpeg:extent', 90);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/b031c3dd35833bcbe817d6c7df2b49d8.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the option
$imagick->setOption('key1', 'option1');

// Get the option with key 'key1'
$option = $imagick->getOption('key1');
echo $option;
?>
```

发帖主题：Re：Колибри0.7.0

```php
option1
```

**引用：**[https://www.php.net/manual/en/imagick.setoption.php](https://www.php.net/manual/en/imagick.setoption.php)
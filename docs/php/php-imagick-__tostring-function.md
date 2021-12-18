# PHP|Imagick__toString()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-__tostring-function/](https://www.geeksforgeeks.org/php-imagick-__tostring-function/)

**Imagick：：__toString()函数**是 PHP 中的一个内置函数，用于将图像作为字符串返回。 此函数将仅返回单个图像，不应用于包含多个图像的 Imagick 对象。

**语法：**

```php
*string* Imagick::__toString( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数以字符串形式返回当前图像。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：__toString()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert it into string
$string = $imagick->__toString();
echo $string;
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will display a large text which is the string form of image.
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert it into string
$string = $imagick->__toString();

// Show the output from string
header("Content-Type: image/png");
echo $string;
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/imagick.tostring.php](https://www.php.net/manual/en/imagick.tostring.php)
# PHP|Imagick IdentifyImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-identifyimage-function/](https://www.geeksforgeeks.org/php-imagick-identifyimage-function/)

**Imagick：：IdentifyImage()**函数是 PHP 中的内置函数，用于标识图像并返回其属性。 属性包含图像宽度、高度、大小等。
**语法：**和

```php
*array* Imagick::identifyImage( $appendRawOutput )
```

**参数：**此函数接受单个参数*$appendRawOutput*，该参数用于存储值 true/false。 如果它设置为 true，则原始输出将附加到数组中。
**返回值：**此函数返回图像属性。
**原图：**和

![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

下面的程序说明了 PHP：
**程序 1：**和
中的**Imagick：：IdentifyImage()**函数

## PHP

```php
<?php

// require_once('path/vendor/autoload.php');

// Create an Imagick Object
$imagick = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Use identifyImage Function
var_dump ($imagick->identifyImage());
?>
```
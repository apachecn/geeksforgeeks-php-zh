# PHP|Imagick getImageUnits()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageunits-function/](https://www.geeksforgeeks.org/php-imagick-getimageunits-function/)

**Imagick：：getImageUnits()**函数是 PHP 中的内置函数，用于获取特定图像的分辨率单位。
**语法：**和

```php
*int* Imagick::getImageUnits( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回图像分辨率单位的整数。
下面的程序说明 PHP：
**程序 1：**和
**原始图像：**和
中的**Imagick：：getImageUnits()**函数

![](img/efa5ea8e0258291fa60ad9a32c288072.png)

## PHP

```php
<?php

// PHP program to illustrate getimageunits function
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageUnits Function
$unit = $image->getImageUnits();

// Display the output
echo "</br>units = ";
print_r($unit);
?>
```
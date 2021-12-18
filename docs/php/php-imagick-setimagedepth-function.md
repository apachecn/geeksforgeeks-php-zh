# PHP|Imagick setImageDepth()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagedepth-function/](https://www.geeksforgeeks.org/php-imagick-setimagedepth-function/)

**Imagick：：setImageDepth()**函数是 PHP 中的内置函数，用于设置特定图像的深度。
**语法：**和

```
*bool* Imagick::setImageDepth( $depth )
```

**参数：**此函数接受单个参数*$Depth*，该参数是一个整数值，用于设置图像的深度。
**返回值：**如果成功，此函数返回 TRUE。
下面的程序说明了 PHP：
**原始图像：**和
中的**Imagick：：setImageDepth()**函数

![](img/efa5ea8e0258291fa60ad9a32c288072.png)

**程序 1：**和

## PHP

```
<?php

// require_once('path/vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageDepth function to find the depth
// of image
$res= $image->getImageDepth();

// Display the depth of image
echo "Previous Depth" . $res;

$image->setImageDepth(20);

$res = $image->getImageDepth();
echo "</br>After Set Depth" . $res;
?>
```
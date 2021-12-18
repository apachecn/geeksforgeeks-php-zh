# PHP|Imagick setImageUnits()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageunits-function/](https://www.geeksforgeeks.org/php-imagick-setimageunits-function/)

**Imagick：：setImageUnits()**函数是 PHP 中的内置函数，用于设置特定图像的分辨率单位。
**语法：**和

```
*bool* Imagick::setImageUnits( $units )
```

**参数：**此函数接受单个参数*$units*，该参数用于指定要为图像设置的单位。*
**分辨率常量：**Imagick：：setImageUnits()函数设置图像单位，如下所述：{

*   Imagick：：RESOLUTION_UNDEFINED(整数)，单位=0
*   Imagick：：RESOLUTION_PIXELSPERINCH(整数)，单位=1
*   Imagick：：RESOLUTION_PIXELSPERCENTIMETER(integer)，单位=2

**返回值：**成功时此函数返回 True。
**原图：**和

![](img/efa5ea8e0258291fa60ad9a32c288072.png)

下面的程序说明 PHP：
**程序 1：**和
中的**Imagick：：setImageUnits()**函数

## PHP

```
<?php

// PHP program to illustrate
// seImageUnits function
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageUnits function
$units = $image->getImageUnits();
echo "units Before SetUnit = ";
print_r($units);

// set image unit = 1
$image->setImageUnits(1);

// Display the output
$units = $image->getImageUnits();
echo "</br>units After Set = ";
print_r($units);

?>
```

发帖主题：Re：Колибри0.7.8.0

```
units Before SetUnit = 2
units After Set = 1
```

**程序 2：**和

## PHP

```
<?php
$i = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

$r = $i->getImageResolution();
$u = $i->getImageUnits();
echo "print previous resolution = ";
print_r($r);

// print units
echo "</br>Check units  = ";
print_r($u);

// for units are based on below resolution
//0=undefined, 1=pixelsperInch, 2=PixelsPerCentimeter

// checking if units = 2
// then set unit = 1
if ($u == Imagick::RESOLUTION_PIXELSPERCENTIMETER) {
   $r[x] = (int)round($r[x] * 2);
   $r[y] = (int)round($r[y] * 2);
   $i->setImageUnits(Imagick::RESOLUTION_PIXELSPERINCH);
   $i->setImageResolution($r[x], $r[y]);

  //note that the number type is double again
   $r = $i->getImageResolution();
}

// print resolution after
echo "</br>resolution after ";
print_r($r);

$u = $i->getImageUnits();

echo "</br>units After Set  = ";
print_r($u);
?>
```

发帖主题：Re：Колибри0.7.8.0

```
print previous resolution = Array ( [x] => 37.8 [y] => 37.8 )
Check units = 2
resolution after Array ( [x] => 76 [y] => 76 )
units After Set = 1
```

**引用：**[http://php.net/manual/en/imagick.setimageunits.php](http://php.net/manual/en/imagick.setimageunits.php)
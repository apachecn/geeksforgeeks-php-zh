# PHP|Imagick setImageFilename()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagefilename-function/](https://www.geeksforgeeks.org/php-imagick-setimagefilename-function/)

**Imagick：：setImageFilename()函数**是 PHP 中的一个内置函数，用于设置特定图像的文件名。

**语法：**

```php
*bool* Imagick::setImageFilename( *string* $filename )
```

**参数：**此函数接受单个参数**$filename**，该参数保存表示文件名的字符串。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageFilename()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Filename
$imagick->setImageFilename('myNewFilename.png');

// Get the Filename
$name = $imagick->getImageFilename();
echo $name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Filename
$imagick->setImageFilename('myAnotherNewFilename.png');

// Get the Filename
$name = $imagick->getImageFileName();

// Write the image to same folder
$imagick->writeImage($name);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimagefilename.php](https://www.php.net/manual/en/imagick.setimagefilename.php)
# PHP|Imagick getImageProfile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageprofile-function/](https://www.geeksforgeeks.org/php-imagick-getimageprofile-function/)

**Imagick：：getImageProfile()函数**是 PHP 中的一个内置函数，用于返回命名的图像配置文件。

**语法：**

```php
*string* Imagick::getImageProfile( *string* $name )
```

**参数：**此函数接受保存配置文件名称的单个参数**$name**。

**返回值：**此函数返回包含图像配置文件的字符串。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：getImageProfile()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Profile
$imagick->setImageProfile('profile_name', 'profile_data');

// Get the Image Profile
$profile = $imagick->getImageProfile('profile_name');

echo $profile;
?>
```

发帖主题：Re：Колибри0.7.0

```php
profile_data
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Profile
$imagick->setImageProfile('color', 'red');

// Use the Image Profile
$imagick->setImageBackgroundColor($imagick->getImageProfile('color'));
$imagick->setImageAlphaChannel(Imagick::ALPHACHANNEL_SHAPE);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/e051b0bb8394856bfab829b0d3fbe6c9.png)

**引用：**[https://www.php.net/manual/en/imagick.getimageprofile.php](https://www.php.net/manual/en/imagick.getimageprofile.php)
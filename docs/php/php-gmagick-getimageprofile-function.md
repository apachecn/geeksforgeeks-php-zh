# PHP|Gmagick getimageprofile()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageprofile-function/](https://www.geeksforgeeks.org/php-gmagick-getimageprofile-function/)

**gmagick：：getimageprofile()函数**是 PHP 中的一个内置函数，用于获取命名的图像配置文件。

**语法：**

```php
*string* Gmagick::getimageprofile( *string* $name )
```

**参数：**此函数接受保存配置文件名称的单个参数**$name**。

**返回值：**此函数返回包含 Profile 的值的字符串值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageprofile()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image profile
$gmagick->setimageprofile('profile_name', 'profile_value');

// Get the image profile
$profile = $gmagick->getimageprofile("profile_name");
echo $profile;
?>
```

发帖主题：Re：Колибри0.7.0

```php
profile_value
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the blur using image profile 
$gmagick->setImageProfile('blur', '10'); 

// Use the image profile 
$gmagick->blurimage($gmagick->getImageProfile('blur'), 9); 

// Display the image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/f41d33c7af031b9411f769d86305c8a1.png)

**引用：**[https://www.php.net/manual/en/gmagick.getimageprofile.php](https://www.php.net/manual/en/gmagick.getimageprofile.php)
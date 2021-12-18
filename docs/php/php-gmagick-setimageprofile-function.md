# PHP|Gmagick setimageprofile()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimageprofile-function/](https://www.geeksforgeeks.org/php-gmagick-setimageprofile-function/)

**gmagick：：setimageprofile()函数**是 PHP 中的一个内置函数，用于将命名配置文件添加到 Gmagick 对象。

**语法：**

```
*Gmagick* Gmagick::setimageprofile( *string* $name, *string* $profile )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**它指定配置文件的名称。
*   **$profile：**它指定配置文件的值。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimageprofile()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
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

```
profile_value
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the color using image profile
$gmagick->setImageProfile('color', 'blue');

// Use the image profile
$gmagick->borderimage($gmagick->getimageprofile('color'), 5, 5);

// Display the image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/5aa5a594c98ebe0783c38365d1ad3111.png)

**引用：**[https://www.php.net/manual/en/gmagick.setimageprofile.php](https://www.php.net/manual/en/gmagick.setimageprofile.php)
# PHP|Imagick setImageProfile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageprofile-function/](https://www.geeksforgeeks.org/php-imagick-setimageprofile-function/)

**Imagick：：setImageProfile()函数**是 PHP 中的一个内置函数，用于将命名配置文件设置为 Imagick 对象。

**语法：**

```
*bool* Imagick::setImageProfile( *string* $name, *string* $profile )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**它指定配置文件的名称。
*   **$profile：**它指定配置文件的值。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageProfile()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Profile
$imagick->setImageProfile('color', 'cyan');

// Use the Image Profile
$imagick->setImageBackgroundColor($imagick->getImageProfile('color'));
$imagick->setImageAlphaChannel(Imagick::ALPHACHANNEL_SHAPE);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/e2e5e30552636e68b7f6b5e53967b7bd.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Image Profile
$imagick->setImageProfile('borderColor', 'green');

// Use the Image Profile
$imagick->borderImage($imagick->getImageProfile('borderColor'), 1, 1);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/805a3d863c9ea82a3a051eccfc094056.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageprofile.php](https://www.php.net/manual/en/imagick.setimageprofile.php)
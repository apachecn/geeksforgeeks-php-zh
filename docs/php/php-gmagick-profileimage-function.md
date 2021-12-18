# PHP|Gmagick profileimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-profileimage-function/](https://www.geeksforgeeks.org/php-gmagick-profileimage-function/)

**gmagick：：profileimage()函数**是 PHP 中的一个内置函数，用于在图像中添加或删除配置文件。

**语法：**

```
*Gmagick* Gmagick::profileimage( *float* $name, *float* $profile )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**它指定配置文件的名称。
*   **$profile：**它指定配置文件的值。

**返回值：**此函数返回带有配置文件的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：profileimage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(添加配置文件)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Add profile to the image
$gmagick->profileimage('my_profile_name', 'my_profile_value');

// Output the image  
echo $gmagick->getimageprofile('my_profile_name'); 
?>
```

发帖主题：Re：Колибри0.7.0

```
my_profile_value
```

**程序 2(删除配置文件)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Add profile to the image
$gmagick->profileimage('my_profile_name', 'my_profile_value');

// Remove all profiles
$gmagick->profileimage('*', NULL);

try {
    $profileValue = $gmagick->getimageprofile('my_profile_name'); 
} catch (\Throwable $e) {
    echo "No such profile exists";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
No such profile exists
```

**引用：**[https://www.php.net/manual/en/gmagick.profileimage.php](https://www.php.net/manual/en/gmagick.profileimage.php)
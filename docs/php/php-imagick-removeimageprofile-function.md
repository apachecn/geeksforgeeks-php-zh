# PHP|Imagick removeImageProfile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-removeimageprofile-function/](https://www.geeksforgeeks.org/php-imagick-removeimageprofile-function/)

**Imagick：：removeImageProfile()函数**是 PHP 中的一个内置函数，用于删除命名的图像配置文件。

**语法：**

```php
*string* Imagick::removeImageProfile( *string* $name )
```

**参数：**此函数接受保存配置文件名称的单个参数**$name**。

**返回值：**此函数返回包含配置文件的字符串。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：removeImageProfile()函数**：

**程序 1：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add two profiles
$imagick->setImageProfile('name1', 'profile1');
$imagick->setImageProfile('name2', 'profile2');

// Remove the first profile
$imagick->removeImageProfile('name1');

// Get all the profiles
$profile =  $imagick->getImageProfiles('*');
print("<pre>".print_r($profile, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add two profiles
$imagick->setImageProfile('name1', 'profile1');
$imagick->setImageProfile('name2', 'profile2');

// Remove all profiles
$imagick->removeImageProfile('name1');
$imagick->removeImageProfile('name2');

// Get all the profiles
$profile =  $imagick->getImageProfiles('*');
print("<pre>".print_r($profile, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.removeimageprofile.php](https://www.php.net/manual/en/imagick.removeimageprofile.php)
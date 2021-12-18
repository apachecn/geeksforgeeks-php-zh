# PHP|Gmagick setimagefilename()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagefilename-function/](https://www.geeksforgeeks.org/php-gmagick-setimagefilename-function/)

**gmagick：：setimagefilename()函数**是 PHP 中的一个内置函数，用于设置序列中特定图像的文件名。

**语法：**

```php
*Gmagick* Gmagick::setimagefilename( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimagefilename()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the delay
$gmagick->setimagefilename('new_name.png');

// Get the image name
$name = $gmagick->getimagefilename();
echo $name;  
?>
```

发帖主题：Re：Колибри0.7.0

```php
new_name.png
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the delay
$gmagick->setimagefilename('new_name.png');

// Save the image with new name
$gmagick->write($gmagick->getimagefilename());
echo 'Image saved successfully in the folder';
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will save the image with new name in the same folder.
```

**引用：**[https://www.php.net/manual/en/gmagick.setimagefilename.php](https://www.php.net/manual/en/gmagick.setimagefilename.php)
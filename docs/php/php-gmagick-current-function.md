# PHP|Gmagick Current()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-current-function/](https://www.geeksforgeeks.org/php-gmagick-current-function/)

**Gmagick：：Current()函数**是 PHP 中的一个内置函数，用于返回当前 Gmagick 对象的引用。 此函数不创建任何副本，但返回相同的 Gmagick 实例。

**语法：**

```php
*Gmagick* Gmagick::current( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：Current()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create two new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');
$gmagicknew = new Gmagick();

// Get the current object
$gmagicknew = $gmagick->current();

// Output the new Gmagick object image to browser
header('Content-type: image/png');  
echo $gmagicknew;  
?>  
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```php
<?php

// Create two new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');
$gmagicknew = new Gmagick();

// Get the current object
$gmagicknew = $gmagick->current();

// Apply blur to new object
$gmagicknew->blurimage(20, 2);

// Output the image to browser
header('Content-type: image/png');  
echo $gmagicknew;  
?>  
```

**输出：**
![](img/6d05c3bec480c5329e52659c76ac72b6.png)

**引用：**[https://www.php.net/manual/en/gmagick.current.php](https://www.php.net/manual/en/gmagick.current.php)
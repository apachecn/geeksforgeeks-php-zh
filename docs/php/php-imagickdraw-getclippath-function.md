# PHP|ImagickDraw getClipPath()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getclippath-function/](https://www.geeksforgeeks.org/php-imagickdraw-getclippath-function/)

**ImagickDraw：：getClipPath()函数**是 PHP 中的一个内置函数，用于获取当前剪切路径 ID。

**语法：**

```php
*string* ImagickDraw::getClipPath( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含剪辑路径 ID 的字符串值，如果不存在剪辑路径，则返回 False。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getClipPath()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get clip path
echo $draw->getClipPath();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the clipPath
$draw->setClipPath('sample_name');

// Get clip path
echo $draw->getClipPath();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickdraw.getclippath.php](https://www.php.net/manual/en/imagickdraw.getclippath.php)
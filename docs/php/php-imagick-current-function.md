# PHP|Imagick Current()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-current-function/](https://www.geeksforgeeks.org/php-imagick-current-function/)

Imagick：：Current()函数是 PHP 中的内置函数，用于返回当前 Imagick 对象的引用。 此函数不创建任何副本，但返回 Imagick 的相同实例。

**语法：**

```
*Imagick* Imagick::current( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回 Imagick 对象的实例。

**程序 1：**这个程序是关于 current()方法的简单功能。 它将创建一个具有指向同一实例的新名称的变量，并在新实例的帮助下显示旧变量的内容。

```
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Use Imagick::current() function and
// initialized with Image 
$im1 = $im->current();

// Imagick instance returned in a new variable $im1
header("Content-type: image/png");

// Display image as output
echo $im1;

?>
```

**输出：**
![Output](img/e0a09f626a53f9798548eeec56f207a9.png)

**程序 2：**它使用第二个变量对图像执行模糊操作，更改将反映在第一个变量上，因为这两个变量都指向同一实例。

```
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Use Imagick::current() function
$im1 = $im->current();

// Use Imagick::blurImage() function to blur the image
$im1->blurImage(5, 3);

header("Content-type: image/png");

// Display the image as
echo $im;

?>
```

**输出：**
![Output 2](img/7865a6f508b11a1762a05dbe0ef8c0f9.png)

**引用：**[https://www.php.net/manual/en/imagick.current.php](https://www.php.net/manual/en/imagick.current.php)
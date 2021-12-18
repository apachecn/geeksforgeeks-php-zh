# PHP|Gmagick getimagedelay()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagedelay-function/](https://www.geeksforgeeks.org/php-gmagick-getimagedelay-function/)

**gmagick：：getimagedelay()函数**是 PHP 中的一个内置函数，用于获取图像延迟。 延迟实际上是在 gif 动画中从一个图像过渡到另一个图像所花费的时间。

**语法：**

```php
*int* Gmagick::getimagedelay( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像延迟的整数值，单位为厘米秒(100centi=1 秒)。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagedelay()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif
$gmagickAnimation = new Gmagick('g4gnanimation1.gif');

// Get the delay
$delay = $gmagickAnimation->getimagedelay();
echo $delay;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif
$gmagickAnimation = new Gmagick('g4gnanimation1.gif');

// Set the delay
$gmagickAnimation->setimagedelay(200);

// Get the delay
$delay = $gmagickAnimation->getimagedelay();
echo $delay;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagedelay.php](https://www.php.net/manual/en/gmagick.getimagedelay.php)
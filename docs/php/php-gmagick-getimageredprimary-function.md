# PHP|Gmagick getimageredprimary()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageredprimary-function/](https://www.geeksforgeeks.org/php-gmagick-getimageredprimary-function/)

**gmagick：：getimageredprimary()函数**是 PHP 中的一个内置函数，它返回色度红色基准点。 此函数返回具有键“x”和“y”的关联数组。

**语法：**

```
*array* Gmagick::getimageredprimary( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个包含点的 x 和 y 坐标的数组。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageredprimary()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Use getimageredprimary function 
$res = $gmagick->getimageredprimary(); 
print_r($res); 
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 0.63999998569489 [y] => 0.33000001311302 )
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Use setimageredprimary function
$gmagick->setimageredprimary(4, 8);

// Use getimageredprimary function 
$res = $gmagick->getimageredprimary(); 
print_r($res); 
?> 
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 4 [y] => 8 )
```

**引用：**[https://www.php.net/manual/en/gmagick.getimageredprimary.php](https://www.php.net/manual/en/gmagick.getimageredprimary.php)
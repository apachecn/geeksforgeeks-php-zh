# PHP|Imagick getImageRedPrimary()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageredprimary-function/](https://www.geeksforgeeks.org/php-imagick-getimageredprimary-function/)

**Imagick：：getImageRedPrimary()**函数是 PHP 中的一个内置函数，它返回色度红色基准点。 此函数返回一个具有键“x”和“y”的数组。

**语法：**

```
*array* Imagick::getImageRedPrimary( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个包含点的 x 和 y 坐标的数组。

**异常：**此函数在出错时引发 ImagickException。
下面的程序说明了 PHP 中的**Imagick：：getImageRedPrimary()**函数：

**程序 1：**

```
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use getImageRedPrimary function
$res = $imagick->getImageRedPrimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 0.64 [y] => 0.33 )
```

**程序 2：**

```
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Use setImageRedPrimary function
$imagick->setImageRedPrimary(0.5, 0.8);

// Use getImageRedPrimary function
$res = $imagick->getImageRedPrimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 0.5 [y] => 0.8 )
```

**引用：**[https://www.php.net/manual/en/imagick.getimageredprimary.php](https://www.php.net/manual/en/imagick.getimageredprimary.php)
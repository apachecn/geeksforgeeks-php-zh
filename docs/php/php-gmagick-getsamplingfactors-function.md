# PHP|Gmagick getsamplingfactor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getsamplingfactors-function/](https://www.geeksforgeeks.org/php-gmagick-getsamplingfactors-function/)

**Gmagick：：getsamplingfactor()函数**是 PHP 中的一个内置函数，用于返回水平和垂直采样因子。 采用采样因子对 JPG 进行压缩。 如果未使用*setsamplingfactor()*函数设置此选项，则使用默认的 JPG 采样因子。

**语法：**

```php
*array* Gmagick::getsamplingfactors( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含采样因子值的关联数组。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getsamplingfactor()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image sampling factors
$res = $gmagick->getsamplingfactors();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image sampling factors
$gmagick->setsamplingfactors(array(3, 4, 5));

// Get the image sampling factors
$res = $gmagick->getsamplingfactors();
print("<pre>".print_r($res, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getsamplingfactors.php](https://www.php.net/manual/en/gmagick.getsamplingfactors.php)
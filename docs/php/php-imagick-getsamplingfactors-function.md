# PHP|Imagick getSsamingFtors()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getsamplingfactors-function/](https://www.geeksforgeeks.org/php-imagick-getsamplingfactors-function/)

**Imagick：：getSsamingFtors()函数**是 PHP 中的一个内置函数，用于获取水平和垂直采样因子。

**语法：**

```
*array* Imagick::getSamplingFactors( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回图像的水平和垂直采样因子的关联数组。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getSsamingFtors()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imagick->setSamplingFactors(array('2', '4', '5'));

// Get the Sampling factors
$samplingFactors = $imagick->getSamplingFactors();
print("<pre>".print_r($samplingFactors, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Sampling factors
$samplingFactors = $imagick->getSamplingFactors();
print("<pre>".print_r($samplingFactors, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getsamplingfactors.php](https://www.php.net/manual/en/imagick.getsamplingfactors.php)
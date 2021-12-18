# PHP|Imagick getQuantum()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getquantum-function/](https://www.geeksforgeeks.org/php-imagick-getquantum-function/)

**Imagick：：getQuantum()函数**是 PHP 中的一个内置函数，用于获取整数形式的量子范围。

**语法：**

```php
*int* Imagick::getQuantum( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含量子范围的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getQuantum()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Quantum
$quantum = $imagick->getQuantum();
echo $quantum;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Get the quantum
$quantum = $imagick->getQuantum();
echo $quantum;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getquantum.php](https://www.php.net/manual/en/imagick.getquantum.php)
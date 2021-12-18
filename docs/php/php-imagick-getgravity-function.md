# PHP|Imagick get 重力()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getgravity-function/](https://www.geeksforgeeks.org/php-imagick-getgravity-function/)

**Imagick：：get 重力()函数**是 PHP 中的一个内置函数，用于获取 Imagick 对象的全局重力属性。

**语法：**

```
*int* Imagick::getGravity( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回表示重力常数的整数值。
重力常数列表如下：

*   Imagick：：Grasion_Northwest(1)
*   Imagick：：重力 _ 北(2)
*   想象力：：重力 _ 东北(3)
*   Imagick：：Grasion_West(4)
*   Imagick：：Grasion_Center(5)
*   Imagick：：Grasion_East(6)
*   Imagick：：Grasion_Southwest(7)
*   Imagick：：Grasion_South(8)
*   Imagick：：重力 _ 东南(9)

下面的程序演示了 PHP 中的**Imagick：：get 重力()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Gravity
$gravity = $imagick->getGravity();

echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.0

```
0 // Which means gravity is not set.
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gravity
$imagick->setGravity(3);

// Get the Gravity
$gravity = $imagick->getGravity();

echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.0

```
3 // Which corresponds to *imagick::GRAVITY_NORTHEAST*.
```

**引用：**[https://www.php.net/manual/en/imagick.getgravity.php](https://www.php.net/manual/en/imagick.getgravity.php)
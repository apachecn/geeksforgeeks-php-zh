# PHP|Imagick setImage 重力()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagegravity-function/](https://www.geeksforgeeks.org/php-imagick-setimagegravity-function/)

**Imagick：：setImage 重力()函数**是 PHP 中的一个内置函数，用于设置图像的重力属性。 *setGraality()*和*setImageGrauity()*的区别在于前者应用于整个 Imagick 对象，而后者设置序列中当前图像的重力(如果有多个图像)。

**语法：**

```
*bool* Imagick::setImageGravity( *int* $gravity )
```

**参数：**此函数接受包含整数值的单个参数**$grasion**。
重力常数列表如下：

*   Imagick：：Grasion_Northwest(0)
*   Imagick：：重力 _ 北(1)
*   想象力：：重力 _ 东北(2)
*   Imagick：：Grasion_West(3)
*   Imagick：：Grasion_Center(4)
*   Imagick：：Grasion_East(5)
*   Imagick：：Grasion_Southwest(6)
*   Imagick：：Grasion_South(7)
*   Imagick：：重力 _ 东南(8)

**返回值：**此函数返回布尔值。

下面的程序演示了 PHP 中的**Imagick：：setImage 重力()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gravity
$imagick->setImageGravity(7);

// Get the Gravity
$gravity = $imagick->getImageGravity();
echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.0

```
7
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gravity
$imagick->setImageGravity(3);

// Get the Gravity
$gravity = $imagick->getImageGravity();
echo $gravity;
?>
```

发帖主题：Re：Колибри0.7.0

```
3
```

**引用：**[https://www.php.net/manual/en/imagick.setimagegravity.php](https://www.php.net/manual/en/imagick.setimagegravity.php)
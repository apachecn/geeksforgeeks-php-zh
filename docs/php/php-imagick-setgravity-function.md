# PHP|Imagick set 重力()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setgravity-function/](https://www.geeksforgeeks.org/php-imagick-setgravity-function/)

**Imagick：：set 重力()函数**是 PHP 中的一个内置函数，用于设置 Imagick 对象的全局重力属性。

**语法：**

```php
*bool* Imagick::setGravity( *int* $gravity )
```

**参数：**此函数接受保存 int 值的单个参数**$grasion**。
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

下面的程序演示了 PHP 中的**Imagick：：set 重力()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the Gravity to imagick::GRAVITY_NORTHWEST
$imagick->setGravity(0);

// Write the caption in a image
$imagick->newPseudoImage(800, 350, "caption:GeekforGeeks");

$imagick->floodfillPaintImage("blue", 1, "white", 1, 1, false);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/6cc9b889f4f5bc5925fde61869c43b00.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the Gravity to imagick::GRAVITY_SOUTH
$imagick->setGravity(7);

// Write the caption in a image
$imagick->newPseudoImage(800, 350, "caption:GeekforGeeks");

$imagick->floodfillPaintImage("blue", 1, "white", 1, 1, false);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/70fbee457b1a8f393f812fc0d78e2a6f.png)

**引用：**[https://www.php.net/manual/en/imagick.setgravity.php](https://www.php.net/manual/en/imagick.setgravity.php)
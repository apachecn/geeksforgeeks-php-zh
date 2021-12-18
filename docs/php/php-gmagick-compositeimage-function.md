# PHP|Gmagick positeimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-compositeimage-function/](https://www.geeksforgeeks.org/php-gmagick-compositeimage-function/)

**Gmagick：：CompositeImage()函数**是 PHP 中的一个内置函数，用于在指定的偏移量将一个图像合成到另一个图像上。 偏移实际上是从开始合成第二幅图像的位置开始的距离。

**语法：**

```
*Gmagick* Gmagick::compositeimage( *Gmagick* $source, *int* $COMPOSE, *int* $x, *int* $y )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$source：**它指定要与另一个图像合成的图像的来源。
*   **$Compose：**它指定要应用的合成类型。
*   **$x：**它指定 x 坐标。
*   **$y：**它指定 y 坐标。

**返回值：**此函数返回包含合成图像的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面的程序演示了 PHP 中的**Gmagick：：CompositeImage()函数**：

**程序 1：**此程序使用 Gmagick：：CompositeImage()函数合成两幅没有偏移的图像。

```
<?php

// Create two new Gmagick object
$gmagick1 = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$gmagick2 = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Composite the images with no offset
$gmagick1->compositeimage($gmagick2,
          Gmagick::COMPOSITE_MULTIPLY, 0, 0);

// Output the image  
header('Content-type: image/png');  
echo $gmagick1;  
?>
```

**输出：**
![](img/9728561974e8cefcc0a5b1000519f18d.png)

**程序 2：**此程序使用 Gmagick：：CompositeImage()函数合成两幅带有偏移量的图像。

```
<?php

// Create two new Gmagick object
$gmagick1 = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$gmagick2 = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Composite the images with offset
$gmagick1->compositeimage($gmagick2,
         Gmagick::COMPOSITE_OVER, 300, 0);

// Output the image  
header('Content-type: image/png');  
echo $gmagick1;  
?>  
```

**输出：**
![](img/ae2c09abf9748069c484bfebb36aa311.png)

**引用：**[https://www.php.net/manual/en/gmagick.compositeimage.php](https://www.php.net/manual/en/gmagick.compositeimage.php)
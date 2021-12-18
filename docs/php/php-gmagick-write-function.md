# PHP|Gmagick write()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-write-function/](https://www.geeksforgeeks.org/php-gmagick-write-function/)

**Gmagick：：Write()函数**是 PHP 中的一个内置函数，用于将图像写入指定的文件名。 这是*Gmagick：：WriteImage()*函数的别名。

**语法：**

```php
*Gmagick* Gmagick::write( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 GmagickException。
**使用图像：**捕获画布区域
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**Gmagick：：Write()函数**：

**程序 1：**写入图像。

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Write the image to a local folder
$gmagick->write('my_image_name.png');
echo 'Image saved successfully';
?>
```

**输出：**这将成功保存图像。

```php
Image saved successfully
```

**程序 2：**写入图纸

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('#1bd911');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Write the image to a local folder
$gmagick->write('my_drawing_name.png');
echo 'Image saved successfully';
?>
```

**输出：**这会将图形保存在本地文件夹中。

```php
Image saved successfully
```

**引用：**[https://www.php.net/manual/en/gmagick.write.php](https://www.php.net/manual/en/gmagick.write.php)
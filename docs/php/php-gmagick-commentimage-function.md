# PHP|Gmagick commentImage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-commentimage-function/](https://www.geeksforgeeks.org/php-gmagick-commentimage-function/)

**Gmagick：：CommentImage()**函数是 PHP 中的一个内置函数，用于在图像中添加注释。

**语法：**

```
*Gmagick* Gmagick::commentImage( $comment )
```

**参数：**此函数接受单个参数*$COMMENT*，该参数用于保存注释。

**返回值：**此函数返回添加了注释的 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：CommentImage()**函数：

**程序 1：**
**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

```
<?php 
// require_once('vendor/autoload.php');

// Create an Gmagick Object
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Add comment to the image 
$image->commentImage("GeeksforGeeks");

// Display the comment 
echo $image->getImageProperty("comment");

?>
```

发帖主题：Re：Колибри0.7.0

```
GeeksforGeeks
```

**程序 2：**
**Gmagick 函数创建的图像：**
![](img/112822c4852515d821106cc2ba5aa0b5.png)

```
<?php
$string = "Computer Science portal for Geeks!";

// creating new image of above String
// and add color and background
$im = new Gmagick();
$draw = new GmagickDraw();

// Fill the color in image
$draw->setFillColor(new GmagickPixel('green'));

// Set the text font size
$draw->setFontSize(50);

$metrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($metrix['textWidth'], $metrix['textHeight'],
         new GmagickPixel('white'));

// Draw the image         
$im->drawImage($draw);

// Function to add border image
$im->borderImage(new GmagickPixel('Blue'), 5, 5);

// Function to add comment
$im->commentImage("G4G");

// Function to set the image format
$im->setImageFormat('png');

// Printing Added Comment 
echo $im->getImageProperty("comment");
?>
```

发帖主题：Re：Колибри0.7.0

```
G4G
```

**引用：**[http://php.net/manual/en/gmagick.commentimage.php](http://php.net/manual/en/gmagick.commentimage.php)
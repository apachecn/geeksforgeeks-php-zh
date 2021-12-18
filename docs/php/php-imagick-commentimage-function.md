# PHP|Imagick CommentImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-commentimage-function/](https://www.geeksforgeeks.org/php-imagick-commentimage-function/)

**Imagick：：CommentImage()**函数是 PHP 中的内置函数，用于在图像中添加注释。

**语法：**

```
*bool* Imagick::commentImage( $comment )
```

**参数：**此函数接受单个参数*$COMMENT*，该参数用于保存注释。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

以下程序说明 PHP：
**程序 1：**中的**Imagick：：CommentImage()**函数

```
<?php 
// require_once('vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
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
**Imagick 函数创建的图像：**
![](img/112822c4852515d821106cc2ba5aa0b5.png)

```
<?php
$string = "Computer Science portal for Geeks!";

// creating new image of above String
// and add color and background
$im = new Imagick();
$draw = new ImagickDraw();

// Fill the color in image
$draw->setFillColor(new ImagickPixel('green'));

// Set the text font size
$draw->setFontSize(50);

$metrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($metrix['textWidth'], $metrix['textHeight'],
         new ImagickPixel('white'));

// Draw the image         
$im->drawImage($draw);

// Function to add border image
$im->borderImage(new ImagickPixel('Blue'), 5, 5);

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

**引用：**[http://php.net/manual/en/imagick.commentimage.php](http://php.net/manual/en/imagick.commentimage.php)
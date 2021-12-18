# PHP|ImagickDraw Comment()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-comment-function/](https://www.geeksforgeeks.org/php-imagickdraw-comment-function/)

**ImagickDraw：：Comment()函数**是 PHP 中的一个内置函数，用于向矢量输出流添加注释。 注释附加在输出流的末尾。

**语法：**

```
*bool* ImagickDraw::comment( *string* $comment )
```

**参数：**此函数接受包含注释的单个参数**$COMMENT**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：Comment()函数**：

**程序 1：**

```
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Add comment
$draw->comment('Hello ! This is my comment.');

// Get the vector graphics as string
$graphics = $draw->getVectorGraphics();

// Get comment from vector graphics
$comment = substr($graphics, 807); 
echo $comment;
?>
```

发帖主题：Re：Колибри0.7.0

```
Hello ! This is my comment.
```

**程序 2：**

```
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$string = 'This is my comment';

// Add comment
$draw->comment($string);

// Get the vector graphics
$graphics = $draw->getVectorGraphics();

// Get comment from vector graphics
$getComment = substr($graphics, 807, strlen($string));

// Set the font size
$draw->setFontSize(50);

// Write on image
$draw->annotation(50, 100, $getComment);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/ad7a4b9b67ae67f31a84d632ea7a17c6.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.comment.php](https://www.php.net/manual/en/imagickdraw.comment.php)
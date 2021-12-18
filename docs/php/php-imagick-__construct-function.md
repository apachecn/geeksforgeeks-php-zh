# PHP|Imagick__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-__construct-function/](https://www.geeksforgeeks.org/php-imagick-__construct-function/)

Imagick：：__Construct()函数是 Imagick 类构造函数，它以图像路径或图像 URL 为参数实例化特定图像或一组图像的 Imagick 对象。

**语法：**

```
Imagick::__construct( $files )
```

**参数：**此函数接受单个参数**$files**，该参数保存要加载的图像的路径或路径数组。 它可以包含文件名的通配符，也可以是 URL。

**返回值：**此函数在成功执行时返回一个新的 Imagick 对象。

**异常：**此函数在出错时引发 ImagickException 异常。

**程序：**此程序使用图像的 URL 加载图像并显示在屏幕上。

```
<?php

// Create a new Imagick object
$image = new Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png"); 

// Browser should know that image is to be loaded on the page
header("Content-Type: image/png");

// Display the image object
echo $image;

?>
```

**输出：**
![](img/675b6279bd4cd0c205249489180917e2.png)

**引用：**[https://www.php.net/manual/en/imagick.construct.php](https://www.php.net/manual/en/imagick.construct.php)
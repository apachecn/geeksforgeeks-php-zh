# PHP|Imagick smushImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-smushimages-function/](https://www.geeksforgeeks.org/php-imagick-smushimages-function/)

**Imagick：：smushImages()函数**是 PHP 中的一个内置函数，用于获取当前图像列表中的所有图像到图像末尾，如果堆栈参数设置为 true，则从上到下将它们相互粉碎，否则从左到右。

**语法：**

```php
*bool* Imagick::smushImages(*bool* $stack, *int* $offset)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$STACK：**此参数保存布尔值，该布尔值决定是从上到下粉碎(如果为 TRUE)还是从左到右粉碎(如果是 FALSE)。
*   **$Offset：**此参数保存平均偏移量。

**返回值：**此函数返回新的粉碎图像。

下面的程序演示了 PHP 中的**Imagick：：smushImages()函数**：

**程序 1：**

```php
<?php

// Create a new Imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Create another new Imagick object
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190920144514/tint22.png');

// Add the image
$imagick1->addimage($imagick2);

// Apply the smushImages() function
$smushed = $imagick1->smushImages(false, 100);

header("Content-Type: image/png");

// Display the output image
echo $smushed->getImageBlob();

?>
```

**输出：**
![](img/e9e19cc1721d99103fab26d59f4fa342.png)

**程序 2：**

```php
<?php
// Create a new Imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190920144514/tint22.png');

// Create another new Imagick object
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Add the image
$imagick1->addimage($imagick2);

// Apply the smushImages() function
$smushed = $imagick1->smushImages(true, 70);

header("Content-Type: image/png");

// Display the output image
echo $smushed->getImageBlob();

?>
```

**输出：**
![](img/e3d90a323525d1de8310710936fa8cd7.png)

**引用：**[https://www.php.net/manual/en/imagick.smushimages.php](https://www.php.net/manual/en/imagick.smushimages.php)
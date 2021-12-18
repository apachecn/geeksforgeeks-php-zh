# PHP|Imagick setImageIndex()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageindex-function/](https://www.geeksforgeeks.org/php-imagick-setimageindex-function/)

**Imagick：：setImageIndex()函数**是 PHP 中的内置函数，用于设置迭代器位置。

**语法：**

```
*bool* Imagick::setImageIndex( *int* $index )
```

**参数：**此函数接受保存索引的单个参数**$index**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setImageIndex()函数**：

**程序 1：**

```
<?php 

// Create a new imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Add two more images in the same imagick object 
$imagick->addImage( new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png')); 

$imagick->addImage( new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png')); 

// Currently Cursor is at 2
// Set the Index to 0
$imagick->setImageIndex(0);

// Get the Index 
$index = $imagick->getImageIndex(); 
echo $index; 
?> 
```

发帖主题：Re：Колибри0.7.0

```
0
```

**程序 2：**

```
<?php 

// Create a new imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Add two more images in the same imagick object 
$imagick->addImage( new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'));

// Currently Cursor is at 1
// Set the Index to 0
$imagick->setImageIndex(0);

// getImageBlob() should show last added image but
// cursor is set to 0 thus it shows first image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![spread-after](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageindex.php](https://www.php.net/manual/en/imagick.setimageindex.php)
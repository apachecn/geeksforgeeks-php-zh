# PHP|Imagick setIteratorIndex()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setiteratorindex-function/](https://www.geeksforgeeks.org/php-imagick-setiteratorindex-function/)

**Imagick：：setIteratorIndex()函数**是 PHP 中的一个内置函数，用于设置图像迭代器位置。 这是*setImageIndex()*函数的替代方法。

**语法：**

```php
*bool* Imagick::setIteratorIndex( *int* $index )
```

**参数：**此函数接受保存索引的单个参数**$index**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setIteratorIndex()函数**：

**程序 1：**

```php
<?php 

// Create a new imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Add two more images in the same imagick object 
$imagick->addImage( new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png')); 

// Currently Cursor is at 1
// Set the Index to 0
$imagick->setIteratorIndex(0);

// getImageBlob should show last added image but
// cursor is set to 0 thus it shows first image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d2cdeddf65779f170b39764ad552411f.png)

**程序 2：**

```php
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
// Set the Index to 1
$imagick->setIteratorIndex(1);

// Get the Index 
$index = $imagick->getIteratorIndex(); 
echo $index; 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**引用：**[https://www.php.net/manual/en/imagick.setiteratorindex.php](https://www.php.net/manual/en/imagick.setiteratorindex.php)
# PHP|Imagick getIteratorIndex()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getiteratorindex-function/](https://www.geeksforgeeks.org/php-imagick-getiteratorindex-function/)

**Imagick：：getIteratorIndex()函数**是 PHP 中的一个内置函数，用于获取当前活动图像的索引。 这是[getImageIndex()](https://www.geeksforgeeks.org/php-imagick-getimageindex-function/)函数的替代函数。

**语法：**

```php
*int* Imagick::getIteratorIndex( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含堆栈中图像索引的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getIteratorIndex()函数**：

**程序 1：**

```php
<?php 

// Create a new imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Get the Index 
$index = $imagick->getIteratorIndex(); 
echo $index; 
?> 
```

发帖主题：Re：Колибри0.7.8.0

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

// Get the Index 
$index = $imagick->getIteratorIndex(); 
echo $index; 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getiteratorindex.php](https://www.php.net/manual/en/imagick.getiteratorindex.php)
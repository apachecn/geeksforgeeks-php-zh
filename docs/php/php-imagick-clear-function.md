# PHP|Imagick Clear()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-clear-function/](https://www.geeksforgeeks.org/php-imagick-clear-function/)

Imagick：：Clear()函数是 PHP 中的一个内置函数，用于清除分配给 Imagick 对象的所有资源。

**语法：**

```php
*bool* Imagick::clear( void )
```

**参数：**此函数不接受任何参数。 它只清除用于调用该函数的 Imagick 对象的资源。

**返回值：**如果清除资源，此函数返回 TRUE，否则返回 FALSE。

**程序 1：**此程序不使用 Imagick：：Clear()函数显示图像内容。

```php
<?php

// Store the image into variable
$url = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png';

// The file_get_contents() function
// reads the image as string
$image = file_get_contents($url);

// Create an Imagick object 
$imagick = new Imagick();
$imagick->readImageBlob($image); 

// Comment the clear() function which 
// will display the image on the web page 
//$imagick->clear(); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick->getImageBlob(); 

?>
```

**输出：**
![](img/ded06631e74b5bffdf1e7968b7550922.png)

**程序 2：**此程序使用 Imagick：：Clear()函数清除与 Imagick 对象关联的所有资源。

```php
<?php

// Store the image into variable
$url = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png';

// The file_get_contents() function
// reads the image as string
$image = file_get_contents($url);

// Create an Imagick object 
$imagick = new Imagick();
$imagick->readImageBlob($image); 

// Comment the clear() function which 
// will display the image on the web page 
$imagick->clear(); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick->getImageBlob(); 

?>
```

**输出：**
![](img/1bb3c033b2056c36c2867a42eb6da19a.png)

**引用：**[https://www.php.net/manual/en/imagick.clear.php](https://www.php.net/manual/en/imagick.clear.php)
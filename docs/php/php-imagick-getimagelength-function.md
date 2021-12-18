# PHP|Imagick getImageLength()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagelength-function/](https://www.geeksforgeeks.org/php-imagick-getimagelength-function/)

**Imagick：：getImageLength()**函数是 PHP 中的内置函数，用于获取图像对象的字节长度。

**语法：**

```
*bool* Imagick::getImageLength( void)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回图像长度(以字节为单位)。

下面的程序演示了 PHP 中的**Imagick：：getImageLength()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Getting Length of image
// using getimagerelength function
$res = $imagick->getImageLength();

// Display Result 
echo "Length of Image = " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
Length of Image = 45435 

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```
<?php

$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png');

// Getting Length of image
// using getimagerelength function
$res = $imagick->getImageLength();

// Display Result 
echo "Length of Image = ". $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
Length of Image = 25694 

```

**引用：**[http://php.net/manual/en/imagick.getimagelength.php](http://php.net/manual/en/imagick.getimagelength.php)
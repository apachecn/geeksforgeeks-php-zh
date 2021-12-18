# PHP|Gmagick setsize()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setsize-function/](https://www.geeksforgeeks.org/php-gmagick-setsize-function/)

**gmagick：：setsize()函数**是 PHP 中的一个内置函数，用于设置与 gmagick 对象相关联的大小。

**语法：**

```
*Gmagick* Gmagick::setsize( *int* $columns, *int* $rows )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Columns：**它指定图像的宽度。
*   **$row：**它指定图像的高度。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setsize()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the size
$gmagick->setsize(200, 200);

// Get the size
$size = $gmagick->getsize();
print_r($size);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [columns] => 200 [rows] => 200 )
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the size
$gmagick->setsize(600, 200);

// Crop image using size
$gmagick->cropimage(
    $gmagick->getsize()['columns'],
    $gmagick->getsize()['rows'], 0, 0
);

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/73d7cf05dd254093c13c9d122ee6dae4.png)

**引用：**[https://www.php.net/manual/en/gmagick.setsize.php](https://www.php.net/manual/en/gmagick.setsize.php)
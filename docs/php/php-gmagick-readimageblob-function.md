# PHP|Gmagick readimageblob()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-readimageblob-function/](https://www.geeksforgeeks.org/php-gmagick-readimageblob-function/)

**Gmagick：：readimageblob()函数**是 PHP 中的一个内置函数，用于从二进制字符串读取图像。 这个字符串被称为 BLOB，因此被命名为*readimageblob*。 此外，可以使用*getimageblob()*函数将图像转换为字符串。

**语法：**

```php
*Gmagick* Gmagick::readimageblob( *string* $imageContents, *string* $filename )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$imageContents：**它指定二进制图像内容。
*   **$filename：**它指定要赋予文件的名称。

**返回值：**此函数返回包含图像的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：readimageblob()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(从字符串读取图像(BLOB))：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Convert image into string
$imageAsString = $gmagick->getimageblob();

// Create new Gmagick object
$gmagickNew = new Gmagick();

// Read image from string
$gmagickNew->readimageblob($imageAsString, 'mygeeksforgeeks.png');

// Output the image
header('Content-type: image/png');
echo $gmagickNew;
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2(读后进一步编辑图像)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Convert image into string
$imageAsString = $gmagick->getimageblob();

// Create new Gmagick object
$gmagickNew = new Gmagick();

// Read image from string
$gmagickNew->readimageblob($imageAsString,
            'myembossedgeeksforgeeks.png');

// Here you can further edit your
// loaded image as given below

// Emboss the image
$gmagickNew->embossimage(30, 20);

// Output the image
header('Content-type: image/png');
echo $gmagickNew;
?>
```

**输出：**
![](img/cb3f3dc8e81fc02517f650ec51bbfd62.png)

**引用：**[https://www.php.net/manual/en/gmagick.readimageblob.php](https://www.php.net/manual/en/gmagick.readimageblob.php)
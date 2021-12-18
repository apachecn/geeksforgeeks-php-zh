# PHP|imagecreatefrom mstring()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromstring-function/](https://www.geeksforgeeks.org/php-imagecreatefromstring-function/)

**imagecreatefrom mstring()函数**是 PHP 中的一个内置函数，用于从字符串文件或 URL 创建新图像。 这个图像可以在程序中进一步处理。 当您想要在从字符串加载图像后对其进行编辑时，通常使用此函数。

**语法：**

```
*resource* imagecreatefromstring( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序演示了 PHP 中的**imagecreatefrom mstring()函数**：

**程序 1(查看字符串中的图像)：**

```
<?php

// Image data in the form of string
$data = 'iVBORw0KGgoAAAANSUhEUgAAAHgAAAAUAQMAAAB'
      . '8nGuwAAAABlBMVEX///8AAP94wDzzAAAACXBIWX'
      . 'MAAA7EAAAOxAGVKw4bAAAAgUlEQVQYlWNgIBHYM'
      . 'TDwMDB8gDEYkkEU4wwog4HhAIx/AMqX4+c5/rDh'
      . '4x4w4wHDAWPJ3h7DxhnPwAwDhuOJG87zsD/mOQB'
      . 'mMDAcrt9/nv1hM88BMOMBw+EEA94GQxAfxDBgSD'
      . 'acceYMUP8BMMOAwU6evyf9YcOHA2DGA1K9QykAA'
      . 'NIrNwD/nKH3AAAAAElFTkSuQmCC';

// Decode the data
$data = base64_decode($data);

// Create an image from data
$im = imagecreatefromstring($data);

// Output the image
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/53d7e1ebd2bf40195945c9e90be8b3ec.png)

**程序 2(处理加载的字符串图像)：**

```
<?php

// Image data in the form of string
$data = 'iVBORw0KGgoAAAANSUhEUgAAAHgAAAAUAQMAAAB'
      . '8nGuwAAAABlBMVEX///8AAP94wDzzAAAACXBIWX'
      . 'MAAA7EAAAOxAGVKw4bAAAAgUlEQVQYlWNgIBHYM'
      . 'TDwMDB8gDEYkkEU4wwog4HhAIx/AMqX4+c5/rDh'
      . '4x4w4wHDAWPJ3h7DxhnPwAwDhuOJG87zsD/mOQB'
      . 'mMDAcrt9/nv1hM88BMOMBw+EEA94GQxAfxDBgSD'
      . 'acceYMUP8BMMOAwU6evyf9YcOHA2DGA1K9QykAA'
      . 'NIrNwD/nKH3AAAAAElFTkSuQmCC';

// Decode the data
$data = base64_decode($data);

// Create an image from data
$im = imagecreatefromstring($data);

// Negate the image
imagefilter($im, IMG_FILTER_NEGATE);

// Output the image
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/72cae62054dba609055ac4b7762e250d.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromstring.php](https://www.php.net/manual/en/function.imagecreatefromstring.php)
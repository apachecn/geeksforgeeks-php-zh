# PHP|Imagick readImageFile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-readimagefile-function/](https://www.geeksforgeeks.org/php-imagick-readimagefile-function/)

**Imagick：：readImageFile()函数**是 PHP 中的一个内置函数，用于从打开的文件句柄读取图像。

**语法：**

```
*bool* Imagick::readImageFile( *resource* $filename, *string* $fileName = NULL )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$fileHandle：**它指定文件句柄。
*   **$filename：**它指定文件的名称。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：readImageFile()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a file handle
$handle = fopen(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png', 'rgb');

// Read the image
$imagick->readImageFile($handle);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a file handle
$handle = fopen(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif',
'rgb');

// Read the image
$imagick->readImageFile($handle);

// Display the image
header("Content-Type: image/gif");
echo $imagick->getImagesBlob();
?>
```

**输出：**
![](img/df7e9c5957f2cb509bf9afaa1f0bbbfd.png)

**引用：**[https://www.php.net/manual/en/imagick.readimagefile.php](https://www.php.net/manual/en/imagick.readimagefile.php)
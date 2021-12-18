# PHP|Imagick WriteImageFile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-writeimagefile-function/](https://www.geeksforgeeks.org/php-imagick-writeimagefile-function/)

**Imagick：：WriteImageFile()函数**是 PHP 中的一个内置函数，用于将图像序列写入打开的文件句柄。 手柄必须用 fopen 打开。

**语法：**

```
*bool* Imagick::writeImageFile( *resource* $filehandle, *string* $format )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$fileHandle：**它指定文件句柄。
*   **$format(可选)：**指定图像的格式。 默认值取自句柄的 filename。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：WriteImageFile()函数**：

**程序 1：**

```
<?php 

// Create a new imagick object 
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Create a file handle with read/write access
$myfile = 'writeimagefile.png';
$handle = fopen($myfile, 'w+'); 

// Write image to filehandle without format
$imagick->writeImageFile($handle); 

// Get image from filehandle
$newImage = new Imagick();
$newImage->readImageFile($handle);
header("Content-Type: image/png");
echo $newImage->getImageBlob();
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```
<?php 
// Create a new imagick object 
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Add floodfillPaintImage
$imagick->floodfillPaintImage("green", 1, "white", 1, 1, false);

// Create a file handle 
$myfile = 'writeimagefile2';
$handle = fopen($myfile, 'w+'); 

// Write image to filehandle with png format
$imagick->writeImageFile($handle, 'png'); 

// Get image from filehandle
$newImage = new Imagick();
$newImage->readImageFile($handle);
header("Content-Type: image/png");
echo $newImage->getImageBlob();
?>
```

**输出：**
![](img/658b5878d8db034974a76877d760620a.png)

**引用：**[https://www.php.net/manual/en/imagick.writeimagefile.php](https://www.php.net/manual/en/imagick.writeimagefile.php)
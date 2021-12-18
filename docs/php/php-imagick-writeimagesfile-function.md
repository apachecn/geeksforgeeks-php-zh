# PHP|Imagick WriteImagesFile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-writeimagesfile-function/](https://www.geeksforgeeks.org/php-imagick-writeimagesfile-function/)

**Imagick：：WriteImagesFile()函数**是 PHP 中的一个内置函数，用于将所有图像帧写入打开的文件句柄。 此方法可用于将动画 gif 或其他多帧图像写入打开的文件句柄。

**语法：**

```
*bool* Imagick::writeImagesFile( *resource* $filehandle, *string* $format )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$fileHandle：**它指定写入图像的文件句柄。
*   **$format(可选)：**指定图像的格式。 它是文件句柄中提供的图像格式的默认设置。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：WriteImagesFile()函数**：

**程序 1：**

```
<?php 

// Create a new imagick object 
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif'); 

// Create a file handle
$myfile = 'writeimagesfile.gif';
$handle = fopen($myfile, 'w+'); 

// Write image to filehandle
$imagickAnimation->writeImagesFile($handle); 

// Get image from filehandle
$newImage = new Imagick();
$newImage->readImageFile($handle);
header("Content-Type: image/gif");
echo $newImage->getImagesBlob();
?>
```

**输出：**
![](img/df7e9c5957f2cb509bf9afaa1f0bbbfd.png)

**程序 2：**

```
<?php 

// Create a new imagick object 
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117192946/delay2.gif'); 

// Create a file handle
$myfile = 'writeimagesfile2';
$handle = fopen($myfile, 'w+'); 

// Write image to filehandle with gif format
$imagickAnimation->writeImagesFile($handle, 'gif'); 

// Get image from filehandle
$newImage = new Imagick();
$newImage->readImageFile($handle);
header("Content-Type: image/gif");
echo $newImage->getImagesBlob();
?>
```

**输出：**
![](img/6d328ebf357b496869a89c7b81e916e4.png)

**引用：**[https://www.php.net/manual/en/imagick.writeimagesfile.php](https://www.php.net/manual/en/imagick.writeimagesfile.php)
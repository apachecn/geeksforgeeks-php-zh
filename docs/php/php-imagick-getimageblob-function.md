# PHP|Imagick getImageBlob()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageblob-function/](https://www.geeksforgeeks.org/php-imagick-getimageblob-function/)

**Imagick：：getImageBlob()函数**是 PHP 中的一个内置函数，用于以 BLOB 形式获取图像序列。 它实现了直接到内存的图像格式。 此函数以字符串形式返回图像序列。

**语法：**

```
*string* Imagick::getImageBlob( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像的字符串。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageBlob()**函数：

**程序 1：**

```
<?php 

// Create an Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

header("Content-Type: image/png"); 

// Display the output image 
echo $imagick->getImageBlob(); 

?>
```

**输出：**
![](img/77c36ca0c1fed4bb69d0f145636d68af.png)

**程序 2：**

```
<?php 

// Create an Imagick object 
$image = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png'); 

header('Content-type: image/jpeg'); 

// Use blurImage function 
$image->blurImage(5, 3); 

// Display the output image 
echo $image->getImageBlob(); 
?> 
```

**输出：**
![imagick](img/587aaf45d52a19f8fa603e80f3fb301b.png)

**引用：**[https://www.php.net/manual/en/imagick.getimageblob.php](https://www.php.net/manual/en/imagick.getimageblob.php)
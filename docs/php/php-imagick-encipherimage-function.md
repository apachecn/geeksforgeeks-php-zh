# PHP|Imagick EncipherImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-encipherimage-function/](https://www.geeksforgeeks.org/php-imagick-encipherimage-function/)

Imagick：：encipherImage()函数是 PHP 中的内置函数，用于将普通像素图像转换为加密像素。 此函数只需将像素转换为加密的像素，然后只有在使用与加密时相同的字符串解密图像时，图像才可读。

**语法：**

```
*bool* Imagick::encipherImage( $passphrase )
```

**参数：**此函数接受保存密钥值的单个参数**$passphrase**。

**返回值：**成功返回 True，失败返回 False。

下面的程序演示了 PHP 中的 Imagick：：EncipherImage()函数：

**程序：**

```
<?php

// Creating new Imagick object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Creating the passphrase
$passphrase = "GeeksforGeeks";

// Calling the function
$image->encipherImage($passphrase);

// $image is now enciphered with string
// "GeeksforGeeks"
// $image can only be made readable by 
// decipherImage() method
// with the same passphrase as parameter

header("Content-Type: image/jpg"); 

// Showing the deciphered image which is
// same as our sampleimage.jpeg
echo $image;

?>
```

**输出：**
**如果密码不正确，则解密图像：**
![](img/fdb93857aa766020c7a3c158875a2a52.png)

**引用：**[https://php.net/manual/en/imagick.encipherimage.php](https://php.net/manual/en/imagick.encipherimage.php)
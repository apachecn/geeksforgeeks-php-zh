# PHP|Imagick decpherImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-decipherimage-function/](https://www.geeksforgeeks.org/php-imagick-decipherimage-function/)

**Imagick：：decpherImage()函数**是 PHP 中的一个内置函数，用于解密以前加密过的图像。

**语法：**

```
*bool* Imagick::decipherImage( *string* $passphrase )
```

**参数：**此函数接受单个参数**$passphrase**，该参数保存用于解密图像的密钥值或密钥。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：decpherImage()函数**：

**程序：**

```
<?php

/* Create a new Imagick object 
which is an enciphered image 
with passphrase 'GeeksforGeeks' */
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191020203919/g4genciphered.png');

// Applying the decipher() function
$imagick->decipher('GeeksforGeeks'); 

header("Content-Type: image/png"); 

// Display the output image 
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/77c36ca0c1fed4bb69d0f145636d68af.png)

**引用：**[https://www.php.net/manual/en/imagick.decipherimage.php](https://www.php.net/manual/en/imagick.decipherimage.php)
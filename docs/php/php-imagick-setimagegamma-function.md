# PHP|Imagick setImageGamma()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagegamma-function/](https://www.geeksforgeeks.org/php-imagick-setimagegamma-function/)

**Imagick：：setImageGamma()函数**是 PHP 中的内置函数，用于设置图像 Gamma。

**语法：**

```
*bool* Imagick::setImageGamma( *float* $gamma )
```

**参数：**此函数接受单个参数**$Gamma**，该参数保存图像的 Gamma。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setImageGamma()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gamma
$imagick->setImageGamma(5);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/4e5b83edc3c0b3f6e035ee3cd1ceb9d9.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Gamma
$imagick->setImageGamma(15);

// Add a border
$imagick->borderImage('black', 2, 2);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/f2f213a5b470b89cd0d102e3e2c4dbce.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagegamma.php](https://www.php.net/manual/en/imagick.setimagegamma.php)
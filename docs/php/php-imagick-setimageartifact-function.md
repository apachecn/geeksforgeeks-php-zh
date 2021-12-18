# PHP|Imagick setImageArtiact()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageartifact-function/](https://www.geeksforgeeks.org/php-imagick-setimageartifact-function/)

**Imagick：：setImageArtiact()函数**是 PHP 中的一个内置函数，用于设置图像工件。 图像属性和图像工件之间的主要区别在于属性是公共的，而工件是私有的。

**语法：**

```
*bool* Imagick::setImageArtifact( *string* $artifact, *string* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$artiact：**此参数保存工件的名称。
*   **$value：**此参数保存工件的值。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageArtiact()函数**：

**程序：**

```
<?php

// Create two new Imagick objects
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190920144344/smushf.png');

// Apply the setImageArtifact() function
$imagick2->setImageArtifact('compose:args', "0, 1, 0.4, -0.6");
$imagick1->compositeImage($imagick2, Imagick::COMPOSITE_MATHEMATICS, 0, 0);

// Display the output image
$imagick1->setImageFormat('png');

header("Content-Type: image/png");

echo $imagick1->getImagesBlob();

?>
```

**输出：**
![](img/18a2289dbfaf23daed4886a78d7b7e59.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageartifact.php](https://www.php.net/manual/en/imagick.setimageartifact.php)
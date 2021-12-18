# PHP|Imagick getImageArtiact()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageartifact-function/](https://www.geeksforgeeks.org/php-imagick-getimageartifact-function/)

**Imagick：：getImageArtiact()函数**是 PHP 中的一个内置函数，用于获取与工件名称相关联的图像工件值。 图像属性和图像工件之间的主要区别在于属性是公共的，而工件是私有的。

**语法：**

```php
*bool* Imagick::getImageArtifact( *string* $artifact )
```

**参数：**此函数接受单个参数**$artiface**，该参数保存工件的名称。

**返回值：**此函数在成功时返回工件值。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImageArtiact()函数**：

**程序：**

```php
<?php

// Create a new Imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the setImageArtifact() function
$imagick->setImageArtifact("artifact_name", "artifact_value");

// Apply the getImageArtifact() function
$artifact_name = $imagick->getImageArtifact("artifact_name");
echo $artifact_name;

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageartifact.php](https://www.php.net/manual/en/imagick.getimageartifact.php)
# PHP|Imagick delete eImageArtiact()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-deleteimageartifact-function/](https://www.geeksforgeeks.org/php-imagick-deleteimageartifact-function/)

**Imagick：：delete eImageArtiact()函数**是 PHP 中的一个内置函数，用于删除图像工件。 图像属性和图像工件之间的主要区别在于属性是公共的，而工件是私有的。

**语法：**

```php
*bool* Imagick::deleteImageArtifact( *string* $artifact )
```

**参数：**此函数接受单个参数**$artiface**，该参数保存工件的名称。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：delete eImageArtiact()函数**：

**程序：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the setImageArtifact() function to create a artifact
$imagick->setImageArtifact("artifact_name", "artifact_value");

// Apply the deleteImageArtifact() function to delete a artifact
$imagick->deleteImageArtifact("artifact_name");

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageartifact.php](https://www.php.net/manual/en/imagick.getimageartifact.php)
# PHP|getimagesize()函数

> Original: [https://www.geeksforgeeks.org/php-getimagesize-function/](https://www.geeksforgeeks.org/php-getimagesize-function/)

PHP 中的 getimagesize()函数是一个内置函数，用于获取图像的大小。 此函数接受文件名作为参数，确定图像大小，并返回包含文件类型和图像高度/宽度的尺寸。

**语法：**

```php
array getimagesize( $filename, $image_info )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**它是指定图像文件名的强制参数。
*   **$IMAGE_INFO：**这是一个可选参数，允许您从图像文件中提取一些扩展信息，例如不同的 JPG 应用程序标记作为关联数组。

**返回值：**它返回尺寸以及文件类型和高度/宽度文本字符串。

**例外：**

*   如果格式可能不包含图像或包含多个图像，则 getimagesize()函数的宽度和高度返回零。
*   Imageinfo 参数仅支持 JFIF 文件。
*   如果无法访问文件名映像，则 getimagesize()函数将生成 E_WARNING 级别的错误。
*   如果读取过程中有任何错误，getimagesize()将生成 E_NOTICE 级别的错误。

下面的程序演示了 PHP 中的 getimagesize()函数：

**注意：**下面的程序中使用的图像*(geeks.png)*。
![geeks image](img/fe5217eb9bf33352cbcbe436b8c9406e.png)

**程序 1：**

```php
<?php

// Calling getimagesize() function
$image_info = getimagesize("geeks.png");
print_r($image_info);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [0] => 667 
        [1] => 184 
        [2] => 3 
        [3] => width="667" height="184" 
        [bits] => 8 
        [mime] => image/png )

```

**程序 2：**

```php
<?php

// Calling getimagesize() function
list($width, $height, $type, $attr) = getimagesize("geeks.png");

// Displaying dimensions of the image
echo "Width of image : " . $width . "<br>";

echo "Height of image : " . $height . "<br>";

echo "Image type :" . $type . "<br>";

echo "Image attribute :" .$attr;
?>
```

发帖主题：Re：Колибри0.7.0

```php
Width of image : 667
Height of image : 184
Image type :3
Image attribute :width="667" height="184"

```

**引用：**[http://php.net/manual/en/function.getimagesize.php](http://php.net/manual/en/function.getimagesize.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
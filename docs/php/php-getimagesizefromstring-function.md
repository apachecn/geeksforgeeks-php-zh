# PHP|getimagesizefrom 字符串()函数

> Original: [https://www.geeksforgeeks.org/php-getimagesizefromstring-function/](https://www.geeksforgeeks.org/php-getimagesizefromstring-function/)

**getimagesizefrom mstring()**函数是 PHP 中的一个内置函数，用于从字符串中获取图像的大小。 此函数接受图像数据作为字符串参数，并确定图像大小并返回尺寸以及图像的文件类型和高度/宽度。

**语法：**

```
*array* getimagesizefromstring( $imagedata, &$imageinfo )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**它是一个强制参数，接受字符串形式的图像数据。
*   **$imageinfo：**这是一个可选参数，允许从图像文件中提取一些扩展信息，例如不同的 JPG 应用程序标记作为关联数组。

**返回值：**此函数返回尺寸以及文件类型和高度/宽度文本字符串。

下面的程序演示了 PHP 中的**getimagesizefrom mstring()**函数：

**图像：**
![](img/05c5bf662a556b71c049ead7820fc8d1.png)

**示例 1：**

```
<?php

$img = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-25.png';

// Open image as a string
$data = file_get_contents($img);

// getimagesizefromstring function accepts image data as string
$info = getimagesizefromstring($data);

// Display the image content
var_dump($info);
?>
```

发帖主题：Re：Колибри0.7.0

```
array(6) { 
    [0]=> int(667) 
    [1]=> int(184) 
    [2]=> int(3) 
    [3]=> string(24) "width="667" height="184"" 
    ["bits"]=> int(8) 
    ["mime"]=> string(9) "image/png" 
} 

```

**示例 2：**

```
<?php
$img = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-25.png';

// Open image as a string
$data = file_get_contents($img);

// getimagesizefromstring function accepts image data as string
list($width, $height, $type, $attr) = getimagesizefromstring($data);

// Displaying dimensions of the image 
echo "Width of image: " . $width . "<br>"; 

echo "Height of image: " . $height . "<br>"; 

echo "Image type: " . $type . "<br>"; 

echo "Image attribute: " . $attr; 
?>
```

发帖主题：Re：Колибри0.7.0

```
Width of image: 667
Height of image: 184
Image type: 3
Image attribute: width="667" height="184"

```

**引用：**[http://php.net/manual/en/function.getimagesizefromstring.php](http://php.net/manual/en/function.getimagesizefromstring.php)
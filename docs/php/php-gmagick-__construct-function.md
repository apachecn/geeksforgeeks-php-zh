# PHP|gmagick__struct()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-__construct-function/](https://www.geeksforgeeks.org/php-gmagick-__construct-function/)

**Gmagick：：__Construct()函数**是 PHP 中的内置函数，用于创建 Gmagick 对象。 可以使用这个新创建的 Gmagick 对象进行进一步的 Gmagick 操作。

**语法：**

```
*public* Gmagick::__construct( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。

**返回值：**如果成功，此函数将返回一个新的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面的程序说明了 PHP 中的**Gmagick：：__Construct()函数**：

**程序 1：**此程序在浏览器中显示图像。

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Output the image to browser
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**此程序显示带边框的图像。

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Border the image
$gmagick->borderimage('red', 20, 20);

// Output the image to browser
header('Content-type: image/png');  
echo $gmagick;  
?>  
```

**输出：**
![](img/d30eea22ec2d2a97ef734c0d04c4d352.png)

**引用：**[https://www.php.net/manual/en/gmagick.construct.php](https://www.php.net/manual/en/gmagick.construct.php)
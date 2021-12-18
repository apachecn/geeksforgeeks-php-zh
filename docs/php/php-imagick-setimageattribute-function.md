# PHP|Imagick setImageAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageattribute-function/](https://www.geeksforgeeks.org/php-imagick-setimageattribute-function/)

**Imagick：：setImageAttribute()函数**是 PHP 中的一个内置函数，用于设置键的值属性。

**语法：**

```
*bool* Imagick::setImageAttribute( *string* $key, *string* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$key：**此参数保存 image 属性的键。
*   **$value：**此参数保存 image 属性的值。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setImageAttribute()函数**：

**程序 1：**

```
<?php

// Create a Imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set an attribute with key 'my_key'
$imagick->setImageAttribute('my_key', 'my_value');

// Get the attribute with key 'my_key'
$attribute = $imagick->getImageAttribute('my_key');

echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.0

```
my_value
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Write the caption in a image
$imagick->newPseudoImage(800, 350, "caption:GeekforGeeks");

// Set the my_color attribute to green
$imagick->setImageAttribute('my_color', 'green');

$imagick->floodfillPaintImage( 
                 $imagick->getImageAttribute('my_color'),
                 1, "white", 1, 1, false);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/96a018bcf112f7d42478cde874a7adf6.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageattribute.php](https://www.php.net/manual/en/imagick.setimageattribute.php)
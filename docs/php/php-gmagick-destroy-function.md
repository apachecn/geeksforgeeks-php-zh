# PHP|Gmagick 销毁()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-destroy-function/](https://www.geeksforgeeks.org/php-gmagick-destroy-function/)

**Gmagick：：Destroy()函数**是 PHP 中的一个内置函数，用于销毁 Gmagick 对象并释放与其关联的所有资源。

**语法：**

```php
*bool* Gmagick::destroy( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 GmagickException。
**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

下面给出的程序演示了 PHP 中的**Gmagick：：Destroy()函数**：

**程序 1：**

```php
<?php
// Create a new Gmagick object

$gmagick = new Gmagick(
    'geeksforgeeks.png');

// Destroy the object resources
$gmagick->destroy();

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>  
```

发帖主题：Re：Колибри0.7.0

```php
No image is shown as output because it is destroyed.
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick(
    'geeksforgeeks.png');

$gmagick->setimageresolution(20, 20);
echo "Before destruction:<br>";
print("<pre>".print_r($gmagick->getimageresolution(), true)."</pre>");

// Destroy the object resources
$gmagick->destroy();

echo "After destruction:<br>";
print("<pre>".print_r($gmagick->getimageresolution(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Before destruction:
Array
(
    [x] => 20
    [y] => 20
)
After destruction:
```

**引用：**[https://www.php.net/manual/en/gmagick.destroy.php](https://www.php.net/manual/en/gmagick.destroy.php)
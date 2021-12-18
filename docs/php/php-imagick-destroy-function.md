# PHP|Imagick Destroy()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-destroy-function/](https://www.geeksforgeeks.org/php-imagick-destroy-function/)

**Imagick：：Destroy()函数**是 PHP 中的一个内置函数，用于销毁 Imagick 对象并释放与其关联的所有资源。 一旦对象内容被销毁，您将无法访问它。

**语法：**

```php
*bool* Imagick::destroy( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：Destroy()函数**：

**程序：**

```php
<?php

// Create a new imagick object with image
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use your $imagick object for whatever you want 
// to do here and destroy it after using it.

// Destroying that object
$imagick->destroy();
?>
```

**输出：**因为图像失真，所以不会显示任何图像。

**引用：**[https://www.php.net/manual/en/imagick.destroy.php](https://www.php.net/manual/en/imagick.destroy.php)
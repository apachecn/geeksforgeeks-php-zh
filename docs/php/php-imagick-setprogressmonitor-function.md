# PHP|Imagick setProgressMonitor()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setprogressmonitor-function/](https://www.geeksforgeeks.org/php-imagick-setprogressmonitor-function/)

**Imagick：：setProgressMonitor()函数**是 PHP 中的一个内置函数，用于设置在 Imagick 图像处理过程中出错时将调用的回调函数。 您可以使用此功能暂停程序，然后再继续。

**语法：**

```php
*bool* Imagick::setProgressMonitor( *callable* $callback )
```

**参数：**此函数接受保存回调函数的单个参数**$callback**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setProgressMonitor()函数**：

**程序 1：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create a image in Imagick object
$imagick->newImage(640, 480, "blue");

$status = 'Not cancelled';
$text = '<br>';

// Callback function
$callback = function ($offset, $span) use (&$status, $text) {
    $status = "Callback is called" . $text;
    return false;
};

// Set the Progress Monitor
$imagick->setProgressMonitor($callback);

try {
    // $x and $y are undefined thus a call to
    // callback funcction is expected here
    $imagick->charcoalImage($x, $y);
    echo "Callback function wasn't called.";
} catch (\Exception $e) {
    echo $status;
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create a image in Imagick object
$imagick->newImage(600, 400, "white");

$status = 'Not cancelled';
$text = '<br>';

// Callback function
$callback = function ($offset, $span) use (&$status, $text) {
    $status = "Callback is called" . $text;
    return true;
};

// Set the Progress Monitor
$imagick->setProgressMonitor($callback);

try {
    // $x and $y are defined thus a call to
    // callback funcction is expected here
    $x = 20;
    $y = 5;
    $imagick->charcoalImage($x, $y);
    echo "Callback function wasn't called.";
} catch (\Exception $e) {
    echo $status;
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setprogressmonitor.php](https://www.php.net/manual/en/imagick.setprogressmonitor.php)
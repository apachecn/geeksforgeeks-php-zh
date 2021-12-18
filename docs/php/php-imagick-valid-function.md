# PHP|Imagick Valid()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-valid-function/](https://www.geeksforgeeks.org/php-imagick-valid-function/)

**Imagick：：Valid()函数**是 PHP 中的内置函数，用于检查当前项是否有效。

**语法：**

```php
*bool* Imagick::valid( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：Valid()函数**：

**程序 1：**

```php
<?php
try {

    // Create a new imagick object with invalid image
    $imagick = new Imagick('undefined_source');
    if ($imagick->valid()) {
        echo 'Image is valid';
    }
} catch (exception $e) {
    echo 'Image is not valid';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
try {

    // Create a new imagick object with valid image
    $imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');
    if ($imagick->valid()) {
        echo 'Image is valid';
    }
} catch (exception $e) {
    echo 'Image is not valid';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.valid.php](https://www.php.net/manual/en/imagick.valid.php)
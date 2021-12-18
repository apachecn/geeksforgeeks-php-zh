# PHP|Imagick setLastIterator()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setlastiterator-function/](https://www.geeksforgeeks.org/php-imagick-setlastiterator-function/)

**Imagick：：setLastIterator()函数**是 PHP 中的一个内置函数，用于将 Imagick 迭代器设置为最后一个图像。

**语法：**

```php
*bool* Imagick::setLastIterator( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setLastIterator()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Add a new image to same object, this
// will automatically move index to new
// image which is added.
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'));

// Move the cursor to first image
$imagick->setFirstIterator();

echo 'Index before setLastIterator() is '
          . $imagick->getIteratorIndex() . '<br>';

// Set the Imagick iterator to the last image
$imagick->setLastIterator();

echo 'Index after setLastIterator() is '
         . $imagick->getIteratorIndex() . '<br>';
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Array of images
$images = [
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png',
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png',
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png',
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png',
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'
];

// Read the images
$imagick->readImages($images);

// Move iterator to first image
$imagick->setFirstIterator();

echo 'Index before setLastIterator() is ' 
        . $imagick->getIteratorIndex() . '<br>';

// Set the Imagick iterator to the last image
$imagick->setLastIterator();

echo 'Index after setLastIterator() is ' 
        . $imagick->getIteratorIndex() . '<br>';
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setlastiterator.php](https://www.php.net/manual/en/imagick.setlastiterator.php)
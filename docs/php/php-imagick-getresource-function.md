# PHP|Imagick getResource()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getresource-function/](https://www.geeksforgeeks.org/php-imagick-getresource-function/)

**Imagick：：getResource()函数**是 PHP 中的一个内置函数，用于获取指定资源的内存使用情况。

**语法：**

```php
*int* Imagick::getResource( *int* $type )
```

**参数：**此函数接受单个参数**$type**，该参数保存与**RESOURCETYPE 常量**之一相对应的整数值。 我们也可以像*getResource(Imagick：：RESOURCETYPE_DISK)；*那样直接传递常量。
所有 RESOURCETYPE 常量列表如下：

*   Imagick：：RESOURCETYPE_UNDEFINED(0)
*   Imagick：：RESOURCETYPE_AREA(1)
*   Imagick：：RESOURCETYPE_DISK(2)
*   Imagick：：RESOURCETYPE_FILE(3)
*   Imagick：：RESOURCETYPE_MAP(4)
*   Imagick：：RESOURCETYPE_MEMORY(5)
*   Imagick：：RESOURCETYPE_THREAD(6)

**返回值：**此函数返回包含资源信息的整数值。
**异常：**此函数在出错时引发 ImagickException。
下面给出的程序说明了 PHP：
**程序 1：**中的**Imagick：：getResource()函数**

## PHP

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

//Get the Resource
$resource = $imagick->getResource(imagick::RESOURCETYPE_AREA);
echo $resource;
?>
```
# PHP|Imagick getResourceLimit()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getresourcelimit-function/](https://www.geeksforgeeks.org/php-imagick-getresourcelimit-function/)

**Imagick：：getResourceLimit()函数**是 PHP 中的内置函数，用于获取指定的资源限制。

**语法：**

```
*int* Imagick::getResourceLimit( *int* $type )
```

**参数：**此函数接受单个参数**$type**，该参数保存与**RESOURCETYPE 常量**之一相对应的整数值。 我们也可以像*getResourceLimit(Imagick：：RESOURCETYPE_DISK)；*那样直接传递常量。

所有 RESOURCETYPE 常量的列表如下：

*   Imagick：：RESOURCETYPE_UNDEFINED(0)
*   Imagick：：RESOURCETYPE_Area(1)
*   Imagick：：RESOURCETYPE_DISK(2)
*   Imagick：：RESOURCETYPE_FILE(3)
*   想象一下。 *RESOURCETYPE_THREAD(6)

**返回值：**此函数返回包含以 MB 为单位的指定资源限制的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getResourceLimit()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

//Get the Resource Limit
$resourceLimit = $imagick->getResourceLimit(imagick::RESOURCETYPE_MAP);
echo $resourceLimit;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

//Get the Resource Limit
$resourceLimit = $imagick->getResourceLimit(imagick::RESOURCETYPE_AREA);
echo $resourceLimit;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getresourcelimit.php](https://www.php.net/manual/en/imagick.getresourcelimit.php)
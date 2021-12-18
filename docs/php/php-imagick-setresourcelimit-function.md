# PHP|Imagick setResourceLimit()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setresourcelimit-function/](https://www.geeksforgeeks.org/php-imagick-setresourcelimit-function/)

**Imagick：：setResourceLimit()函数**是 PHP 中的内置函数，用于设置特定资源的限制。

**语法：**

```
*int* Imagick::setResourceLimit( *int* $type, *int* $limit )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$type:** it specifies the integer value corresponding to one of the RESOURCETYPE constants.
*   **$Limit:** it specifies the integer value that contains the limit.

所有 RESOURCETYPE 常量的列表如下：

*   Imagick：：RESOURCETYPE_UNDEFINED(0)
*   Imagick：：RESOURCETYPE_Area(1)
*   Imagick：：RESOURCETYPE_DISK(2)
*   Imagick：：RESOURCETYPE_FILE(3)
*   想象一下。 *RESOURCETYPE_THREAD(6)

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setResourceLimit()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Resource Limit
$imagick->setResourceLimit(imagick::RESOURCETYPE_AREA, 5000);

//Get the Resource Limit
$resourceLimit = $imagick->getResourceLimit(imagick::RESOURCETYPE_AREA);
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

// Set the Resource Limit
$imagick->setResourceLimit(imagick::RESOURCETYPE_MAP, 80000);

//Get the Resource Limit
$resourceLimit = $imagick->getResourceLimit(imagick::RESOURCETYPE_MAP);
echo $resourceLimit;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setresourcelimit.php](https://www.php.net/manual/en/imagick.setresourcelimit.php)
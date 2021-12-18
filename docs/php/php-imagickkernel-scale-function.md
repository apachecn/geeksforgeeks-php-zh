# PHP|ImagickKernel scale()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-scale-function/](https://www.geeksforgeeks.org/php-imagickkernel-scale-function/)

**ImagickKernel：：Scale()函数**是 PHP 中的一个内置函数，用于按给定数量缩放给定的内核列表。

**语法：**

```
*void* ImagickKernel::scale( *float* $scale, *int* $normalizeFlag )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$scale：**它指定缩放量。
*   **$NormizeFlag：**它指定刻度的类型。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ImagickKernel：：Scale()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix = [
    [0, 0, 1],
    [0, 2, 1],
    [1, 1, 1],
];

// Create a kernel from built-in matrix
$kernel = ImagickKernel::fromMatrix($matrix);

echo 'Before scaling:<br>';
print("<pre>".print_r($kernel->getMatrix(), true)."</pre>");

// Scale the kernel
$kernel->scale(5, Imagick::NORMALIZE_KERNEL_VALUE);

echo 'After scaling:<br>';
print("<pre>".print_r($kernel->getMatrix(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Before scaling:
Array
(
    [0] => Array
        (
            [0] => 0
            [1] => 0
            [2] => 1
        )

    [1] => Array
        (
            [0] => 0
            [1] => 2
            [2] => 1
        )

    [2] => Array
        (
            [0] => 1
            [1] => 1
            [2] => 1
        )

)
After scaling:
Array
(
    [0] => Array
        (
            [0] => 0
            [1] => 0
            [2] => 0.71428571428571
        )

    [1] => Array
        (
            [0] => 0
            [1] => 1.4285714285714
            [2] => 0.71428571428571
        )

    [2] => Array
        (
            [0] => 0.71428571428571
            [1] => 0.71428571428571
            [2] => 0.71428571428571
        )

)
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix = [
    [1, 2, -3],
    [4, 5, 6],
    [7, 8, 9]
];

// Create a kernel from matrix
$kernel = ImagickKernel::fromMatrix($matrix);

// Scale the kernel
$kernel->scale(4, Imagick::NORMALIZE_KERNEL_VALUE);

// Add the filter
$imagick->filter($kernel);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/e216beea6bd18b53b49b99c0fc733823.png)

**引用：**[https://www.php.net/manual/en/imagickkernel.scale.php](https://www.php.net/manual/en/imagickkernel.scale.php)
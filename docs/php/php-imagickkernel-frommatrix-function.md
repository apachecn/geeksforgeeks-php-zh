# PHP|ImagickKernel from mMatrix()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-frommatrix-function/](https://www.geeksforgeeks.org/php-imagickkernel-frommatrix-function/)

**ImagickKernel：：FromMatrix()函数**是 PHP 中的一个内置函数，用于从二维值矩阵创建内核。 如果使用元素，则 2D 矩阵的值为 FLOAT，否则，如果跳过元素，则为 FALSE。

**语法：**

```
*ImagickKernel* ImagickKernel::fromMatrix( *array* $matrix, *array* $origin )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Matrix：**它指定定义内核的值矩阵。 值可以是 Float 或 False。
*   **$Origin(可选)：**它指定应该用作原始像素的内核元素。 这仅在非方阵的情况下是必需的。

**返回值：**如果成功，此函数将返回一个新的 ImagickKernel 对象。

下面的程序说明了 PHP 中的**ImagickKernel：：FromMatrix()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix = [
    [-1.5, -1, -0.2],
    [0, 1, 1],
    [0, 0.5, 1],
];

// Create a kernel from matrix
$kernel = ImagickKernel::fromMatrix($matrix);

// Add the filter
$imagick->filter($kernel);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/db28b56998b87f388e4404d6f54bf95b.png)

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

// Get the matrix
$matrix = $kernel->getMatrix();

print("<pre>".print_r($matrix, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [0] => Array
        (
            [0] => 1
            [1] => 2
            [2] => -3
        )

    [1] => Array
        (
            [0] => 4
            [1] => 5
            [2] => 6
        )

    [2] => Array
        (
            [0] => 7
            [1] => 8
            [2] => 9
        )

)
```

**引用：**[https://www.php.net/manual/en/imagickkernel.frommatrix.php](https://www.php.net/manual/en/imagickkernel.frommatrix.php)
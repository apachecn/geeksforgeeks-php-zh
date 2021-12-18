# PHP|ImagickKernel getMatrix()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-getmatrix-function/](https://www.geeksforgeeks.org/php-imagickkernel-getmatrix-function/)

**ImagickKernel：：getMatrix()函数**是 PHP 中的一个内置函数，用于获取内核中使用的值的 2D 矩阵。 如果应跳过元素，则元素为 Float 或‘false’。

**语法：**

```
*array* ImagickKernel::getMatrix( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含矩阵的数组值。

下面的程序演示了 PHP 中的**ImagickKernel：：getMatrix()函数**：

**程序 1：**本程序使用 getMatrix()函数从自定义矩阵中获取矩阵。

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix = [
    [-1, 0, 0],
    [4, -1, 6],
    [7, 8, 6]
];

// Create a kernel from matrix
$kernel = ImagickKernel::fromMatrix($matrix);

// Get the matrix
$matrix = $kernel->getMatrix();

print("<pre>".print_r($matrix, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(从内置矩阵获取矩阵)：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a kernel from built-in matrix
$kernel = ImagickKernel::fromBuiltIn(Imagick::KERNEL_DISK, "2");

// Get the matrix
$matrix = $kernel->getMatrix();

foreach ($matrix as $row) {
    foreach ($row as $cell) {
        if ($cell === false) {
            $output .= 0;
        } else {
            $output .= $cell;
        }
    }
    $output .= "<br>";
}
echo $output;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickkernel.getmatrix.php](https://www.php.net/manual/en/imagickkernel.getmatrix.php)
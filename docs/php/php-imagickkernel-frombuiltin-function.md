# PHP|ImagickKernel from mBuiltIn()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-frombuiltin-function/](https://www.geeksforgeeks.org/php-imagickkernel-frombuiltin-function/)

**ImagickKernel：：from mBuiltIn()函数**是 PHP 中的内置函数，用于从内置内核创建内核。

**语法：**

```
*ImagickKernel* ImagickKernel::fromBuiltIn( *int* $kernelType, *string* $kernelString )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$kernelType：**它指定内核的类型。
*   **$kernelString：**它指定描述参数的字符串。

**返回值：**如果成功，此函数将返回一个新的 ImagickKernel 对象。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickKernel：：from mBuiltIn()函数**：

**程序 1：**

```
<?php

// Create a kernel from matrix
$kernel = ImagickKernel::fromBuiltIn(Imagick::KERNEL_DIAMOND, "2");

echo "The matrix of Builtin kernel - Diamond: <br/>";

// Get the matrix from kernel
$matrix = $kernel->getMatrix();

foreach ($matrix as $row) {
    foreach ($row as $cell) {
        if ($cell === false) {
            $output .= "0";
        } else {
            $output .= $cell;
        }
    }
    $output .= "<br>";
}

echo $output;
?>
```

发帖主题：Re：Колибри0.7.0

```
The matrix of Builtin kernel - Diamond:
00100
01110
11111
01110
00100
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a kernel from built In types
$kernel = ImagickKernel::fromBuiltIn(Imagick::KERNEL_SQUARE, "2");

// Scale the kernel
$kernel->scale(2, Imagick::NORMALIZE_KERNEL_VALUE);

// Add the filter
$imagick->filter($kernel);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/bcd265121a143b1fe6a70b94b08c7209.png)

**引用：**[https://www.php.net/manual/en/imagickkernel.frombuiltin.php](https://www.php.net/manual/en/imagickkernel.frombuiltin.php)
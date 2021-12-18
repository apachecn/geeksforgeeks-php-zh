# PHP|ImagickKernel addUnityKernel()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-addunitykernel-function/](https://www.geeksforgeeks.org/php-imagickkernel-addunitykernel-function/)

**ImagickKernel：：addUnityKernel()函数**是 PHP 中的一个内置函数，用于将给定数量的‘Unity’卷积内核添加到给定内核。 此函数用于将定义的内核转换为混合软模糊、锐化内核或锐化内核。

**语法：**

```
*bool* ImagickKernel::addUnityKernel( *float* $scale )
```

**参数：**此函数接受单个参数**$scale**，该参数保存单位内核的刻度。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickKernel：：addUnityKernel()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a kernel from matrix
$kernel = ImagickKernel::fromMatrix(
        [[-1, 0, -1], [0, 4, 0], [-1, 0, 0]]);

// Add the Unity Kernel
$kernel->addUnityKernel(0.7);

// Add the filter
$imagick->filter($kernel);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/f5dfe302845fa9b17afd924dc3951fd0.png)

**程序 2：**

```
<?php

// Create a kernel from matrix
$kernel = ImagickKernel::fromMatrix(
        [[-3, 0, -2], [ 3, 4,  2], [-1, 0, -1]]);

echo "Before adding unity kernel: <br/>";
print("<pre>".print_r($kernel->getMatrix(), true)."</pre>");

// Add the Unity Kernel
$kernel->addUnityKernel(12);

echo "After adding unity kernel: <br/>";
print("<pre>".print_r($kernel->getMatrix(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Before adding unity kernel:
Array
(
    [0] => Array
        (
            [0] => -3
            [1] => 0
            [2] => -2
        )

    [1] => Array
        (
            [0] => 3
            [1] => 4
            [2] => 2
        )

    [2] => Array
        (
            [0] => -1
            [1] => 0
            [2] => -1
        )

)
After adding unity kernel:
Array
(
    [0] => Array
        (
            [0] => -3
            [1] => 0
            [2] => -2
        )

    [1] => Array
        (
            [0] => 3
            [1] => 16
            [2] => 2
        )

    [2] => Array
        (
            [0] => -1
            [1] => 0
            [2] => -1
        )

)
```

**引用：**[https://www.php.net/manual/en/imagickkernel.addunitykernel.php](https://www.php.net/manual/en/imagickkernel.addunitykernel.php)
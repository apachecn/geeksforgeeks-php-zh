# PHP|ImagickKernel addKernel()函数

> Original: [https://www.geeksforgeeks.org/php-imagickkernel-addkernel-function/](https://www.geeksforgeeks.org/php-imagickkernel-addkernel-function/)

**ImagickKernel：：addKernel()函数**是 PHP 中的一个内置函数，用于将另一个内核附加到该内核。 使用此函数，我们可以将多个矩阵附加到同一内核，并使用我们想要的任何一个。

**语法：**

```php
*void* ImagickKernel::addKernel( *ImagickKernel* $ImagickKernel )
```

**参数：**此函数接受保存内核的单个参数**$ImagickKernel**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickKernel：：addKernel()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix1 = [
    [-1, -1, -1],
    [4, 4, 4],
    [1, 1, 1],
];

$matrix2 = [
    [-1, 0, 0],
    [0, 0, 1],
    [-1, 0, 1],
];

// Create ImagickKernel objects from matrices
$kernel1 = ImagickKernel::fromMatrix($matrix1);
$kernel2 = ImagickKernel::fromMatrix($matrix2);

// Add the kernel
$kernel1->addKernel($kernel2);

// Apply filter from second attached kernel
$imagick->filter($kernel1->separate()[1]);
header("Content-Type: image/jpg");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/a45c29a64ada96aca3184f2a6a16b1c6.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$matrix1 = [
    [-1, -1, -1],
    [4, 4, 4],
    [1, 1, 1],
];

$matrix2 = [
    [-1, 0, 0],
    [0, 0, 1],
    [-1, 0, 1],
];

$matrix3 = [
    [-1, 1, 0],
    [0, 0, 1],
    [-1, 0, 1],
];

$matrix4 = [
    [0, 1, 0],
    [0, 0, 1],
    [-1, 0, 1],
];

// Create ImagickKernel objects from matrices
$kernel1 = ImagickKernel::fromMatrix($matrix1);
$kernel2 = ImagickKernel::fromMatrix($matrix2);
$kernel3 = ImagickKernel::fromMatrix($matrix3);
$kernel4 = ImagickKernel::fromMatrix($matrix4);

// Add the kernels
$kernel1->addKernel($kernel2);
$kernel1->addKernel($kernel3);
$kernel1->addKernel($kernel4);

$kernelList = $kernel1->separate();

echo 'Total number of attached kernels are: ';
echo count($kernelList);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Total number of attached kernels are: 4
```

**引用：**[https://www.php.net/manual/en/imagickkernel.addkernel.php](https://www.php.net/manual/en/imagickkernel.addkernel.php)
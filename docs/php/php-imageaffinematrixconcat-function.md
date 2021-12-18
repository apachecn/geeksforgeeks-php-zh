# PHP|imageaffinemailxcatat()函数

> Original: [https://www.geeksforgeeks.org/php-imageaffinematrixconcat-function/](https://www.geeksforgeeks.org/php-imageaffinematrixconcat-function/)

**图像仿射变换函数**是 PHP 中内置的 GD 函数，用于连接两个仿射变换矩阵。 使用 GD 的**imageaffinemaxxget()**函数和**img_affine_*常量**得到仿射变换数组。

**语法：**

```
*array* imageaffinematrixconcat( *array* $m1, *array* $m2 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$M1：**此参数保存仿射变换矩阵，该矩阵具有一个键为 0 到 5 的数组和浮点值。
*   **$m2：**此参数保存仿射变换矩阵，该矩阵具有一个键为 0 到 5 的数组和浮点值。

**返回值：**它返回串联的仿射变换矩阵，该矩阵有一个键为 0 到 5 的数组，成功时为浮点值，失败时为 False。

下面的程序演示了 PHP 中的 imageaffinemailxcatat()函数：

**程序 1：**

```
<?php

// 1st Affine transformation matrix to be concatenate
$m1 = imageaffinematrixget(IMG_AFFINE_TRANSLATE,
                     array('x' => 12, 'y' => 23));

// 2nd Affine transformation matrix to be concatenate
$m2 = imageaffinematrixget(IMG_AFFINE_SCALE,
                     array('x' => 54, 'y' => 35));

// Concatenation process
$matrix = imageaffinematrixconcat($m1, $m2);

print_r($matrix);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [0] => 54 [1] => 0 [2] => 0 [3] => 35 [4] => 648 [5] => 805 )

```

**程序 2：**

```
<?php

// 1st Affine transformation matrix to be concatenate
$m1 = imageaffinematrixget(IMG_AFFINE_SHEAR_HORIZONTAL, 270);

// 2nd Affine transformation matrix to be concatenate
$m2 = imageaffinematrixget(IMG_AFFINE_ROTATE, 120);

// Concatenation process
$matrix = imageaffinematrixconcat($m1, $m2);
print_r($matrix);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [0] => -0.5 [1] => 0.86602540378444 [2] => -2.7218732255326E+15
        [3] => 4.7144227183838E+15 [4] => 0 [5] => 0 )

```

**引用：** [https://www.php.net/manual/en/function.imageaffinematrixconcat.php](https://www.php.net/manual/en/function.imageaffinematrixconcat.php)
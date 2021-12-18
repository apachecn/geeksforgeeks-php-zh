# PHP|ImagesetClip()函数

> Original: [https://www.geeksforgeeks.org/php-imagesetclip-function/](https://www.geeksforgeeks.org/php-imagesetclip-function/)

函数**的作用是：在 PHP 中内置函数，用于设置当前的裁剪矩形，也就是不绘制像素的区域。**

**语法：**

```
*bool* imagesetclip( *resource* $im, *int* $x1, *int* $y1, *int* $x2, *int* $y2 )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$im：**它指定要处理的图像资源。
*   **$x1：**它指定左上角的 x 坐标。
*   **$y1：**它指定左上角的 y 坐标。
*   **$x2：**它指定右下角的 x 坐标。
*   **$y2：**它指定右下角的 y 坐标。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。
下面给出的程序说明了 PHP
**程序 1 中的**ImagesetClip()函数**：**

```
<?php
// Load the png image
$image = imagecreatefrompng(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the clip
imagesetclip($image, 0, 0, 40, 40);

// Get the clip
$clip = imagegetclip($image);
print("<pre>".print_r($clip, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [0] => 0
    [1] => 0
    [2] => 40
    [3] => 40
)
```

**程序 2：**

```
<?php
// Load the png image
$image = imagecreatefrompng(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the clip
imagesetclip($image, 20, 20, 150, 150);

// Create a line from upper left corner to (400, 400)
// and you will see the line doesn't start from upper
// left corner because it is clipped from (20, 20)
$red = imagecolorallocate($image, 255, 0, 0);
imageline($image, 0, 0, 400, 400, $red);

// Output image to the browser
header('Content-type: image/png');
imagepng($image);
?>
```

**输出：**
![](img/88217fa2858ca19d8236315c1c2bae49.png)

**引用：**[https://www.php.net/manual/en/function.imagesetclip.php](https://www.php.net/manual/en/function.imagesetclip.php)
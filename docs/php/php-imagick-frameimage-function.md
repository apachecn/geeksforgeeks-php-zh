# PHP|Imagick Frame Image()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-frameimage-function/](https://www.geeksforgeeks.org/php-imagick-frameimage-function/)

Imagick：：FrameImage()函数是 PHP 中的一个内置函数，用于在图像周围添加三维边框。

**语法：**

```
*bool* Imagick::frameImage( $color, $width, $height, $inner_bevel, $outer_bevel )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$color：**边框的颜色，可以是字符串，也可以是十六进制格式。
*   **$width：**它设置边框的宽度。
*   **$Height：**它设置边框的高度。
*   **$INNER_BEVELL：**它设置内部倒角阴影的宽度。
*   **$out_bevel：**它设置外部倒角阴影的宽度。

**返回值：**成功返回 True，失败返回 False。

下面的程序演示了 PHP 中的 Imagick：：Frame Image()函数：

**程序 1：**

```
<?php 

// Create an Imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png'); 

// Use frameImage function 
$imagick->frameImage('yellow', 30, 30, 10, 10); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick->getImageBlob(); 

?> 
```

**输出：**
![](img/e1bb94b0ccbb2c65d8a2ac3276641a5e.png)

**程序 2：**

```
<?php

// Create new Imagick object
$image = new Imagick(__DIR__.'\sample_image.jpeg');

// Set the value of parameters
$color = "#211544";
$width_of_frame = 30;
$height_of_frame = 40;
$inner_Bevel = 15;
$outer_Bevel = 15;

// Call the function with parameters
$image->frameImage(
    $color,
    $width_of_frame,
    $height_of_frame,
    $inner_Bevel,
    $outer_Bevel
);

header('Content-type: image/jpeg');

// Writing the new image to specified directory
$image->writeImage(__DIR__.'\sample_image_with_border2.jpeg');

?>
```

**输出：**
![](img/607e58ac3977d4d0e20d3055344d5421.png)

**程序 3：**

```
<?php

// Create a function which accepts the parameters
// and returns the framed image object
function frame_image($Imagik_obj, $color, $width_of_frame,
                $height_of_frame, $inner_bevel, $outer_bevel)
{
    $Imagik_obj->frameImage(
        $color,
        $width_of_frame,
        $height_of_frame,
        $inner_Bevel,
        $outer_Bevel
    );

    return $Imagik_obj;
}

// Call the function with the parameters
echo frame_image(new Imagick(__DIR__.'\sample_image.jpeg'),
                 "#211544", 30, 40, 15, 15)->getImageBlob();

header('Content-type: image/jpeg');

?>
```

**输出：**
![](img/607e58ac3977d4d0e20d3055344d5421.png)

**参考：**[https://www.php.net/manual/en/imagick.frameimage.php](https://www.php.net/manual/en/imagick.frameimage.php)
如果您发现错误或想要添加更多信息，请发表意见。 编码快乐！！
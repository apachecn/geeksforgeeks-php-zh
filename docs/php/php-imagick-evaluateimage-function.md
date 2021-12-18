# PHP|Imagick valuateImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-evaluateimage-function/](https://www.geeksforgeeks.org/php-imagick-evaluateimage-function/)

Imagick：：valuateImage()函数是 PHP 中的内置函数，用于将表达式应用于图像。 它可以将任何算术、逻辑或关系表达式应用于图像并评估其结果。 该操作符有许多用途，从改变图像的亮度即使图像变亮或变暗，或改变图像的对比度或产生图像的负片。

**语法：**

```php
*bool* Imagick::evaluateImage( $evaluation_op, $constant, $channel = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$EVALUATION_OP：**它包含加、减、除、模等求值运算符。
*   **$Constant：**它保存将进行评估的运算符的值。
*   **$channel：**它提供适合所需通道模式的任何通道常量。

**返回值：**如果函数执行成功，则返回布尔值 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 Imagick：：valuateImage()函数：

**程序 1：**

```php
<?php  

// Create an Imagick object  
$imagick = new Imagick(  
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');  

// Declare and initialize the value of variable
$evaluation_op = Imagick::EVALUATE_DIVIDE;
$constant = 3;
$channel = Imagick::CHANNEL_ALPHA;

// Use evaluateImage function  
$imagick->evaluateImage($evaluation_op, $constant, $channel);  

header("Content-Type: image/jpg");  

// Display the output image  
echo $imagick->getImageBlob();  

?>  
```

**输出：**
![](img/deaea876fe3977ab94bb6dfadc3dea56.png)

**程序 2：**

```php
<?php

// Creating new Imagick object
 $image = new Imagick(__DIR__ . '\sample.png');

// Set the Alpha Channel to Opaque to facilitate Opaque operation
$image->setImageAlphaChannel(Imagick::ALPHACHANNEL_OPAQUE);

// Set the values of parameters 
$evaluation_op = Imagick::EVALUATE_DIVIDE;
$constant = 3;
$channel = Imagick::CHANNEL_ALPHA;

// Calling the function with the parameters
$image->evaluateImage( $evaluation_op, $constant, $channel );

header('Content-type: image/jpeg'); 

// Writing the new image to specified directory
$image->writeImage(__DIR__ . '\sample_with_33perc_opacity.png');

?>
```

**输出：**
![](img/b398c4b31bab38531e6fe12bfdbf0244.png)

**程序 3：**

```php
<?php

// Function definition
function Evaluate_Image( $image, $evaluation_op, $constant, $channel )
{
    $image->evaluateImage( $evaluation_op, $constant, $channel );

    return $image;
}

// Set values of the parameters 
$final_image = Evaluate_Image(new Imagick(__DIR__ . '\sample.png'),
        Imagick::EVALUATE_MEAN, 3, Imagick::CHANNEL_BLUE);

header('Content-type: image/jpeg');

// Display the output image  
echo $final_image->getImageBlob();  

?>
```

**输出：**
![](img/4ab7367af7e79eb61ee29eb3a39b10ec.png)

**参考：**[https://www.php.net/manual/en/imagick.evaluateimage.php](https://www.php.net/manual/en/imagick.evaluateimage.php)
如果您发现错误或想要添加更多信息，请发表意见。 编码快乐！！
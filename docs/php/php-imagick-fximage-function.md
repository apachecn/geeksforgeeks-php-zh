# PHP|Imagick fxImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-fximage-function/](https://www.geeksforgeeks.org/php-imagick-fximage-function/)

*   **Imagick：：fxImage()**函数是 PHP 中的一个内置函数，用于计算图像中每个像素的表达式。
*   Imagick：：fxImage()函数允许您通过处理图像中每个像素的 FX 表达式集来执行图像操作。

**语法：**

```
Imagick::fxImage ( string $expression [, int $channel = Imagick::CHANNEL_DEFAULT ] )

```

**参数：**

*   **$expression**
    它是用于图像处理的 FX 表达式。
*   **$channel**
    可以根据有效的通道模式获取任何通道常量。 如果需要添加更多通道常量，请使用按位运算符合并通道类型常量。

**Return Value:**

*   **Imagick::fxImage** function will returns **TRUE** if success or returns
    **FALSE** on failure.

    **示例 1：**
    说明使用**Imagick：：fxImage()**函数通过 fx 表达式进行的图像操作。

    ```
    <?php
    // Imagick-fxImage
    $imagick = new \Imagick();
        //new pseudo image
        $imagick->newPseudoImage(200, 200, "gradient:white-black");

        //$fx value applied
        $fx = 'floor(s*10+0.5)/10';
        $fxImage = $imagick->fxImage($fx);
    //Display Image
        header("Content-Type: image/png");
        $fxImage->setimageformat('png');
        echo $fxImage->getImageBlob();
    ?>
    ```

    **输出：**
    ![](img/21376a2d4e7f340a31fecd84c22ee3f8.png)

    **示例 2：**
    说明使用**Imagick：：fxImage()**函数通过 fx 表达式进行的图像操作。

    ```
    <?php
    // Imagick-fxImage
    $imagick = new \Imagick();
    //New pseudo image
        $imagick->newPseudoImage(200, 200, "plasma:fractal");

        //$fx value applied
        $fx = '(u.g+v.g)/2';
        $fxImage = $imagick->fxImage($fx);

        //Display Image
        header("Content-Type: image/png");
        $fxImage->setimageformat('png');
        echo $fxImage->getImageBlob();
        $fxImage->WriteImage('Imagick-fxImageex02.png');
    ?>
    ```

    **输出：**
    ![](img/e8e0e84339ea6d5c10ea5e68eb2dde39.png)

    **引用：**[https://www.php.net/manual/en/imagick.fximage.php](https://www.php.net/manual/en/imagick.fximage.php)
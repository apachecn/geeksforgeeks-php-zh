# PHP|Imagick IdentifyFormat()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-identifyformat-function/](https://www.geeksforgeeks.org/php-imagick-identifyformat-function/)

**Imagick：：IdentifyFormat()函数**是 PHP 中的一个内置函数，用于将嵌入的格式字符替换为其相应的图像属性，并返回解释的文本。

**转义序列列表：**请参考链接查看转义序列列表。 参考：[http://www.imagemagick.org/script/escape.php](http://www.imagemagick.org/script/escape.php)

以下是一些重要的嵌入格式字符，如相应图像属性的转义序列：

*   **%h**当前图像高度(像素)*   **%i**图像文件名(注意：成为“info：”的输出文件名)*   **%k**已计算：唯一颜色数*   **%m**图像文件格式(文件魔术)*   **%n**当前图像序列中的图像数*   **%w**当前宽度(像素)*   **%x**x 分辨率(密度)*   **%y**y 分辨率(密度)*   **%z**图像深度(读入，除非修改，图像保存深度)*   **%U**个图像分辨率单位*   **%@** CALCULATED: trim bounding box (without actually trimming) etc…

    **语法：**

    ```php
    *string* Imagick::identifyFormat( $embedText )
    ```

    **参数：**此函数接受单个参数**$embedText**，该参数保存包含格式化序列的字符串。

    **返回值：**此函数返回图像格式，失败时返回 False。

    下面的程序演示了 PHP 中的 Imagick：：IdentifyFormat()函数：

    **程序：**此程序使用 Imagick：：IdentifyFormat()函数查找给定图像的格式。

    ```php
    <?php

    // Declare new Imagick object
    $imagick = new \Imagick(
    "https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png");

    // Store a string into variable
    $embedText = "Output of 'Trim box: %@ number of unique colors: %k' is: <br/>";

    // Use Imagick::identifyFormat() function to replace the embedded
    // format characters with its appropriate image property
    $embedText .= $imagick->identifyFormat("Trim box: %@ number of unique colors: %k");

    // Display the output
    echo $embedText;

    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    Output of 'Trim box: %@ number of unique colors: %k' is:
    Trim box: 656x144+5+15 number of unique colors: 2955
    ```

    **引用：**[https://www.php.net/manual/en/imagick.identifyformat.php](https://www.php.net/manual/en/imagick.identifyformat.php)
# PHP|GmagickDraw settext 装饰()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-settextdecoration-function/](https://www.geeksforgeeks.org/php-gmagickdraw-settextdecoration-function/)

GmagickDraw：：settextDecomment()函数是 PHP 中的一个内置函数，用于指定在使用文本进行批注时要应用的修饰。

**语法：**

```
*public* GmagickDraw::settextdecoration( $decoration ) : GmagickDraw
```

**参数：**此函数接受单个参数*$DEVERATION*，该参数用于保存 DEVERATION_CONSTANTINT 的值。
装饰常量列表如下：

*   Gmagick：：DEVERATION_NO(整数)
*   Gmagick：：装饰 _ 下划线(整数)
*   Gmagick：：Decay_OVERLINE(整数)
*   Gmagick ::DECORATION_LINETROUGH (integer)

    **返回值：**此函数在成功时返回 GmagickDraw 对象

    下面的程序演示了 PHP 中的 GmagickDraw：：settextDecomment()函数：

    **程序 1：**

    ```
    <?php

    // Create an GmagickDraw  object
    $draw = new GmagickDraw ();

    // Set the image filled color 
    $draw->setFillColor('green');

    // Set the font size
    $draw->setFontSize(60);

    // Set the Text Decoration
    $draw->setTextDecoration(4);

    // Set the text to be added
    $draw->annotation(50, 75, "GeeksForGeeks");

    // Create new Gmagick Object
    $gmagick = new Gmagick ();

    // Set image dimensions
    $gmagick ->newImage(500, 160, 'white');

    // Set the image format
    $gmagick ->setImageFormat("png");

    // Draw the image
    $gmagick ->drawImage($draw);
    header("Content-Type: image/png");

    // Display the image
    echo $gmagick ->getImageBlob();
    ?>
    ```

    **输出：**
    ![setTextDecoration](img/17d44b1e44a161e375cb910d0ba9f4d2.png)

    **程序 2：**

    ```
    <?php

    // Create an GmagickDraw object
    $draw = new GmagickDraw ();

    // Set the image filled color 
    $draw->setFillColor('yellow');

    // Set the font size
    $draw->setFontSize(20);

    // Set the TextDecoration() function
    // Text is Upperline
    $draw->setTextDecoration(3);
    // Set the text to be added
    $draw->annotation(50, 75, "A Computer Science Portal For Geeks!");

    // Create new Gmagick Object 
    $gmagick = new Gmagick ();

    // Set the image dimensions
    $gmagick ->newImage(500, 160, 'black');

    // Set the image format
    $gmagick ->setImageFormat("png");

    // Draw the image
    $gmagick ->drawImage($draw);
    header("Content-Type: image/png");

    // Display the image
    echo $gmagick ->getImageBlob();
    ?>
    ```

    **输出：**
    ![setTextDecoration](img/7bd49066a15f76c45ba421e45f723a07.png)

    **引用：**[http://php.net/manual/en/gmagickdraw.settextdecoration.php](http://php.net/manual/en/gmagickdraw.settextdecoration.php)
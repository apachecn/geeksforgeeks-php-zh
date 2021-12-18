# PHP|Imagick modateImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-modulateimage-function/](https://www.geeksforgeeks.org/php-imagick-modulateimage-function/)

**Imagick：：modateImage()**函数是 PHP 中的内置函数，用于控制图像的亮度、饱和度和色调。

**语法：**

```
*bool* Imagick::modulateImage( $brightness, $saturation, $hue )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Brightness：**此参数用于保存亮度值。
*   **$饱和度：**此参数用于保持饱和度的值。
*   **$hue：**此参数用于保存色调的值。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：modateImage()**函数：

**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

**程序 1：**

```
<?php 

/*require_once('vendor/autoload.php'); */

header('Content-type: image/png');

/*Create Imagick Object*/

$image = new Imagick('img/geeksforgeeks.png');

/*modulateImage function*/

$image->modulateImage(60, 100, 100);
echo $image;
?>
```

**输出：**
![Modulate Image](img/8f530aa6631f925eaed2b0dd878d7afa.png)

**程序 2：**

```
<?php 

/*require_once('vendor/autoload.php');*/
/*Imagick Object*/

$imagick = new Imagick('img/geeksforgeeks.png');

/*modulateImage*/

$imagick->modulateImage(100, 0, 100);

/*Write Image*/
$imagick->writeImage('rotationalImage1.png');

/*Destroy Imagick Variable*/
$imagick->destroy();
?>
```

**输出：**
![Modulate Image](img/a1b71337b30f284963fba3f83a79b8d9.png)

**引用：**[http://php.net/manual/en/imagick.modulateimage.php](http://php.net/manual/en/imagick.modulateimage.php)
# PHP|Imagick WriteImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-writeimages-function/](https://www.geeksforgeeks.org/php-imagick-writeimages-function/)

**Imagick：：WriteImages()函数**是 PHP 中的一个内置函数，用于将图像或图像序列写入指定的文件名。 此函数将图像文件保存在 PHP 脚本所在的同一文件夹中。 此函数支持 GIF 动画，而*writeImage()*不支持。

**语法：**

```
*bool* Imagick::writeImages( *string* $filename, *bool* $adjoin )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**它指定文件的名称。
*   **$ADJOIN：**它指定是否添加 ADJOIN。 如果为 True，则将动画保存为单个 gif 文件；如果为 False，则将动画的所有帧保存为单独的文件。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：WriteImages()函数**：

**程序 1：**

```
<?php 

// Create a new imagick object 
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif'); 

// Write that animation with name 'myanimation.gif'
$imagickAnimation->writeImages('myanimation.gif', true);
?>
```

**输出：**
这将在同一文件夹中保存名为*myAnimation.gif*的 GIF 图像。
![](img/9ed9dcd468491cbaf0ccc0c5e035eef6.png)

**程序 2：**

```
<?php 

// Create a new imagick object 
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif'); 

// Write that animation with name 'myanimation2.gif'
$imagickAnimation->writeImages('myanimation2.gif', false);
?>
```

发帖主题：Re：Колибри0.7.0

```
This will save 16 images all from different frames of given animation file with filenames as:
```

*   Myanimation2-0.gif
*   Myanimation2-1.gif
*   Myanimation2-2.gif
*   Myanimation2-3.gif
*   Myanimation2-4.gif
*   Myanimation2-5.gif
*   Myanimation2-6.gif
*   Myanimation2-7.gif
*   Myanimation2-8.gif
*   Myanimation2-9.gif
*   Myanimation2-10.gif
*   Myanimation2-11.gif
*   Myanimation2-12.gif
*   Myanimation2-13.gif
*   Myanimation2-14.gif
*   Myanimation2-15.gif

**引用：**[https://www.php.net/manual/en/imagick.writeimages.php](https://www.php.net/manual/en/imagick.writeimages.php)
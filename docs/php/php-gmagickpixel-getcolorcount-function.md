# PHP|GmagickPixel getColorcount()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickpixel-getcolorcount-function/](https://www.geeksforgeeks.org/php-gmagickpixel-getcolorcount-function/)

**GmagickPixel：：getColorcount()函数**是 PHP 中的一个内置函数，用于获取与像素颜色相关联的颜色计数。 颜色计数是图像中与此 GmagickPixel 具有相同颜色的像素数。 *getColorcount()*似乎只适用于通过*getimagehistgraph()*函数创建的 GmagickPixel 对象。

**语法：**

```
*int* GmagickPixel::getcolorcount( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含颜色计数的整数。

**异常：**此函数在出错时引发 GmagickPixelException。

下面给出的程序演示了 PHP 中的**GmagickPixel：：getColorcount()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image histogram (image as array of gmagickpixels)
$histogramElements = $gmagick->getImageHistogram(); 

// Get the last index 
$lastIndex = count($histogramElements) - 1; 

// Get the last element from array which is  
// a gmagickPixel object 
$lastColor = $histogramElements[$lastIndex]; 

// Get the Color count 
echo $lastColor->getcolorcount(); 
?>
```

发帖主题：Re：Колибри0.7.0

```
100064
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image histogram (image as array of gmagickpixels)
$histogramElements = $gmagick->getImageHistogram(); 

// Get the first element from array which is  
// a gmagickPixel object 
$firstColor = $histogramElements[0]; 

// Get the Color count 
echo $firstColor->getcolorcount(); 
?>
```

发帖主题：Re：Колибри0.7.0

```
1
```

**程序 3：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image histogram (image as array of gmagickpixels)
$histogramElements = $gmagick->getImageHistogram(); 

// Get the whole color stats 
echo "R G B Hue :Count<br>"; 
foreach ($histogramElements as $pixel) { 
    $colors = $pixel->getcolor(true); 
    foreach ($colors as $color) { 
        print($color . " "); 
    } 
    print(":" . $pixel->getcolorcount() . "<br>"); 
} 
?>
```

发帖主题：Re：Колибри0.7.0

```
R G B Hue :Count
0 22 35 :1
0 24 37 :1
0 25 37 :1
0 31 43 :1
0 32 44 :1
0 33 45 :1
0 36 48 :1
0 37 49 :3
.
.
.
```

**引用：**[https://www.php.net/manual/en/gmagickpixel.getcolorcount.php](https://www.php.net/manual/en/gmagickpixel.getcolorcount.php)
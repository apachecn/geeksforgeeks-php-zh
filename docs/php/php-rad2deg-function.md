# PHP|rad2deg()函数

> Original: [https://www.geeksforgeeks.org/php-rad2deg-function/](https://www.geeksforgeeks.org/php-rad2deg-function/)

角度测量是几何学和三角学的基石之一，最常用的两种测量方法是度数和弧度。 由于它的简单性，许多人更喜欢使用度数而不是弧度。 让学位更受欢迎的一些原因包括：

*   在计算导数或复杂关系时，次数可能效率不高，但它很容易理解和可视化。
*   虽然弧度实际上是一个比率，但度被认为是旋转位移的单位，其中完整的旋转相当于 360 度。 由于这种简单性，学生们接受的教育比弧度要熟悉得多，而且他们对学位的熟悉程度要比弧度高得多。

因此，在某些情况下，我们可能需要将弧度转换为度，这就是方法 rad2deg()的用武之地。

**语法：**

```
*float* rad2deg($value)

```

**参数**：该函数接受单个参数$value，该参数的类型为 Float，表示以弧度表示的角度。

**返回类型**：此函数返回表示给定角度$值等效度的浮点值。

例如：

```
Input :  $value = M_PI_4;
Output : 45

Input : $value = M_PI_2;
Output : 90

Input : $value = M_PI;
Output : 180

```

下面的程序演示了 rad2deg()在 PHP 中的工作方式：

```
<?php

// PHP code to illustrate the working of rad2deg()

$rad = M_PI;
$k = 1;

for(;$k<=8;$k*=2, $rad/=2)
{
    if($k!=1)
       echo 'pi/'.$k.' = '.rad2deg($rad)."\n";
    else
       echo 'pi = '.rad2deg($rad)."\n";
}

?>
```

产出：

```
pi = 180
pi/2 = 90
pi/4 = 45
pi/8 = 22.5

```

**需要注意的重要事项**：

*   它计算与以弧度为单位给定的角度相等的度数。
*   与该方法对应的是 rad2deg()。
*   这种方法可以产生非常精确的结果，但是时间效率不高。

**参考**：
[http://php.net/manual/en/function.rad2deg.php](http://php.net/manual/en/function.rad2deg.php)
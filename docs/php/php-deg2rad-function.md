# PHP|des2rad()函数

> Original: [https://www.geeksforgeeks.org/php-deg2rad-function/](https://www.geeksforgeeks.org/php-deg2rad-function/)

在测量角度的方法中，最常用的两种是度数和弧度。 学生们通常学习学位，而学习弧度则成为后来关注的问题。 但在某些情况下，弧度是首选的测量单位，例如：

*   在处理三角函数的导数时，最好使用角度的弧度度量，因为避免了圆周率 pi，所以导数更容易。
*   为了推导圆内任何运动的线速度和角速度之间的关系，在使用弧度测量时，它产生自然单位的速度，即 m/s，但是如果我们使用度，那么我们得到的速度是 m 度/s 的单位，必须经过另一次转换才能变成自然形式。

因此，在某些情况下需要将度数转换为弧度，这就是方法 des2rad()的用武之地。

**语法：**

```
*float* deg2rad ($value)

```

**参数**：该函数接受单个参数，该参数是一个浮点型，表示角度(以度为单位)。

**返回类型**：此函数返回表示角度的等值弧度的浮点值。

例如：

```
Input :  $deg = 45;
Output : 0.78539816339745

Input : $deg = 90;
Output : 1.5707963267949

Input : $deg = 180;
Output : 3.1415926535898

```

下面的程序演示了 des 2rad()在 PHP 中的工作方式：

```
<?php
// PHP code to illustrate the working of deg2rad()
$deg = 22.5;
$k = 8;
for(;$k>=1;$k/=2, $deg*=2)
{
  if($k!=1)
   echo 'pi/'.$k.' = '.deg2rad($deg).'<br>';
  else
   echo 'pi = '.deg2rad($deg).'<br>';
}

?>
```

产出：

```
pi/8 = 0.39269908169872
pi/4 = 0.78539816339745
pi/2 = 1.5707963267949
pi = 3.1415926535898

```

**需要注意的重要事项**：

*   它计算给定角度的弧度当量(以度为单位)。
*   该方法的对应物是 des2rad()。
*   这种方法可以产生非常精确的结果，但是时间效率不高。

**参考**：
[http://php.net/manual/en/function.deg2rad.php](http://php.net/manual/en/function.deg2rad.php)
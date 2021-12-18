# PHP|jdday of Week()函数

> Original: [https://www.geeksforgeeks.org/php-jddayofweek-function/](https://www.geeksforgeeks.org/php-jddayofweek-function/)

JddayofWeek()函数是 PHP 中的一个内置函数，它返回传入参数的儒略整数的给定星期几。 根据函数中传递的模式，返回值有三种类型。 它返回表示星期几的三种类型的值。 如果该模式作为 0 传递，则返回 0，1，2…。 表示周日、周一、周二的…。 周日、周一、周二…返回。 当 1 作为模式传递时。 当 2 作为模式传递时，它返回缩写 SUN，MON，TUE…。 作为一周中的某一天。

**语法：**

```
jddayofweek($jd, $mode)
```

**参数：**该函数接受两个参数，如下所示。

1.  **$jd**-这是一个强制参数，它将儒略日数字指定为整数。 使用**gregoriantojd(*****$Month，$day，$Year*****)**将公历日期转换为儒略日整数。
2.  **$mode**-这是一个可选参数，用于指定返回值的类型。 它接受 0-2 范围内的值(包括 0-2)。 默认值为 0。 以下是三种退货方式的描述：
    *   **0**-当模式作为 0 传递时，它返回 0、1、2、3.。 表示周日、周一、周二…。 分别作为星期几。 当没有模式参数丢失或传递的任何值超出范围时，这是模式的默认值。
    *   **1**-当模式作为 1 传递时，它返回星期日、星期一、星期二…
    *   **2**-当模式作为 2 传递时，它返回周日、周一、周二的缩写形式为 Sun、Mon、Tues。

**返回值：**该函数根据如上所述在参数中传递的模式的值返回星期几。
示例：

```
Input : $jd = 4/27/2018 ,  mode=0 
Output : 5

Input : $jd = 4/27/2018 ,  mode=1 
Output : Friday
```

下面的程序说明了**jdday of Week()**函数
**程序 1：**下面的程序演示了未通过模式并采用默认模式时的输出。

## PHP

```
<?php
// PHP program to demonstrate the
// use of jddayofweek() function
// when second parameter is not passed

// converts date to julian integer
$jd=gregoriantojd(4, 27, 2018);

// prints the day on the given date
echo jddayofweek($jd);
?>
```

**输出：**

```
5
```

**程序 2：**下面的程序演示了模式为 1 时的输出。

## PHP

```
<?php
// PHP program to demonstrate the
// use of jddayofweek() function
// when mode is 1

// converts date to julian integer
$jd=gregoriantojd(4, 27, 2018);

// prints the day on the given date
echo jddayofweek($jd, 1);
?>
```

**输出：**

```
Friday
```

**程序 3：**下面的程序演示了模式为 2 时的输出。

## PHP

```
<?php
// PHP program to demonstrate the
// use of jddayofweek() function
// when mode is 2

// converts date to julian integer
$jd=gregoriantojd(4, 27, 2018);

// prints the day on the given date
echo jddayofweek($jd, 2);
?>
```

**输出：**

```
Fri
```

**程序 4：**下面的程序演示了模式超出范围时的输出。

## PHP

```
<?php
// PHP program to demonstrate the
// use of jddayofweek() function
// when mode is out of range

// converts date to julian integer
$jd=gregoriantojd(4, 27, 2018);

// prints the day on the given date
echo jddayofweek($jd, 4);
?>
```

**输出：**

```
5
```

**引用：**
[http://php.net/manual/en/function.jddayofweek.php](http://php.net/manual/en/function.jddayofweek.php)
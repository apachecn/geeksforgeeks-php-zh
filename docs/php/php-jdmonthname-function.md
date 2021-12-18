# PHP|jdmonthname()函数

> Original: [https://www.geeksforgeeks.org/php-jdmonthname-function/](https://www.geeksforgeeks.org/php-jdmonthname-function/)

Jdmonthname()函数是 PHP 中的一个内置函数，它返回作为参数传递的儒略日数字的月份名称。 返回值有六种类型，具体取决于函数中传递的模式，下面的参数部分将对此进行简要说明。

**语法：**

```php
 jdmonthname($jd, $mode) 
```

**参数：**此函数接受两个参数，如下所示：

1.  **$jd-**此参数将儒略日指定为整数。 这是必选参数。
2.  **$mode-**这是指定返回值类型的强制参数。 该模式可以在 0-5 的范围内(包括 0-5)。
    *   **0**-它返回缩写形式(Jan、Feb、Mar 等)。 当模式作为 0 传递时，公历中月份名称的。
    *   **1**-返回月份名称(1 月、2 月、3 月等)。 在公历中，当模式作为 1 传递时。
    *   **2**-它返回缩写形式(Jan、Feb、Mar 等)。 当模式作为 2 传递时，儒略历中月份名称的。
    *   **3**-它返回月份名称(1 月、2 月、3 月等)。 在儒略历中，当模式作为 3 传递时。
    *   **4**-返回月份名称(Tishri、Heshvan、Kislev 等)。 在犹太历法中，当模式被传递为 4 时。
    *   **5**-in 返回月份名称(Vendemiaire、Brumaire、Frimaire 等)。 在法国共和党中，当模式被传递为 5 时。

**返回值：**该函数根据传递的模式返回月份名称。 如果将除 0-5 以外的任何值作为模式传递，则该模式被视为 0。

例如：

```php
Input : $jd = 2458236, $mode = 0 
Output : Apr
Explanation: In program below we have converted the 
date(4/27/2018) to the Julian Day integer which is 
2458236

Input : $jd = 2457031, $mode = 4 
Output : Tevet
Explanation: date(1/8/2015) in Julian Day integer is 2457031\. 
Tevet is the month on this Julian Day integer. 

```

以下程序说明了 jdmonthname()函数：

**程序 1：**下面的程序演示了当 mode 作为 0 传递时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the use
// of jdmonthname() function 
// when mode is passed as 0

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed as 0
echo (jdmonthname($jd, 0)), "\n"; 

?>
```

产出：

```php
Apr

```

**程序 2：**下面的程序演示了模式作为 1 传递时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the use
// of jdmonthname() function 
// when mode is passed as 1

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed as 1
echo (jdmonthname($jd, 1)), "\n"; 

?>
```

产出：

```php
April 

```

**程序 3：**下面的程序演示了模式作为 2 传递时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the
// use of jdmonthname() function 
// when mode is passed as 2

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed as 2
echo (jdmonthname($jd, 2)), "\n"; 

?>
```

产出：

```php
Apr

```

**程序 4：**下面的程序演示了模式作为 3 传递时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the
// use of jdmonthname() function 
// when mode is passed as 3

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed as 3
echo (jdmonthname($jd, 3)), "\n"; 

?>
```

产出：

```php
April

```

**程序 5：**下面的程序演示了模式作为 4 传递时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the
// use of jdmonthname() function 
// when mode is passed as 4

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed as 3
echo (jdmonthname($jd, 4)), "\n"; 

?>
```

产出：

```php
Iyyar

```

**程序 6：**下面的程序演示了当模式传递超出范围时的 jdmonthname()函数。

```php
<?php
// PHP program to demonstrate the
// use of jdmonthname() function 
// when mode is passed out of range

// converts the gregorian date to julian day integer 
$jd = gregoriantojd(4, 27, 2018); 

// prints the month name when mode is passed out of range
echo (jdmonthname($jd, 8)), "\n"; 

?>
```

产出：

```php
Apr

```

**引用：**
[http://php.net/manual/en/function.jdmonthname.php](http://php.net/manual/en/function.jdmonthname.php)
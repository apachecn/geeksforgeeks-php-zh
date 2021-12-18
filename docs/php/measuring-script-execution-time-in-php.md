# 在 PHP 中测量脚本执行时间

> 原文:[https://www . geesforgeks . org/measuring-script-execution-time-in-PHP/](https://www.geeksforgeeks.org/measuring-script-execution-time-in-php/)

PHP 中的脚本执行时间是执行 PHP 脚本所需的时间。要计算脚本执行时间，请使用时钟时间，而不是 CPU 执行时间。了解脚本执行前和执行后的时钟时间有助于了解脚本执行时间。

**示例:**样本脚本

```
<?php
for($i = 1; $i <=1000; $i++)
{
    echo "Hello Geeks!";
} 
?>
```

时钟时间可以使用[微时间()功能](https://www.geeksforgeeks.org/php-microtime-function/)获取。首先在脚本开始前使用，然后在脚本结束时使用。然后使用公式*(结束时间-开始时间)*。函数的作用是:以秒为单位返回时间。执行时间不是固定的，它取决于处理器。

**例:**

```
<?php

// Starting clock time in seconds
$start_time = microtime(true);
$a=1;

// Start loop
for($i = 1; $i <=1000; $i++)
{
    $a++;
} 

// End clock time in seconds
$end_time = microtime(true);

// Calculate script execution time
$execution_time = ($end_time - $start_time);

echo " Execution time of script = ".$execution_time." sec";
?>
```

**输出:**

```
Execution time of script = 1.6927719116211E-5 sec

```
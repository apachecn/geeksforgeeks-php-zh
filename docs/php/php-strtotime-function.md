# PHP|strtotime()函数

> Original: [https://www.geeksforgeeks.org/php-strtotime-function/](https://www.geeksforgeeks.org/php-strtotime-function/)

Strtotime()函数是 PHP 中的一个内置函数，用于将英文文本日期时间描述转换为 UNIX 时间戳。 该函数接受英语字符串参数，该参数表示日期-时间的描述。 例如，在英文日期-时间描述中，“Now”指的是当前日期。 此函数返回自[Unix 纪元](https://en.wikipedia.org/wiki/Unix_time)以来的时间(以秒为单位)。 我们可以使用 date()函数返回日期格式的英文文本日期时间。

**语法：**

```
strtotime ($EnglishDateTime, $time_now)
```

**参数：**此函数接受两个参数，如下所示：

1.  **$englishDateTime**-此参数指定英文文本日期-时间描述，表示要返回的日期或时间。 该函数解析字符串并返回以秒为单位的时间。 该参数是必填的
2.  **$TIME_NOW**此参数指定用于计算返回值的时间戳。 这是一个可选参数。

**注意：**由于时间/日期不是静态的，因此输出会有所不同。

下面的程序演示了 strtotime()函数。

**程序 1：**下面的程序演示了当英文文本为“NOW”时的 strtotime()
函数。

```
<?php
// PHP program to demonstrate the strtotime() 
// function when the english text is "now"

// prints current time in second 
// since now means current 
echo strtotime("now"), "\n"; 

// prints the current time in date format 
echo date("Y-m-d", strtotime("now"))."\n";
?>
```

产出：

```
1525378260
2018-05-03

```

**程序 2：**下面的程序演示了英文文本为日期时的 strtotime()
函数。

```
<?php
// PHP program to demonstrate the strtotime() 
// function when the english text is a date

// prints the converted english text in second 
echo strtotime("12th february 2017"), "\n"; 

// prints the above time in date format 
echo date("Y-m-d", strtotime("12th february 2017"))."\n";
?>
```

产出：

```
1486857600
2017-02-12

```

**程序 3：**下面的程序演示了当英文文本对应于任何一天时的 strtotime()
函数。

```
<?php
// PHP program to demonstrate the strtotime() 
// function when the english text corresponds to any 
// day 

// prints the converted english text in second 
echo strtotime("next sunday"), "\n"; 

// prints the above time in date format 
echo date("Y-m-d", strtotime("next sunday"))."\n";
?>
```

产出：

```
1525564800
2018-05-06

```

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
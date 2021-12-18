# PHP|gmp_add()加法大数

> Original: [https://www.geeksforgeeks.org/php-gmp_add-for-adding-large-numbers/](https://www.geeksforgeeks.org/php-gmp_add-for-adding-large-numbers/)

Gmp_add()是 PHP 中的一个内置函数，用于将两个 GMP 数字相加([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```
gmp_add ( $num1, $num2 )
```

**参数：**此函数接受两个 GMP 编号作为必选参数，如上面的语法所示。 它们可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以是数字字符串，前提是可以将后者转换为数字。 此函数将这两个数字相加并返回。

**返回值：**此函数返回一个 GMP 编号，它是作为参数传递的两个数字之和。

例如：

```
Input : "123456789", "987654321"
Output : 1111111110

Input : "5628179032615", "7136454221086"
Output : 12764633253701

```

以下程序说明了 PHP 中的 gmp_add()函数：

**程序 1：**

```
<?php
$sum = gmp_add("5628179032615", "7136454221086");
echo gmp_strval($sum);

?>
</div>
```

发帖主题：Re：Колибри0.7.8.0

```
12764633253701

```

**程序 2：**

```
<?php

$sum = gmp_add("123456789", "987654321");

echo gmp_strval($sum);

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1111111110

```

**引用：**
[http://php.net/manual/en/function.gmp-add.php](http://php.net/manual/en/function.gmpadd.php)
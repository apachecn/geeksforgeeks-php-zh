# 用 PHP 生成随机字符串

> 原文:[https://www . geesforgeks . org/generating-random-string-use-PHP/](https://www.geeksforgeeks.org/generating-random-string-using-php/)

使用 PHP 生成一个随机的、唯一的字母数字字符串。

示例:

```php
EA070
aBX32gTf

```

**方法 1:蛮力**
第一种方法最容易理解，因此也是蛮力。
可以通过以下方式实现:

*   将所有可能的字母存储到一个字符串中。
*   生成从 0 到字符串长度-1 的随机索引。
*   在那个索引处打印这封信。
*   执行此步骤 n 次(其中 n 是所需字符串的长度)。

**程序:**

```php
<?php
$n=10;
function getName($n) {
    $characters = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
    $randomString = '';

    for ($i = 0; $i < $n; $i++) {
        $index = rand(0, strlen($characters) - 1);
        $randomString .= $characters[$index];
    }

    return $randomString;
}

echo getName($n);
?>
```

产出 1:

```php
3HDrSOvRIs

```

产出 2:

```php
lipHh

```

**方法 2:使用散列函数**
PHP 有几个函数，像 md5()，sha1()和 hash()，可以用来基于某些算法对字符串进行散列，比如“sha1”，“sha256”，“md5”等。所有这些函数都以一个字符串作为参数，并输出一个字母数字散列字符串。

要了解这些功能的更多信息[请点击此处。](https://www.geeksforgeeks.org/php-md5-sha1-hash-functions/)

一旦我们理解了如何利用这些功能，我们的任务就变得非常简单。

*   使用 rand()函数生成一个随机数。
*   使用上述函数之一对其进行哈希运算。

**程序 1:**

```php
<?php
$str=rand();
$result = md5($str);
echo $result;
?>
```

产出 1:

```php
2e437510c181dd2ae100fc1661a445d4

```

产出 2:

```php
256394010059991a71ea05e5d859d2be

```

**程序 2:**

```php
<?php
$str=rand();
$result = sha1($str);
echo $result;
?>
```

产出 1:

```php
6eadd9b2c4389d9b109b3b869f66aab5d8f9420a

```

产出 2:

```php
ca2d3c0993ab87e842d0a7a01f319aca6c587a87

```

**程序 3:**

```php
<?php
$str = rand();
$result = hash("sha256", $str);
echo $result;
?>
```

产出 1:

```php
2a41cbc8cc11f8c8d0eb54210fe524748b4def1c5b04fcf18c2d5972e24d11c2

```

产出 2:

```php
291144c1cbba4de0bf199d37ee265ac95cc2e44e80fd2642b22a6e8ef2f42a39

```

**注意:**上述所有函数都是散列函数，因此生成的字符串长度将始终取决于所使用的算法，但对于算法来说，它将始终保持不变。因此，如果您想要生成一个固定长度的字符串，您可以根据需要截断生成的字符串或者与另一个字符串连接。

**方法三:使用 uniqid()函数。**
PHP 中的 [uniqid( )](https://www.geeksforgeeks.org/php-uniqid-function/) 函数是一个内置函数，用于根据当前时间(以微秒为单位)生成唯一的 id。默认情况下，它返回一个 13 个字符长的唯一字符串。

**程序:**

```php
<?php 
$result = uniqid();  
echo $result;
?> 
```

输出 1:

```php
5bdd0b74e9a6c 

```

输出 2:

```php
5bdd0bbc200c4   

```

**注:**以上所有方法都是建立在 rand()和 uniqid()函数上的。这些函数不是加密安全的随机生成器。因此，建议如果随机性的程度影响应用程序的安全性，则应避免使用这些方法。

**方法 4:使用 random_bytes()函数。(密码安全)**
[random _ bytes()](https://www.geeksforgeeks.org/php-random_bytes-function/)函数生成密码安全的伪随机字节，稍后可以使用 [bin2hex()](https://www.geeksforgeeks.org/php-bin2hex-function/) 函数将其转换为十六进制格式。

**程序:**

```php
<?php 
$n = 20;
$result = bin2hex(random_bytes($n));
echo $result;
?> 
```

输出 1:

```php
235aed08a01468f90fa726bd56319fb893967da8 

```

输出 2:

```php
508b84494cdf31bec01566d12a924c75d4baed39 

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
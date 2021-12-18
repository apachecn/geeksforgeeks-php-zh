# PHP|inet_ntop()函数

> Original: [https://www.geeksforgeeks.org/php-inet_ntop-function/](https://www.geeksforgeeks.org/php-inet_ntop-function/)

函数**inet_ntop()**是 PHP 中的一个内置函数，用于将 32 位 IPv4 或 128 位 IPv6 地址转换为可读格式。

**语法：**

```
*string* inet_ntop( *string* $ip_address )
```

**参数：**此函数接受一个如上所述的参数，如下所述：

*   **$IP_ADDRESS：**必选参数。 它指定 32 位 IPv4 或 128 位 IPv6 地址。

**返回值：**此函数成功时返回字符串格式的人类可读地址，失败时返回 False。

**注意：**此函数在 PHP 5.1.0 及更新版本中可用。

下面的程序演示了 PHP 中的 inet_ntop()函数：

**程序 1：**

```
<?php

// Store the address into variable
$addr = chr(127) . chr(0) . chr(1) . chr(1);

// Use inet_ntop() function to convert
// internet address to a human readable
// representation
$exp = inet_ntop($addr);

// Display result
echo $exp;

?>
```

**Output:**

```
127.0.1.1

```

**程序 2：**此程序直接在参数中使用大小为 4 的 ASCII 字符字符串。

```
<?php

// Use inet_ntop() function to convert
// internet address to a human readable
// representation
echo inet_ntop("[][]") . "<br>";
echo inet_ntop("4509") . "<br>";
echo inet_ntop("*^b@") . "<br>";
echo inet_ntop("hqp0") . "<br>";
echo inet_ntop("2c#!");

?>
```

**Output:**

```
91.93.91.93
52.53.48.57
42.94.98.64
104.113.112.48
50.99.35.33

```

**引用：**[https://www.php.net/manual/en/function.inet-ntop.php](https://www.php.net/manual/en/function.inet-ntop.php)
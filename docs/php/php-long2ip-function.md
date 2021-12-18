# PHP|Long2ip()函数

> Original: [https://www.geeksforgeeks.org/php-long2ip-function/](https://www.geeksforgeeks.org/php-long2ip-function/)

函数**Long2ip()**是 PHP 中的一个内置函数，用于将长整型转换为字符串格式的相应 IPv4 地址。

**语法：**

```
*string* long2ip( *int* $ip_in_long )
```

**参数：**此函数接受单个参数，如上所述，如下所述：

*   **$ip_in_long:** required parameter. It specifies a long integer that represents the IP address.

**返回值：**此函数返回字符串格式的 IP 地址。

**注意：**此函数在 PHP 4.0.0 及更新版本中可用。

下面的程序演示了 PHP 中的 Long2ip()函数：

**程序 1：**

```
<?php

// Use long2ip() function to converts
// long integer address into a string
// format
echo(long2ip(344294967296));
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Store the long integer address in an array
$hosts = array( 874081766, 3627733732, 3627734286,
                520968740, 2539994370, 2539979077);

$out = "List of IP addresses:";

foreach( $hosts as $host ) {

    $ip = long2ip($host);
    $hostname = gethostbyaddr($ip);

    $out .= "<br> https://" . $host . "/  https://" .
            $ip . "/  https://" . $hostname . "/";
}

echo $out;

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.long2ip.php](https://www.php.net/manual/en/function.long2ip.php)
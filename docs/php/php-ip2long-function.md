# PHP|ip2long()函数

> Original: [https://www.geeksforgeeks.org/php-ip2long-function/](https://www.geeksforgeeks.org/php-ip2long-function/)

函数**ip2long()**是 PHP 中的一个内置函数，用于将 IPv4 地址(以点分隔的 IP 地址)转换为长整数。

**语法：**

```php
*int* ip2long( *string* $ip_address )
```

**参数：**此函数接受上述单个参数，如下所述：

*   **$IP_ADDRESS：**它是指定 IP 地址的必需参数。

**返回值：**此函数成功时返回长整数，失败时返回 False。

**注：**

*   此函数在 PHP 4.0.0 和更新版本上可用。
*   此功能将用于不完整的 IP 地址。

以下程序说明了 PHP 中的 ip2long()函数：

**程序 1：**

## PHP

```php
<?php

// Store host name into variable
$host="geeksforgeeks.org";

// Get IP address from hostname
$ip = gethostbyname($host);

echo "These three URLs are equivalent:<br>";

$out = "1\. https://" . $host . "/<br>" .
       "2\. https://" . $ip . "/<br>" .
       "3\. https://" . sprintf("%u", ip2long($ip)) . "/";

echo $out;

?>
```

发帖主题：Re：Колибри0.7.0

```php
These three URLs are equivalent:
1\. https://geeksforgeeks.org/
2\. https://52.25.109.230/
3\. https://874081766/
```

**程序 2：**

## PHP

```php
<?php

// Store the list of hostname in an array
$hosts = array(
    "geeksforgeeks.org",
    "www.google.com",
    "www.youtube.com",
    "www.facebook.com",
    "www.quora.com",
    "www.stackoverflow.com"
);

$out = "Equivalent Contents:";

foreach( $hosts as $host ) {

    $ip = gethostbyname($host);

    $out .= "<br>https://" . $host . "/  https://" . $ip .
            "/  https://" . sprintf("%u", ip2long($ip)) . "/";
}

echo $out;

?>
```

发帖主题：Re：Колибри0.7.0

```php
Equivalent Contents:
https://geeksforgeeks.org/ https://52.25.109.230/ https://874081766/
https://www.google.com/ https://172.217.167.196/ https://2899945412/
https://www.youtube.com/ https://172.217.18.206/ https://2899907278/
https://www.facebook.com/ https://185.60.216.35/ https://3107772451/
https://www.quora.com/ https://151.101.1.2/ https://2539979010/
https://www.stackoverflow.com/ https://151.101.1.69/ https://2539979077/
```

**引用：**[https://www.php.net/manual/en/function.ip2long.php](https://www.php.net/manual/en/function.ip2long.php)
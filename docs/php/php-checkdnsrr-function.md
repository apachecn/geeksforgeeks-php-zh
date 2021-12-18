# PHP | checkdnsrr()函数

> 原文:[https://www.geeksforgeeks.org/php-checkdnsrr-function/](https://www.geeksforgeeks.org/php-checkdnsrr-function/)

**checkdnsrr()函数**是 PHP 中的一个内置函数，用于检查主机名或 IP 地址对应的 DNS 记录。此功能可用于验证域名是否存在。

**语法:**

```
*bool* checkdnsrr( *string* $host, *string* $type )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$host:** 必选参数。它指定要检查的主机名或 IP 地址。
*   **$type:** 为可选参数。它指定要检查的域名系统记录的类型。它的可能值有:A、AAAA、A6、ANY、CNAME、MX(默认)、NAPTR、NS、PTR、SOA、SRV、TXT。

**返回值:**如果找到记录，该函数返回真，否则返回假。

**注:**

*   此功能适用于 PHP 4.0.0 及更高版本。
*   在 Windows 平台上，这个功能可以从 PHP 5.3.0 获得。

下面的程序说明了 PHP 中的 checkdnsrr()函数:

**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$domain = "geeksforgeks.org";

if(checkdnsrr($domain, "MX")) {
    echo "Record exists.";
} else {
    echo "Record not found or error occurred.";
}
?>
```

**输出:**

```
Record exists.
```

**程序 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$domain = "geeksforgeks.org";

$arr = array(
    "A", "MX", "NS", "SOA",
    "PTR", "CNAME", "AAAA", "A6",
    "SRV", "NAPTR", "TXT", "ANY"
);

foreach( $arr as $element) {
    echo $element . ":";

    if(checkdnsrr($domain, $element)) {
        echo "found <br>";
    } else {
        echo "not found <br>";
    }
}

?>
```

**输出:**

```
A:found
MX:found
NS:found
SOA:found
PTR:found
CNAME:found
AAAA:found
A6:found
SRV:found
NAPTR:found
TXT:found
ANY:found
```

**参考:**T2https://www.php.net/manual/en/function.checkdnsrr.php
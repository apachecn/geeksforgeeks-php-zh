# PHP|DNS_CHECK_RECORD()函数

> Original: [https://www.geeksforgeeks.org/php-dns_check_record-function/](https://www.geeksforgeeks.org/php-dns_check_record-function/)

**dns_check_Records()函数**是 PHP 中的一个内置函数，用于检查与主机名或 IP 地址对应的 DNS 记录。 此函数可用于验证域名是否存在。

**注意：**此函数是 checkdnsrr()函数的别名。

**语法：**

```
*bool* dns_check_record( *string* $host, *string* $type )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$HOST：**必选参数。 它指定要检查的主机名或 IP 地址。
*   **$type：**可选参数。 它指定要检查的 DNS 记录的类型。 其可能值为：A、AAAA、A6、ANY、CNAME、MX(默认值)、NAPTR、NS、PTR、SOA、SRV、TXT。

**返回值：**如果找到记录，此函数返回 TRUE，否则返回 FALSE。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   在 Windows 平台上，PHP 5.3.0 提供此功能。

以下程序说明了 PHP 中的 dns_check_ord()函数：

**程序 1：**

## PHP

```
<?php

$domain = "geeksforgeks.org";

if(dns_check_record($domain, "MX")) {
    echo "Record exists.";
} else {
    echo "Record not found or error occurred.";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Record exists.
```

**程序 2：**

## PHP

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

    if(dns_check_record($domain, $element)) {
        echo "found <br>";
    } else {
        echo "not found <br>";
    }
}

?>
```

发帖主题：Re：Колибри0.7.0

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

**引用：**[https://www.php.net/manual/en/function.dns-check-record.php](https://www.php.net/manual/en/function.dns-check-record.php)
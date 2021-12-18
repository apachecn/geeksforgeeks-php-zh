# PHP|dns_get_mx()函数

> Original: [https://www.geeksforgeeks.org/php-dns_get_mx-function/](https://www.geeksforgeeks.org/php-dns_get_mx-function/)

**dns_get_mx()函数**是 PHP 中的内置函数，它返回指定 Internet 主机名的 MX 记录。 此函数是**getmxrr()**函数的别名。

**语法：**

```php
*bool* dns_get_mx( $host, $mxhosts, $weight );
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$host:** required parameter. It specifies the hostname whose MX record is to be found.
*   **$mxhosts:** required. Array specifies the MX hostname found.
*   **$weight:** optional parameters. An array filled with collected weight information.

**返回值：**如果找到任何记录，此函数返回 TRUE，否则返回 FALSE。

**注意：**此函数适用于 PHP 5.0.0 及更新版本。

以下程序说明了 PHP 中的**dns_get_mx()函数**：

**程序 1：**

```php
<?php

$domain = "geeksforgeeks.org";

if(dns_get_mx($domain, $mx_details)) {
    foreach( $mx_details as $key => $value) {
        echo "$key => $value <br>";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

$domain = "yahoo.com";

if(dns_get_mx($domain, $mx_details)) {
    foreach( $mx_details as $key => $value ) {
        echo "$key => $value <br>";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.dns-get-mx.php](https://www.php.net/manual/en/function.dns-get-mx.php)
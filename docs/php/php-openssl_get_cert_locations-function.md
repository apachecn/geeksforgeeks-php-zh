# PHP openssl_get_cert_locations()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_get_cert_locations-function/](https://www.geeksforgeeks.org/php-openssl_get_cert_locations-function/)

**openssl_get_cert_locations()**函数是 PHP 中的内置函数，用于获取证书位置。 此函数返回一个数组，其中包含将搜索 SSL 证书的可用证书位置的信息。

**语法：**

```php
*array* openssl_get_cert_locations( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含可用证书位置的数组。

下面的程序演示了 PHP 中的**openssl_get_cert_locations()**函数：

**示例：**

## PHP

```php
<?php

var_dump(openssl_get_cert_locations());

// openssl get cert location represent in array
return openssl_get_cert_locations();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-get-cert-locations.php](https://www.php.net/manual/en/function.openssl-get-cert-locations.php)
# PHP|Geoip_db_avail()函数

> Original: [https://www.geeksforgeeks.org/php-geoip_db_avail-function/](https://www.geeksforgeeks.org/php-geoip_db_avail-function/)

Geoip_db_avail()函数是 PHP 中的一个内置函数，用于检查 GeoIP 数据库是否可用。 该函数不考虑文件是否正确存在，而是检查该文件是否可读。

**语法：**

```php
bool geoip_db_avail( $database )
```

**参数：**此函数接受整数类型的单个参数*$database*，它需要 GeoIP 数据库(GeoIP 是指通过识别终端的 IP 地址来定位计算机终端的地理位置的方法。 GeoIP 可以将终端位置指向城市，它需要使用 GeoIP 数据库)。

**返回值：**如果成功(如果数据库存在)，此函数返回 True；如果失败(如果找不到数据库)，则返回 False；如果遇到错误，则返回 NULL。

下面的程序演示了 PHP 中的 Geoip_db_avail()函数：

**程序 1：**

```php
<?php
// PHP code implementing geoip_db_avail() function

// Checks if the database entered is valid or not
if (geoip_db_avail(GEOIP_COUNTRY_EDITION))
    echo "True";
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
// PHP code implementing geoip_db_avail() function

// Checks if the database entered is valid or not
if (geoip_db_avail(GEOIP_ORG_EDITION))
    echo "True";
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   __T0__PHP|Geoip_dB_filename()_
*   [php|GEOIP_COUNTRY_CODE_BY_NAME()函数](https://www.geeksforgeeks.org/php-geoip_country_code_by_name-function/)

**引用：**[http://php.net/manual/en/function.geoip-db-avail.php](http://php.net/manual/en/function.geoip-db-avail.php)
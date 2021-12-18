# PHP|Geoip_db_filename()函数

> Original: [https://www.geeksforgeeks.org/php-geoip_db_filename-function/](https://www.geeksforgeeks.org/php-geoip_db_filename-function/)

Geoip_db_filename()函数是 PHP 中的一个内置函数，用于生成作为参数接受的对应 GeoIP 数据库的文件名。 该函数不会指示磁盘上是否存在文件，而只是返回库在其中搜索数据库的文件名。

**语法：**

```
string geoip_db_filename ( $database )
```

**参数：**此函数接受单个参数*$database*，这是必需的。 数据库类型为整型。 下面列出了用作数据库的各种预定义常量：

*   GEOIP_ 国家/地区 _ 版本
*   GEOIP_REGION_EDITION_REV0
*   GEOIP_CITY_EDITION_REV0
*   GEOIP_ORG_EDITION
*   GEOIP_ISP_EDITION
*   GEOIP_CITY_EDITION_Rev1[T16.。 ]
*   GEOIP_ASNUM_EDITION
*   GEOIP_NETSPEED_EDITION
*   GEOIP_DOMAIN_EDITION

以下常量用于网速：

*   GEOIP_UNKNOWN_SPEED
*   GEOIP 拨号速度
*   GEOIP_CABLEDSL_SPEED
*   GEOIP_COMPOMENT_SPEED

**返回值：**此函数成功时返回对应 GeoIP 数据库的文件名，失败/错误时返回 NULL。

下面的程序演示了 PHP 中的 Geoip_db_filename()函数：

**程序 1：**

```
<?php

// PHP code implementing the geoip_db_filename() function 

// The function takes the database and returns
//  the filename according to the database
print geoip_db_filename(GEOIP_COUNTRY_EDITION);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
$arr = array(
             'GEOIP_COUNTRY_EDITION' => GEOIP_COUNTRY_EDITION,
             'GEOIP_REGION_EDITION_REV1' => GEOIP_REGION_EDITION_REV1,
             'GEOIP_PROXY_EDITION' => GEOIP_PROXY_EDITION,
             'GEOIP_ASNUM_EDITION' => GEOIP_ASNUM_EDITION,
             'GEOIP_DOMAIN_EDITION' => GEOIP_DOMAIN_EDITION,
             'EOIP_UNKNOWN_SPEED' => GEOIP_UNKNOWN_SPEED,
             'GEOIP_DIALUP_SPEED' => GEOIP_DIALUP_SPEED,
             'GEOIP_CABLEDSL_SPEED' => GEOIP_CABLEDSL_SPEED,
             'GEOIP_CORPORATE_SPEED' => GEOIP_CORPORATE_SPEED
             );

foreach ($arr as $val) {
    echo geoip_db_filename($val) . (geoip_db_avail($val) ? 'Available':'') . '<br>';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|GEOIP_COUNTRY_CODE_BY_NAME()函数](https://www.geeksforgeeks.org/php-geoip_country_code_by_name-function/)
*   [php|GeoIP_Continental_Code_by_Name()函数](https://www.geeksforgeeks.org/php-geoip_continent_code_by_name-function/)

**引用：**[http://php.net/manual/en/function.geoip-db-filename.php](http://php.net/manual/en/function.geoip-db-filename.php)
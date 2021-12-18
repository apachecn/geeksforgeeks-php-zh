# 如何用 PHP 从访客的 IP 中获取访客国家？

> 原文:[https://www . geeksforgeeks . org/如何从他们的 ip-in-php 中获取访问者国家/地区/](https://www.geeksforgeeks.org/how-to-get-visitors-country-from-their-ip-in-php/)

**概述:**要获取访客的国家、大陆、城市等详细信息，首先需要获取访客的 IP。IP 地址可以借助 PHP 中的 superglobal $_SERVER 获得。最后，通过使用应用编程接口 geoPlugin，我们可以获得关于 IP 地址的信息，即网站的访问者。

**第一步:**获取访客的 IP 地址。
$_SERVER 是一个 PHP [Superglobals](https://www.geeksforgeeks.org/php-superglobals/) 变量，它保存关于头部、IP、脚本细节等信息。像 REMOTE_ADDR、HTTP_X_REAL_IP、HTTP_CLIENT_IP 和 HTTP_X_FORWARDED_FOR 这样的元素可以用来从这个超级全局获取 IP。

**示例:**此示例获取访问者的 IP。

```php
<?php
// PHP code to extract IP 

function getVisIpAddr() {

    if (!empty($_SERVER['HTTP_CLIENT_IP'])) {
        return $_SERVER['HTTP_CLIENT_IP'];
    }
    else if (!empty($_SERVER['HTTP_X_FORWARDED_FOR'])) {
        return $_SERVER['HTTP_X_FORWARDED_FOR'];
    }
    else {
        return $_SERVER['REMOTE_ADDR'];
    }
}

// Store the IP address
$vis_ip = getVisIPAddr();

// Display the IP address
echo $vis_ip;

?>
```

**注意:**在 CloudFlare 的情况下，可能需要使用 HTTP_X_REAL_IP 这样的元素来获取 IP 地址。

**第二步:使用 API 获取访客 IP 的详细信息:**在这里，我们将使用[地理博客](https://www.geoplugin.com/) API 获取访客的详细信息。api 将提供一个 json 对象，它可以转换成一个 PHP 变量。

```php
<?php
// PHP code to obtain country, city, 
// continent, etc using IP Address

$ip = '52.25.109.230';

// Use JSON encoded string and converts
// it into a PHP variable
$ipdat = @json_decode(file_get_contents(
    "http://www.geoplugin.net/json.gp?ip=" . $ip));

echo 'Country Name: ' . $ipdat->geoplugin_countryName . "\n";
echo 'City Name: ' . $ipdat->geoplugin_city . "\n";
echo 'Continent Name: ' . $ipdat->geoplugin_continentName . "\n";
echo 'Latitude: ' . $ipdat->geoplugin_latitude . "\n";
echo 'Longitude: ' . $ipdat->geoplugin_longitude . "\n";
echo 'Currency Symbol: ' . $ipdat->geoplugin_currencySymbol . "\n";
echo 'Currency Code: ' . $ipdat->geoplugin_currencyCode . "\n";
echo 'Timezone: ' . $ipdat->geoplugin_timezone;

?>
```

**输出:**

```php
Country Name:    United States
City Name:       Boardman
Continent Name:  North America
Latitude:        45.8491
Longitude:       -119.7143
Currency Symbol: $
Currency Code:   USD
Timezone:        America/Los_Angeles

```
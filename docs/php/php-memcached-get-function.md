# PHP memcached get()函数

> Original: [https://www.geeksforgeeks.org/php-memcached-get-function/](https://www.geeksforgeeks.org/php-memcached-get-function/)

**memcached：：get()函数**是 PHP 中 memcached 类的内置函数，用于获取存储在 memcache 服务器上的给定键下的值。

**语法：**

```php
public Memcached::get( $key, 
    callable $cache_cb = ?,  $flags = ?): mixed
```

**参数**：此函数接受三个参数，它们是：

*   **键：**要检索的项的键。
*   **CACHE_CB：**直读缓存回调或 NULL。
*   **标志：**控制返回结果的标志。 当给定 memcached：：GET_EXTENDED 时，该函数还将返回 CAS 令牌。

**返回值：**返回缓存中存储的值，否则返回 False。 如果将标志设置为 memcached：：GET_EXTENDED，则返回包含该值和 CAS 标记的数组，而不是仅返回值。 如果键不存在，memcached：：getResultCode()将返回 memcached：：res_NotFound。

下面的程序演示了 PHP 中的 memcached：：set()函数：

**示例 1：**

## PHP

```php
<?php

echo "<pre>";

// Server & port details
$server = '127.0.0.1';
$port = 11211;

// Initiate a new object of memcache
$memcacheD = new Memcached();

// Add server
if ($memcacheD->addServer($server, $port)) {
    echo "**  server added ** \n";
}
else {
    echo "** issue while creating a server **\n";
}

// Set key & value with TTL
$key = "GEEKSFORGEEKS";
$value = "computer science portal";
$ttl = 3600;

if ($memcacheD->add($key, $value, $ttl)) 
    echo "** added key-value (" . $key . ":" 
    . $value . ")to cache successfully!! **\n";

else 
    echo "** error while adding value to cache!! **\n";

// Get value of key
echo "****   FETCHED VALUE   FOR KEY :" 
    . $key . " ****\n";

$valD = $memcacheD->get($key);
var_dump($valD);

?>
```

发帖主题：Re：Колибри0.7.0

> **服务器添加**
> **添加 Key-Value(GEEKSFORGEEKS：计算机科学门户)缓存成功！！**
> *获取 KEY：GEEKSFORGEEKS*
> String(23)“计算机科学门户”

**示例 2(已存储的键值)：**

## PHP

```php
<?php
echo "<pre>";

// Server & port details
$server = '127.0.0.1';
$port = 11211;

// Initiate a new object of memcache
$memcacheD = new Memcached();

// Add server
if ($memcacheD->addServer($server, $port)) {
    echo "**  server added ** \n";
}
else {
    echo "** issue while creating a server **\n";
}

// Set key & value with TTL
$key = "GEEKSFORGEEKS";
$value = "computer science portal";
$ttl = 3600;

if ($memcacheD->add($key, $value, $ttl)) 
      echo "** added key-value (" . $key . ":" 
      . $value . ")to cache successfully!! **\n";
else 
      echo "** error while adding value to cache!! **\n";

// Get value of key
echo "****   FETCHED VALUE   FOR KEY :"
      . $key . " ****\n";

$valD = $memcacheD->get($key);
var_dump($valD);

?>
```

发帖主题：Re：Колибри0.7.0

> **服务器添加了**
> **向缓存添加值时出错！！：：Msg：：Not Stored**
> *为 key：geeksforgeek*
> string(23)“计算机科学门户”提取的值列表

**引用：**[https://www.php.net/manual/en/memcached.get.php](https://www.php.net/manual/en/memcached.get.php)
# PHP memcached add()函数

> Original: [https://www.geeksforgeeks.org/php-memcached-add-function/](https://www.geeksforgeeks.org/php-memcached-add-function/)

函数**memcached：：add()函数**是 PHP 中 memcached 类的内置函数，用于在 memcache 服务器上设置/添加给定值下具有过期时间(TTL)的给定值。 此函数类似于 memcached：：set()函数，但如果密钥已存在于服务器上，则操作将失败。

**语法：**

```php
public Memcached::add( $key,  $value,  $expiration = ?): bool
```

**参数：**此函数接受三个参数，它们是：

*   **键：**存储值的键。
*   **值：**要存储的值。
*   **过期时间：**过期时间，默认为 0。 有关详细信息，请参阅过期时间。

**返回值：**如果键值对存储成功，则此函数返回 TRUE，如果存储失败，则返回 FALSE。 如果键已经存在，memcached：：getResultCode()函数将返回 memcached：：RES_NOTSTORED。

下面的示例说明了 PHP 中的 memcached：：add()函数：

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
> **添加 Key-Value(GEEKSFORGEEKS：计算机科学门户)成功！！**
> *为 Key：GEEKSFORGEEKS*
> String(23)“计算机科学门户”取值成功

**示例 2(已存在的密钥对)：**

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

**引用：**[https://www.php.net/manual/en/memcached.add.php](https://www.php.net/manual/en/memcached.add.php)
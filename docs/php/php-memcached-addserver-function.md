# PHP memcached addServer()函数

> Original: [https://www.geeksforgeeks.org/php-memcached-addserver-function/](https://www.geeksforgeeks.org/php-memcached-addserver-function/)

函数**memcached：：add()**是 PHP 中 memcached 类的内置函数，用于将服务器添加到服务器池。 它会将指定的服务器添加到服务器池中。 目前还没有建立到服务器的连接，但是如果您使用一致密钥分发选项(通过 memcached：：Distribution_consistent 或 memcached：：opt_LIBKETAMA_COMPATIBLE)，则必须更新一些内部数据结构。 因此，如果需要添加多个服务器，最好使用 memcached：：addServers()，因为更新只发生一次。

同一台服务器可能会在服务器池中多次出现，因为不会进行重复检查。 这是不可取的；相反，请使用权重选项来增加此服务器的选择权重。

**语法：**

> 公共 memcached：：addServer($host，$port，$weight=0)：bool

**参数：**此函数接受三个参数，它们是：

*   **host：**memcache 服务器的主机名。
*   **端口：**运行 memcache 的端口。 通常，这是 11211。
*   **权重：**服务器相对于池中所有服务器的总权重的权重。 用于负载均衡。

**返回值：**成功返回 TRUE，失败返回 FALSE。

下面的程序演示了 PHP 中的 memcached：：addServer()函数：

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

// Get server detail
echo "Server Details :: \n";
var_dump($memcacheD->getServerList());

?>
```

发帖主题：Re：Колибри0.7.0

> **服务器已添加**
> 服务器详细信息：：Array(1){
> [0]=>array(3){
> [“host”]=>string(9)“127.0.0.1”
> [“port”]=>int(11211)
> [“type”]=>string(3)“tcp”
> }
> }

**示例 2(创建服务器时出错：端口已使用)：**

## PHP

```php
<?php
echo "<pre>";

// Server & port details
$server = '127.0.0.1';
$port = "8000";

// Initiate a new object of memcache
$memcacheD = new Memcached();

// Add server
if ($memcacheD->addServer($server, $port)) {
    echo "**  server added ** \n";
}
else {
    echo "** issue while creating a server **\n";
}

// Get server detail
echo "Server Details :: \n"; 
var_dump($memcacheD->getServerList());

?>
```

发帖主题：Re：Колибри0.7.0

> **服务器添加**
> *创建服务器时出现问题**
> 服务器详细信息：：

**引用：**[https://www.php.net/manual/en/memcached.addserver.php](https://www.php.net/manual/en/memcached.addserver.php)
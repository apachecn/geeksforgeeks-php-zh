# PHP 内存缓存

> Original: [https://www.geeksforgeeks.org/php-memchached/](https://www.geeksforgeeks.org/php-memchached/)

每当涉及到读取时间非常短的键值存储时，缓存在系统设计中都扮演着重要的角色。 因此，为了消除数据库延迟，我们都使用了高速缓存，它有点易失性，但具有很高的可用性，并且很容易用作会话存储和类似的用例。

Memcached 是一种高速缓存，它是一种高性能的分布式内存对象高速缓存系统，本质上是通用的，但旨在通过减轻数据库负载来加速动态 Web 应用。

它与 libMemcached 配合使用，libMemcached 旨在提供最多的选项来使用 memcached。 提供的一些功能包括：

*   支持异步和同步传输。
*   一致的散列和分发。
*   匹配密钥的可调哈希算法。
*   访问大型对象支持。
*   本地复制。
*   API 的完整参考指南和文档。
*   管理 memcached 网络的工具

**在 ubuntu 上安装：**要在 ubuntu 上安装 memcached，请转到终端并键入以下命令−

```
$sudo apt-get update
$sudo apt-get install memcached
```

**示例：**

## PHP

```
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

**引用：**[https://www.php.net/manual/en/book.memcached.php](https://www.php.net/manual/en/book.memcached.php)
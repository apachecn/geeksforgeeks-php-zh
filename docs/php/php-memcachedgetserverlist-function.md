# PHP memcached：：getServerList()函数

> Original: [https://www.geeksforgeeks.org/php-memcachedgetserverlist-function/](https://www.geeksforgeeks.org/php-memcachedgetserverlist-function/)

**memcached：：getServerList()函数**是 PHP 中 memcached 类的内置函数，用于获取 memcache 服务器池中的服务器列表。

**语法：**

```
public Memcached::getServerList(): array
```

**参数：**此函数没有参数。

**返回值：**此函数返回一个包含服务器列表的数组。

下面的程序演示了 memcached：：getServerList()函数：

**示例 1：**

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

    // Get server detail
    echo "Server Details :: \n";
    var_dump($memcacheD->getServerList());
?>
```

发帖主题：Re：Колибри0.7.8.0

示例 2：(创建服务器时出错：因此没有可用的列表)

## PHP

```
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

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/book.memcached.php](https://www.php.net/manual/en/book.memcached.php)
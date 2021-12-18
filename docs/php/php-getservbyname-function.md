# PHP|getservbyname()函数

> Original: [https://www.geeksforgeeks.org/php-getservbyname-function/](https://www.geeksforgeeks.org/php-getservbyname-function/)

函数**的作用是：getservbyname()函数**是 PHP 的内置函数，它返回给定协议和 Internet 服务的端口号。

**语法：**

```php
*int* getservbyname( *string* $service, *string* $protocol )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$protocol:** required parameter. It specifies the protocol name in a string format, such as TCP, UDP, and so on.
*   **$service:** required parameters. It specifies the Internet service name, such as http int string format.

**返回值：**如果成功，则此函数返回端口号，如果未找到服务或协议，则返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

以下程序说明了 PHP 中的 getservbyname()函数：

**程序 1：**

```php
<?php

// Use getservbyname() function to get
// port number associated with an 
// Internet service and protocol
$portnum = getservbyname("http", "tcp");

// Display the result
echo $portnum;

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**此程序检查多个服务。

```php
<?php

// Create an array of services
$services = array("ftp", "ssh",
            "telnet", "http", "https");

// Loop run for each services
foreach( $services as $index) {

    // Use getservbyname() function to get
    // the port number associated with an 
    // Internet service and protocol
    echo getservbyname($index, "tcp") 
            . ": " . $index . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.getservbyname.php](https://www.php.net/manual/en/function.getservbyname.php)
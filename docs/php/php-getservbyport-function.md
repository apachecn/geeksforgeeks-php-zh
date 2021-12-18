# PHP|getservbyport()函数

> Original: [https://www.geeksforgeeks.org/php-getservbyport-function/](https://www.geeksforgeeks.org/php-getservbyport-function/)

函数**的作用是：getservbyport()函数**是 PHP 中的一个内置函数，它返回给定协议和端口号的 Internet 服务。

**语法：**

```
*string* getservbyport( *int* $port, *string* $protocol)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$protocol:** required parameter. Specify the protocol name, such as TCP, UDP, and so on.
*   **$port:** required parameter. It specifies the port number, such as 80.

**返回值：**此函数成功时返回 Internet 服务名称。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

以下程序说明了 PHP 中的 getservbyport()函数：

**程序 1：**

```
<?php

// Use getservbyport() function to get
// the Internet service which corresponds
// to port and protocol
$intservname = getservbyport(80, "tcp");

// Display the output
echo $intservname;

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create an array of port numbers
$port = array(21, 22, 23, 25, 80);

// Loop run for each services
foreach( $port as $index) {

    // Use getservbyport() function to get
    // the Internet service which corresponds
    // to port and protocol
    echo $index . ": " .getservbyport($index, "tcp")
            . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.getservbyport.php](https://www.php.net/manual/en/function.getservbyport.php)
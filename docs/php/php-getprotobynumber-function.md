# PHP|getProtobynumber()函数

> Original: [https://www.geeksforgeeks.org/php-getprotobynumber-function/](https://www.geeksforgeeks.org/php-getprotobynumber-function/)

函数**的作用是：getprotocol bynumber()函数**是 PHP 中的一个内置函数，它返回指定协议号的协议名。

**语法：**

```
*string* getprotobynumber( *int* $protocol_number )
```

**参数：**此函数接受必需的单个参数**$protocol_number**。 它指定协议号，如 6 表示 TCP，17 表示 UDP 等。

**返回值：**此函数成功时返回协议名，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

下面的程序演示了 PHP 中的 getProtobynumber()函数：

**程序 1：**此程序使用协议号作为协议名称“TCP”。

```
<?php

// The getprotobynumber() function get protocol
// name associated with protocol number 
$protocolname = getprotobynumber(6);

// Display result
echo $protocolname;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**此程序检查多个协议名称。

```
<?php

// Store the protocol number in an array
$protocol_number  = array(6, 17, 20, 41);

foreach( $protocol_number as $number ){

    // The getprotobynumber() function get protocol
    // name associated with protocol number 
    echo $number . ": " . getprotobynumber($number)
            . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.getprotobynumber.php](https://www.php.net/manual/en/function.getprotobynumber.php)
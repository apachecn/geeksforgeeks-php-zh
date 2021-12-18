# PHP|确定客户端 IP 地址

> Original: [https://www.geeksforgeeks.org/php-determining-client-ip-address/](https://www.geeksforgeeks.org/php-determining-client-ip-address/)

**什么是 IP 地址？**和
IP 地址代表网际协议地址。 IP 地址用于为联网设备提供标识。IP 地址可以精确定位连接到 Internet 的不同数字设备的位置，并将其与其他设备区分开来。

在本文中，我们讨论了从 PHP 脚本确定客户端 IP 地址的两种不同方法，如下所述：

*   **使用 getenv()函数**：要获取 IP 地址，我们使用**getenv(“Remote_ADDR”)**命令。
    PHP 中的 getenv()函数用于检索 PHP 中的环境变量的值。
    用于返回特定环境变量的值。
    **语法：**和

![](img/e738d95a141a2f841a22bcb787c91f99.png)

## PHP

```
<?php
 $ipaddress = getenv("REMOTE_ADDR") ;
 Echo "Your IP Address is " . $ipaddress;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Your IP is 127.1.1.0
```

*   **使用$_SERVER 变量方法确定 IP 地址**：还有另一种方法可以使用**$_SERVER[‘REMOTE_ADDR’]**或**$_SERVER[‘REMOTE_HOST’]**变量获取 IP 地址。 **$_server**数组中的变量由 Apache 等 Web 服务器创建，可以在 PHP 中使用。
    基本上，**$_SERVER[‘REMOTE_ADDR’]**给出了将请求发送到 Web 服务器的 IP 地址。
    **语法：**

## PHP

```
<?php
 $ipaddress = $_SERVER['REMOTE_ADDR']
 Echo "Your IP Address is " . $ipaddress;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Your IP is 127.1.1.0
```
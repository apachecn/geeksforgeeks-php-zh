# 如何在 PHP 中获取连接客户端的 MAC 和 IP 地址？

> 原文:[https://www . geesforgeks . org/如何获取 php 中已连接客户端的 mac 和 ip 地址/](https://www.geeksforgeeks.org/how-to-get-the-mac-and-ip-address-of-a-connected-client-in-php/)

**什么是 MAC 地址？**
MAC 是“媒体访问控制”的缩写，是与每台网络设备相关联的 48 位物理地址。它打印在网卡(网络接口卡)上，对于每个网络设备都是全球唯一的。数据链路层使用媒体访问控制地址将数据包从源路由到目的地。

**什么是 IP 地址？**
互联网协议(IP)地址也称为逻辑地址，由互联网服务提供商(ISP)给出，它通过网络唯一标识系统。IP 地址不断变化。

**如何在 PHP 中获取连接客户端的 IP 地址:** $_SERVER 是一个 PHP 超全局变量，它保存了关于头部、路径和脚本位置的信息。超全局变量是预定义的变量，总是可以访问的。这些超级全局变量以关联数组的形式存储信息，这里我们将获取$_SERVER 关联数组的“REMOTE_ADDR”键来获取客户端的 IP 地址。“远程 _ADDR”返回客户端的 IP 地址

**示例 1:** 此示例说明了如何使用$_SERVER['REMOTE_ADDR']获取客户端的 IP 地址。

```php
<?php

// PHP program to get IP address of client
$IP = $_SERVER['REMOTE_ADDR'];

// $IP stores the ip address of client
echo "Client's IP address is: $IP";

// Print the ip address of client
?>
```

**输出:**

```php
Client's IP address is: ::1

```

**注意:**对于在线 IDE，可能会显示运行时错误或者不会显示任何输出，因为私有域不共享其 IP。对于本地主机，IP 地址是 127.0.0.1，这是一个环回地址，因此客户端的 IP 地址是::1。

**如何在 PHP 中获取连接客户端的 MAC 地址:**exec()'是一个函数，用于在 PHP 中运行一个外部程序。它返回命令结果的最后一行。要获取媒体访问控制地址，请传递返回客户端媒体访问控制地址的参数“getmac”。“getmac”是一个获取 mac 地址的 CMD 命令。

**示例 2:** 本示例使用 exec()函数获取 MAC 地址。

```php
<?php

// PHP code to get the MAC address of Client
$MAC = exec('getmac');

// Storing 'getmac' value in $MAC
$MAC = strtok($MAC, ' ');

// Updating $MAC value using strtok function, 
// strtok is used to split the string into tokens
// split character of strtok is defined as a space
// because getmac returns transport name after
// MAC address   
echo "MAC address of client is: $MAC";
?>
```

**输出:**

```php
MAC address of client is: 00-20-10-2A-03-0A

```

**注意:**这个代码在联机 IDE 上不会工作，因为‘getmac’是一个 CMD 命令。请尝试在本地主机上运行它。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
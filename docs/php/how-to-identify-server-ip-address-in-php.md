# PHP 中如何识别服务器 IP 地址？

> 原文:[https://www . geesforgeks . org/如何识别服务器-ip-address-in-php/](https://www.geeksforgeeks.org/how-to-identify-server-ip-address-in-php/)

**什么是 IP 地址？** IP 地址或互联网协议地址是分配给网络上使用互联网协议进行通信的每个设备的数值。
一个 IP 地址有两大功能:

*   网络/主机接口标识
*   位置寻址

提供给服务器的不经常变化的静态 IP 地址。ISP 为通过调制解调器拨号的家用机器提供唯一的 IP 地址，并且该 IP 地址对于该会话是唯一的，并且它可能会在下次为该机器更改。

**如何识别你的服务器的 IP 地址:**这个$_SERVER 是 PHP 中的一个数组，包含了关于头、路径和脚本位置的信息。web 服务器自己创建这个数组的条目。虽然它不能保证每个 web 服务器都会提供这些数组的内容，但是服务器通常会省略一些$_SERVER 数组的内容。
为了获得可以使用['SERVER_ADDR']的服务器的 IP 地址，它返回当前脚本正在执行的服务器的 IP 地址。

另一种方法是在$_SERVER 数组中使用['REMOTE_ADDR']。['REMOTE_ADDR']仅用于获取本地服务器的 IP 地址，尽管生成的输出将与使用['SERVER_ADDR']获取本地服务器的 IP 地址相同。

**示例 1:** 本示例使用['服务器 _ADDR']标识服务器的 IP 地址。

```
<?php

// PHP program to obtain IP address of
// the server

// Creating a variable to store the
// server address
$ip_server = $_SERVER['SERVER_ADDR'];

// Printing the stored address
echo "Server IP Address is: $ip_server";

?>
```

**输出:**

```
Server IP Address is: ::1
```

**示例 2:** 本示例使用['REMOTE_ADDR']标识服务器的 IP 地址。

```
<?php

// PHP program to obtain IP address of
// the server

// Create a variable to store the
// server ip address
$ip = $_SERVER['REMOTE_ADDR'];

// Printing the stored address
echo "IP Address is: $ip", "<br>";

?>
```

**输出:**

```
Server IP Address is: ::1
```

**注意:**如果您尝试在任何在线 IDE 上运行上述代码，它将返回运行时错误或没有输出，因为私有域不共享其 IP，请尝试在本地主机或服务器上运行。对于 localhost，如果使用 ipv4 环回地址，则给出 127.0.0.1，如果使用 ipv6 环回地址，则给出::1。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
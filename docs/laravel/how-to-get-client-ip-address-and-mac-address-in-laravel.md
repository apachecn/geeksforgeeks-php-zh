# 如何在 Laravel 中获取客户端 IP 地址和 MAC 地址？

> 原文:[https://www . geesforgeks . org/how-to-client-IP-address-MAC-address-in-laravel/](https://www.geeksforgeeks.org/how-to-get-client-ip-address-and-mac-address-in-laravel/)

**什么是 MAC 地址？**
MAC 是“媒体访问控制”的缩写，是与每台网络设备相关联的 48 位物理地址。它打印在网卡(网络接口卡)上，对于每个网络设备都是全球唯一的。数据链路层使用媒体访问控制地址将数据包从源路由到目的地。

**如何在 Laravel 中获取连接客户端的 MAC 地址？**

“exec()”是一个函数，用 PHP 运行一个外部程序。它返回命令结果的最后一行。要获取媒体访问控制地址，请传递返回客户端媒体访问控制地址的参数“getmac”。“getmac”是一个获取 mac 地址的 CMD 命令。

要获取 MAC 地址，我们使用 exec()函数。

```php
$macAddr = exec('getmac');
```

**什么是 IP 地址？**
互联网协议(IP)地址也称为逻辑地址，由互联网服务提供商(ISP)给出，它通过网络唯一标识系统。IP 地址不断变化。

**如何在 Laravel 中获取连接客户端的 IP 地址？**

为了获得 IP 地址，我们必须包括**使用照明\ Http \ Request**然后在控制器中添加下面预标签的代码。它会给出网络的接入点地址。

```php
$ipAddr=\Request::ip();
```
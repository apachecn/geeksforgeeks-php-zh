# 如何用 PHP 获取系统的本地 IP 地址？

> 原文:[https://www . geesforgeks . org/如何使用-php 获得本地系统 ip 地址/](https://www.geeksforgeeks.org/how-to-get-local-ip-address-of-system-using-php/)

网际协议地址是网络硬件的地址。它有助于将您的计算机连接到网络上和世界各地的其他设备。一个 IP 地址由数字或字符组合而成符号。

**例:**是 IP 地址的一个例子。

```
506.457.14.512
```

所有连接到互联网的设备都有一个唯一的 IP 地址，这实际上意味着必须为每个系统创建大量的 IP 地址。

**本地 IP 地址:**这是您的计算机系统的 IP 地址，旨在保持私有，因此也称为私有 IP 地址。本文重点介绍如何提取 IP 地址。私有 IP 地址是连接到家庭或企业网络的设备的地址。如果您有几个不同的设备连接到一个 ISP(互联网服务提供商)，那么您的所有设备都将有一个唯一的私有 IP 地址。无法从家庭或企业网络之外的设备访问该 IP 地址。私有 IP 地址不是唯一的，因为您的网络上的设备数量有限。还有一些其他类型的 IP 地址，如公共 IP 地址、静态 IP 地址和动态 IP 地址，它们遵循相同的表示格式。

**IPv4 地址:**IP v4 版本用于以数字值配置 IP 地址，它使用十六进制数字系统来完成其工作，即什么使获得数百万个 IP 成为可能，每个系统都不一样。

**示例:**在本例中，我们尝试在不使用终端及其命令的情况下获取本地 IP 地址。相反，我们使用一个 PHP 程序来完成同样的工作。我们将需要下面提到的两种方法:

*   **[gethostbyname () function:](https://www.geeksforgeeks.org/php-gethostbyname-function/)** It gets the IPv4 address corresponding to a given Internet host name.
*   **[gethostname () function:](https://www.geeksforgeeks.org/php-gethostname-function/)** It gets the standard hostname of the local machine.

*   **Program:** Here, we first get the name of the local machine as a string, and then by using the string, we will get the corresponding address of the name.

    ```
    <?php

    // Declaring a variable to hold the IP
    // address getHostName() gets the name
    // of the local machine getHostByName()
    // gets the corresponding IP
    $localIP = getHostByName(getHostName());

    // Displaying the address 
    echo $localIP;

    ?>
    ```

由于安全原因，该程序不提供任何输出。共享 IP 地址可能会导致安全漏洞，应该小心不要共享。任何不道德的访问都可能导致个人空间甚至身份被盗。
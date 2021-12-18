# PHP 中的 HTTP_HOST 和 SERVER_NAME 有什么区别？

> 原文:[https://www . geesforgeks . org/http _ host-and-server _ name-in-PHP/](https://www.geeksforgeeks.org/what-is-the-difference-between-http_host-and-server_name-in-php/)区别是什么

**HTTP_HOST:** 从客户端请求获取的 HTTP 请求头中获取

**示例:**

```
Website: https://www.geeksforgeeks.org
HTTP_HOST: www.geeksforgeeks.org

```

**HTTP_SERVER:** 根据主机配置从服务器名称中提取。

**示例:**

```
Website: https://www.geeksforgeeks.org
HTTP_SERVER: Display the server name

```

| HTTP_HOST | 服务器名 |
| 它从客户端检索请求头。 | 它检索服务器配置。 |
| 它不可靠，因为它的值可以修改。 | 它更可靠，因为它的价值来自服务器配置。 |
| 语法:$_SERVER['HTTP_HOST'] | 语法:$_SERVER['SERVER_NAME'] |
| 它给出了完成请求的主机的域名。 | 它给出了主机配置中指定的服务器名称。 |
| 示例:localhost:8080 | 例子:www.google.com |
| 这是基于客户的要求。 | 它基于网络服务器的配置。 |
| 因为它与请求直接相关，所以在大多数应用程序中都使用它。 | 它根本没有给出任何关于请求的信息。 |
| 它取自目标主机。 | 它取自服务器配置。 |
| 这是客户控制的价值。 | 这是服务器控制的值 |
| http://www.google.com
HTTP _ HOST:www.google.com | http://www.google.com
HTTP _ SERVER:google.com |

**HTTP _ HOST 示例:**

```
<?php
 echo $_SERVER['HTTP_HOST']; 
?>
```

**输出:**

```
It display the host name.
```

**HTTP _ SERVER 示例:**

```
<?php
echo $_SERVER['SERVER_NAME'];
?>
```

**输出:**

```
It display the server name.
```

**注意:**在 localhost 的情况下，host 和 SERVER 名称都将相同。
# PHP | connection_status()函数

> 原文:[https://www . geesforgeks . org/PHP-connection _ status-function/](https://www.geeksforgeeks.org/php-connection_status-function/)

**connection_status()** 函数是 PHP 中的一个内置函数，返回当前的连接状态。

**语法:**

```php
*int* connection_status( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回连接状态位域。返回的连接状态位域的可能值为:

*   **0:** 连接 _ 正常–正常运行
*   T8] 1: connection _ aborted-aborted by user or network error.
*   **2:**CONNECTION _ time out–超时
*   **3:** 连接中止&连接超时–中止并超时

**注意:**此功能适用于 PHP 4.0.0 及更新版本。

下面的程序说明了 PHP 中的 **connection_status()函数**。

**节目 1:**

```php
<?php

switch (connection_status()) {
    case CONNECTION_ABORTED:
        echo'Connection aborted';
        break;
    case CONNECTION_TIMEOUT:
        echo'Connection timed out';
        break;
    case CONNECTION_NORMAL:
        echo'Connection is in a normal state';
        break;

    case (CONNECTION_ABORTED & CONNECTION_TIMEOUT):
        echo'Connection aborted and timed out';
        break;
    default:
        echo'Unknown';
        break;
}
?>
```

**输出:**

```php
Connection is in a normal state
```

**程序 2:** 在浏览器中断或关闭的情况下，一些输出将被发送到浏览器以供 **connection_status()** 工作。

```php
<?php

// This will work even if browser breaks or closed
// Sending this to client's browser
switch (connection_status()) {
    case CONNECTION_ABORTED:
        echo'Connection aborted';
        break;
    case CONNECTION_TIMEOUT:
        echo'Connection timed out';
        break;
    case CONNECTION_NORMAL:
        echo'Connection is in a normal state';
        break;

    case (CONNECTION_ABORTED & CONNECTION_TIMEOUT):
        echo'Connection aborted and timed out';
        break;
    default:
        echo'Unknown';
        break;
}
?>
```

**输出:**

```php
Connection is in a normal state

```

**参考:**[https://www . PHP . net/manual/en/function . connection-status . PHP](https://www.php.net/manual/en/function.connection-status.php)
# 什么是 PHP 中的线程安全或非线程安全？

> 原文:[https://www . geesforgeks . org/什么是 php 中的线程安全或非线程安全/](https://www.geeksforgeeks.org/what-is-thread-safe-or-non-thread-safe-in-php/)

**线程安全:**用于保证当不同线程操作的共享数据结构被阻止进入争用状态时。当 web 服务器为不同的请求同时运行多个执行线程时，建议使用线程安全。在线程安全中，二进制可以在多线程 web 服务器上下文中工作。线程安全的工作原理是在每个线程中创建一个本地存储副本，这样数据就不会与另一个线程冲突。
**例如:**

*   Apache +加载模块
*   （同 ImmigrationInspectors 移民检查）

**非线程安全:**它不检查线程的安全性，这使得它运行得更快，但同时，它变得更加不稳定，崩溃非常频繁。它仅指单线程构建。在非线程安全版本中，二进制文件在通过 FastCGI 协议与网络服务器交互的情况下被广泛使用，这是通过不使用多线程实现的。
**例如:**

*   Apache + FastCGI
*   IIS + FastCGI

所以这取决于你想用 PHP 的方式。AFAIR 用 fastCGI 运行 PHP 是更好的方法。如果你不知道你的系统中安装了哪个版本的 PHP，那么有一个简单的方法可以知道。
**检查已安装的 PHP 线程安全或非线程安全版本:**
打开一个 phpinfo()并搜索线程安全构建的线程安全行，您应该找到 enable。

*   在窗口上:

    ```php
    php -i|findstr "Thread"

    ```

*   On *nix:

    ```php
    php -i|grep Thread

    ```

*   在这两种情况下都会显示任意一个

    ```php
    Thread Safety => enabled
    //or
    Thread Safety => disabled

    ```
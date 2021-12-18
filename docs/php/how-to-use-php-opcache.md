# 如何使用 PHP OPCache？

> 原文:[https://www.geeksforgeeks.org/how-to-use-php-opcache/](https://www.geeksforgeeks.org/how-to-use-php-opcache/)

OPCache 用于提高 PHP 的性能，因为它存储了预编译的字节码，因此无需在每次请求时加载和解析 PHP 脚本。

**要求:**有目的的使用需要 Zend OPCache 等包装。zendOPCache 包包含 PHP 版本 **5.2** 、 **5.3** 和 **5.4** 。这个包用于满足操作码缓存和优化的基本需求。它将通过将预编译的字节码存储在共享内存中来提高 PHP 的性能，并且消除了从磁盘中读取代码并将其编译以备将来访问的需要。
关于 Zend OPCache 的包下载(直接下载链接):

| 版本 | 释放状态 | 环 |
| 7.0.1 | 贝塔 | [Zend opcachev 7 . 0 . 1](http://zendopcache-7.0.1.tgz (83.1kB))(83.1 kb) |
| 7.0.2 | 贝塔 | [Zend opcache v 7 . 0 . 2](http://zendopcache-7.0.2.tgz)(85.8 kb) |
| 7.0.3 | 贝塔 | [Zend opcache v 7 . 0 . 3](http://zendopcache-7.0.3.tgz)(92.0 kb) |
| 7.0.4 | 稳定的 | [Zend opcache v 7 . 0 . 4](http://zendopcache-7.0.4.tgz)(94.1 kb) |
| 7.0.5 | 稳定的 | [Zend opcache v 7 . 0 . 5](http://zendopcache-7.0.5.tgz)(94.8 kb) |

**启用 OPCache 扩展:**

*   **For PHP versions 5.2, 5.3 and 5.4**

    > As the dynamic link library (DLL) of PECL is unavailable, the installation of PECL extension can be found here [and](https://www.php.net/manual/en/install.pecl.php) .

*   **对于 PHP 版本 5.5.0 或更高版本**
    OPCache 只能编译为该版本下的共享扩展。首先，您需要使用–enable-op cache 选项来启用默认扩展的构建，以使其可用。
    之后，可以使用 [zend_extension](https://www.php.net/manual/en/ini.core.php#ini.zend-extension) 配置指令将 OP Cache 扩展导入到 PHP 中。在非 Windows 平台上使用 Zend _ extension =/full/path/to/op cache . so，在 Windows 上使用 Zend _ extension = C:\ path \ to \ PHP _ op cache . dll。

> 要将 OPCache 与 [Xdebug](https://xdebug.org/) 一起使用，需要在 Xdebug 之前加载 OPCache。

关于新版本、下载、变更日志和其他信息的信息可以在[这里](https://pecl.php.net/package/ZendOpcache)找到。

**建议 php.ini 设置:**

*   在 php.ini 文件中进行以下更改，以优化性能。

    ```php
    opcache.memory_consumption=128
    opcache.interned_strings_buffer=8
    opcache.max_accelerated_files=4000
    opcache.revalidate_freq=60
    opcache.fast_shutdown=1
    opcache.enable_cli=1
    ```

OPcache 支持的[配置指令](https://www.php.net/manual/en/opcache.configuration.php)的完整列表也是可用的。

**OPCache 功能:**

1.  **opcache_compile_file() Function:** This function is used to compile and cache a PHP script without executing it.

    **语法:**

    ```php
    *bool* opcache_compile_file( $file ) 
    ```

    该函数编译一个 PHP 脚本，并将其添加到操作码缓存中，而不执行文件，这可用于在网络服务器重启后，通过预缓存将包含在后续请求中的文件来填充缓存。**$文件**用作参数。它是要编译的 PHP 脚本的路径。如果文件编译成功，以上描述返回**真**否则返回**假**。

    **错误/异常:**对于任何错误(如果发生)，例如，在这种情况下，如果生成了级别为 **E_Warning** 的错误，请使用作为前缀的 **@** ，因为我们将其作为前缀，可能生成的错误消息可能会被忽略。
    如果调用了任何带有 set_error_handler()的自定义错误处理函数，该函数又调用了 error_reporting()，该函数在前面带有@时返回 0，这意味着该错误被忽略，程序继续执行。
    如果启用了 track_errors 功能，则表达式生成的任何错误消息都将保存在一个变量中，即$php_errormsg，如果出现任何进一步的错误，该变量将覆盖这些错误。此外，如果您想使用这个变量，可以尽早检查它。

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```php
    <?php

    // Intentional file error
    $my_file = @file('non existent file') 
    or die("Failed opening file, error was : '$php_errormsg'" );

    // This works for any expression, not just functions
    $value = @$cache[$key];
    ?>
    ```
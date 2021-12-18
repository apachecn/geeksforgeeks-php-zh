# PHP . ini 文件的目的是什么？

> 原文:[https://www . geesforgeks . org/PHP-ini-file 的目的是什么/](https://www.geeksforgeeks.org/what-is-the-purpose-of-php-ini-file/)

在本文中，我们将了解 php.ini 文件的用途。在 PHP 安装时， **php.ini** 是作为默认配置文件提供的特殊文件。
T3】目的

*   这是一个非常重要的配置文件，它控制用户可以或不可以对网站做什么。
*   每次初始化 PHP 时，系统都会读取 php.ini 文件。
*   有时候你需要在运行时改变 PHP 的行为，那么这个配置文件就可以使用了。
*   与注册全局变量、上传最大大小、显示日志错误、资源限制、执行 PHP 脚本的最长时间等相关的所有设置都作为一组有助于声明更改的指令写入文件。
*   php.ini 文件是运行需要 php 的应用程序的默认配置文件。它用于控制变量，如上传大小、文件超时和资源限制。
*   php.ini 文件是配置文件。当服务器启动或模块中的 HTTP 重新启动时，它总是被检查，并且它配置网站以知道用户可以对网站做什么或不可以做什么。
*   它还有助于轻松管理 web 服务器。

**注:**

*   每当对文件进行一些更改时，您都需要重新启动 web 服务器。

*   使用这些配置文件有助于服务器轻松管理 web。我们还可以编写自己的自定义配置文件。

要检查文件路径，请使用以下程序:

```php
<?php

echo phpinfo();

?>
```

**注意:**文件中的关键字区分大小写，关键字值不是空格，以分号开头的行被忽略。这个文件评论得很好。布尔值由**开/关、1/0、真/假、是/否**表示

该文件包含一组指令以及分配给它的一组相应的值。这些值可以是字符串、数字、PHP 常量、INI 常量或表达式、带引号的字符串或对先前设置的变量的引用。INI 文件中的表达式仅限于按位运算符或括号。具有特定主机名的设置将仅在该特定主机下工作。

**PHP . ini 文件的环境变量:**

*   **memory_limit:** 此设置用于显示脚本消耗的最大内存量。

**PHP . ini 文件的重要设置或常用参数:**

*   **enable_safe_mode =** on 每当编译 PHP 时，其默认设置为 on。安全模式与 CGI 的使用最为相关。
*   **register_globals =** 关于其默认设置为 on，这意味着 EGPCS(环境、GET、POST、Cookie、Server)变量的内容被注册为全局变量。但是由于安全风险，用户必须确保它是否为所有脚本设置了 OFF。
*   **upload_max_filesize** 此设置用于脚本中上传文件的最大允许大小。
*   **upload_tmp_dir = [DIR]** 不要取消对该设置的注释。
*   **post_max_size** 此设置是针对 PHP 将接受的 post 数据的最大允许大小。
*   **display_errors =** off 此设置不允许在指定主机上运行 PHP 项目时显示错误。
*   **报错= E_ALL & ~E_NOTICE:** 该设置有 E_ALL 和~E_NOTICE 等默认值，显示除 NOTICE 以外的所有错误。
*   **error _ prepend _ string =[" "]**此设置允许您制作不同颜色的消息。
*   **max_execution_time = 30** 任何脚本的最大执行时间都设置为秒，以限制在生产服务器上的时间。
*   **short_open_tags = Off** 要使用 XML 函数，我们必须将该选项设置为 Off。
*   **session . save-handler = files**您不需要在此设置中更改任何内容。
*   **变量 _ 顺序= EGPCS** 这个设置是为了设置变量的顺序为 Environment、GET、POST、COOKIE、SERVER。开发人员也可以根据需要更改订单。
*   **warn _ plus _ overload = Off**如果+与值形式的字符串一起使用，该设置会发出警告。
*   **gpc_order =** gpc 此设置已被 GPC 弃用。
*   **magic_quotes_gpc =** on 此设置是在使用许多表单的情况下完成的，这些表单向自己或他人提交并显示表单值。
*   **magic_quotes_runtime = Off** 如果 magic_quotes_sybase 设置为 On，则必须关闭。此设置不使用引号。
*   **magic_quotes_sybase = off** 如果设置为 Off，则应该为 Off。此设置不使用引号。
*   **自动前置文件=[文件路径** ]当我们需要在每个 PHP 文件的开头自动包含()它时，这个设置就完成了。
*   **自动追加文件=[文件路径]** 当我们需要在每个 PHP 文件的末尾自动包含()它时，这个设置就完成了。
*   **include_path = [DIR** ]当我们需要从指定目录中获取文件时，会进行此设置。使用冒号设置多个目录。
*   **ignore _ user _ abort =[开/关]** 这些设置控制当用户单击任何停止按钮时会发生什么。默认值是该设置在 CGI 模式下不起作用，它只在模块模式下起作用。
*   **doc_root = [DIR]** 如果我们想将 PHP 应用到我们网站的一部分，那么这个设置就完成了。
*   **file_uploads = [on/off]** 如果 PHP 代码中包含文件上传，则该标志设置为 on。
*   **mysql . default _ host****= hostname**如果没有提到其他服务器主机，则此设置用于连接到 MySQL 默认服务器。
*   **mysql . default _ user**=**username**这个设置是为了连接到一个 MySQL 的默认用户名，如果没有提到其他名字的话。
*   **mysql . default _ password**=**password**如果没有提到其他密码，这个设置是用来连接 MySQL 默认密码的。

**php . ini 文件的配置:**每当我们安装 PHP 的时候，都可以在 PHP 文件夹里面找到配置文件。如果使用 xampp，我们可以在路径“\xampp\php”中找到一个或多个版本的配置文件。

**注意:**这个文件的其他版本是 php.ini-development 和 php.ini-production。最优选的是 php.ini-development 文件。
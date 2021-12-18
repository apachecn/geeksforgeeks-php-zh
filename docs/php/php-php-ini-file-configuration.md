# 加入时间：清华大学 2007 年 01 月 25 日下午 3：33

> Original: [https://www.geeksforgeeks.org/php-php-ini-file-configuration/](https://www.geeksforgeeks.org/php-php-ini-file-configuration/)

在 PHP 安装时，**php.ini**是作为默认配置文件提供的特殊文件。 这是一个非常重要的配置文件，它控制用户可以或不可以对网站做什么。 每次初始化 PHP 时，系统都会读取**php.ini**文件。 有时您需要在运行时更改 PHP 的行为，然后使用此配置文件。

所有与注册全局变量、上传最大大小、显示日志错误、资源限制、执行 PHP 脚本的最长时间等相关的设置都作为一组指令写入到一个文件中，这有助于声明更改。

**注意：**每当在文件中执行某些更改时，您都需要重新启动我们的 Web 服务器。

它有助于使用这些配置文件轻松管理 Web 服务器。 我们还可以编写自己的自定义配置文件。

**要检查文件路径，请使用以下程序：**

```php
<?php
echo phpinfo();
?>
```

**注意：文件中的**键区分大小写，关键字值不是空格，以分号开头的行将被忽略。 这份文件有很好的注释。 布尔值由**开/关、1/0、真/假、是/否**表示。

该文件包含一组指令，并为其分配了一组相应的值。 这些值可以是字符串、数字、PHP 常量、INI 常量，也可以是表达式、带引号的字符串或对先前设置的变量的引用。 INI 文件中的表达式仅限于位运算符或圆括号。 具有特定主机名的设置仅在该特定主机下有效。

***php.ini*文件的环境变量：**

*   **MEMORY_LIMIT:** this setting is performed to show the maximum amount of memory consumed by the script.

**php.ini 文件的重要设置或常用参数：**

1.  **ENABLE_SAFE_MODE=ON** whenever PHP is compiled, its default setting is ON. Safe mode is most relevant to the use of CGI.
2.  **REGISTER_GLOBALS=ON** is set to ON by default, indicating that the contents of the EGPCS (Environment, Get, POST, Cookie, Server) variable are registered as global variables. However, due to security risks, users must ensure that all scripts are set to OFF.
3.  **Upload_max_filesize** this setting is used for the maximum size of the uploaded file allowed in the script.
4.  **Upload_tmp_dir= [Dir]** do not uncomment this setting.
5.  **POST_MAX_SIZE** this setting is used for the maximum allowable size of POST data that PHP can accept.
6.  **DISPLAY_ERROR=OFF** this setting does not allow errors to be displayed when running PHP projects on the specified host.
7.  **ERROR_REPORTING=E_ALL & ~ E_NOTICE:** the default values for this setting are E_ALL and ~ E_NOTICE, which displays all errors except notifications.
8.  **ERROR_PAREND_STRING= ["]** this setting allows you to set different message colors.
9.  **max_ecution_time=30** sets the maximum execution time of any script to seconds to limit the time in the production server.
10.  **SHORT_OPEN_TAG=OFF** to use the XML function, we must set this option to *OFF.*
11.  **session.save-handler=files** you do not need to change anything in this setting.
12.  **Variables_Order=EGPCS** this setting is used to set the order of variables to Environment, GET, POST, Cookie, SERVER. Developers can also change orders as needed.
13.  **WARN_PLUS_OVERLOADING=OFF** this setting warns when + is used with a string in the form of a value.
14.  **GPC_ORDER=GPC** this setting has been deprecated by GPC.
15.  **MAGIC_QUOTES_GPC=ON** perform this setting if you use many forms that are submitted to yourself or others and display form values.
16.  **MAGIC_QUOTES_RUNTIME=OFF** if MAGIC_QUOTES_SYBASE is set to ON, this setting must be OFF, which is escaped quotation marks.
17.  **MAGIC_QUOTES_SYBASE=OFF** if this setting is set to OFF, it should be OFF, which is escaped quotation marks.
18.  **AUTO-PAREND-FILE= [filepath]** this setting is performed when we need to automatically *INCLUDE ()* at the beginning of each PHP file.
19.  **AUTO-APPEND-FILE= [filepath]** this setting is performed when we need to automatically *INCLUDE ()* at the end of each PHP file.
20.  **INCLUDE_PATH= [DIR]** this setting is performed when we need to specify files in the directory. Use colons to set up multiple directories.
21.  **IGNORE_USER_ABORT= [on / OFF]** this setting controls what happens when the user clicks any stop button. The default value is on. This setting does not work in CGI mode, it only works in module mode.
22.  **doc_root= [DIR]** perform this setting if we want to apply PHP to part of the website.
23.  **FILE_UPLOADS= [on / OFF]** if the PHP code contains file uploads, this flag is set to *on.*
24.  **mysql.default_host=hostname** if no other server host is mentioned, this setting is performed to connect to the MySQL default server.
25.  **mysql.default_user=username** if no other name is mentioned, this setting is performed to connect to the MySQL default user name.
26.  **mysql.default_password=password** if no other password is mentioned, perform this setting to connect to the MySQL default password.

**php.ini 文件的配置：**每当我们安装 PHP 时，我们都可以在 PHP 文件夹中找到配置文件。 如果使用 xampp，我们可以在路径*‘\xampp\php’中找到一个或多个版本的配置文件。*

**注意：**该文件的其他版本是***php.ini-Development***和***php.ini-Production***。 最受欢迎的是***php.ini-Development***文件。
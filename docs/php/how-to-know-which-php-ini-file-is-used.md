# 如何知道使用的是哪个 php.ini 文件？

> 原文:[https://www . geesforgeks . org/how-know-哪个-PHP-ini-file-is-use/](https://www.geeksforgeeks.org/how-to-know-which-php-ini-file-is-used/)

**php.ini** 文件是用于运行需要 php 的应用程序的默认配置文件。这是处理 PHP 功能的有效方法。它用于控制变量，如文件超时、上传的大小以及它所使用的资源的限制。

**1。检查 CGI(公共网关接口)中的 php.ini:**这里，我们可以使用两个内置函数来获取使用了哪个 PHP . ini。

*   **php_ini_loaded_file:** 它检索一个指向加载的 php.ini 文件的路径。

    ## 服务器端编程语言(专业超文本预处理器的缩写)

    ```
    <?php
    $php_inipath = php_ini_loaded_file();

    if ($php_inipath) {
        echo 'Loaded php.ini is: ' . $php_inipath;
    } else {
        echo 'A php.ini file is not loaded';
    }
    ?>
    ```

*   **php_ini_scanned_files:** 它返回一个。从附加 ini 目录解析的 ini 文件。

    ## 服务器端编程语言(专业超文本预处理器的缩写)

    ```
    <?php
    if ($list_of_files = php_ini_scanned_files()) {
        if (strlen($list_of_files) > 0) {
            $files = explode(', ', $list_of_files);

            foreach ($files as $file) {
                echo "<li>" . trim($file) . "</li>\n";
            }
        }
    }
    ?>
    ```

**2。在 CLI(命令行界面)中查看 php.ini:**要了解 PHP . ini，只需在 CLI 上运行即可。

```
php --ini
```

它会在输出中查找命令行界面使用的 php.ini 的加载配置文件。

**注意:**如果我们从 CLI 运行一个 PHP 脚本，可能会使用与服务器(即 apache 或 Nginx)运行不同的 php.ini 文件。

**3。了解 php.ini 的其他选项:**

*   php -i|grep 'php.ini'
*   只需在 web 根目录下创建“information.php”文件并添加代码(如下)，然后在浏览器中运行它。

    ```
    <?php 
    phpinfo(); 
    ?>
    ```
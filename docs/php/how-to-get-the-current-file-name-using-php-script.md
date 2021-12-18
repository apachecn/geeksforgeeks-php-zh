# 如何用 PHP 脚本获取当前文件名？

> 原文:[https://www . geesforgeks . org/如何使用 php 脚本获取当前文件名/](https://www.geeksforgeeks.org/how-to-get-the-current-file-name-using-php-script/)

在本文中，我们将学习如何使用 PHP 获取当前文件名。

```
Input : c:/xampp/htdocs/project/home.php
Output : project/home.php

Input : c:/xampp/htdocs/project/abc.txt
Output : project/abc.txt
```

有时，出于不同的目的，我们需要获取当前文件名和存储页面的目录名。由于我们使用的是 PHP，所以我们可以通过使用$_SERVER['SCRIPT_NAME']轻松获取当前页面的当前文件名或目录名。

**使用$ _ SERVER[' SCRIPT _ NAME ']:**$ _ SERVER 是存储信息的数组，如标题、路径和脚本位置。这些条目由 web 服务器创建。没有其他方法可以让每个网络服务器都提供这些信息。

**语法:**“SCRIPT _ NAME”**给出了从根目录到包含目录名的路径。**

***   Get the current file name. We use

    ```
    $currentPage= $_SERVER['SCRIPT_NAME'];
    ```

    *   To display the current file name. We use

    ```
    echo $currentPage;
    ```** 

****PHP 代码:**下面是用目录名获取当前文件名的完整代码。**

 **## PHP

```
<?php 

// To Get the Current Filename.
$currentPage= $_SERVER['SCRIPT_NAME'];

// To Get the directory name in 
// which file is stored.
$currentPage = substr($currentPage, 1);

// To Show the Current Filename on Page.
echo $currentPage; 

?>
```** 

****输出:****

```
 project/home.php
```

**在这段代码中， [substr()](https://www.geeksforgeeks.org/php-substr-function/) PHP 函数用于从$currentPage 变量字符串中提取字符串的部分。**
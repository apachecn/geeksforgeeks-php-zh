# 如何在一个 PHP 脚本中导入 config.php 文件？

> 原文:[https://www . geesforgeks . org/how-import-config-PHP-file-in-a-PHP-script/](https://www.geeksforgeeks.org/how-to-import-config-php-file-in-a-php-script/)

PHP 中的 **include** 语句将上述文件中的文本代码复制到使用 include 语句的文件中。它指示预处理器将指定的内容插入到下面的程序中。要包含的文件名用双引号引起来。将基本的数据库细节和用户细节写在一个名为**“config . PHP”**的文件中是一个很好的做法。您也可以在**config.php**文件中包含连接建立语句，以便为包含**config.php**文件的每个页面自动建立到数据库的连接。包含文件允许您形成网站多个页面所需的代码模板。

**语法:**

```php
<?php
   include('config.php');
?>
```

**示例 1:** 这显示了 config.php 文件的创建和包含。

*   **代码 1:** 创建一个 PHP 文件，并以“config.php”的名称保存。

    ```php
    <?php
       $host = 'localhost';
       $database = 'GeeksForGeeks';
       $username = 'admin';
       $password = '';
    ?>
    ```

*   **代码 2:** 创建一个 PHP 文件，并以“try.php”的名称将其保存在与“config.php”文件相同的文件夹中。复制下面的代码以包含“config.php”文件，并打印数据库的名称和用户名。

    ```php
    <?php
       include('config.php');
       echo "Host: ".$host." Database: ".$database;
    ?>
    ```

*   **输出:**
    ![](img/8083c076194cd3dc22674aaebd8c8cca.png)

**示例 2:** 如果您想将 config.php 文件的内容保存到一个变量中，那么下面的代码可以做到。

*   **代码 1:** 只需返回“config.php”文件的内容。

    ```php
    <?php
       return [
       'host' => 'localhost2',
       'database' => 'GeeksForGeeks2',
       'username' => 'admin',
       'password' => ''
       ];
    ?>
    ```

*   **代码 2:** 接受变量中返回的数组。

    ```php
    <?php
       $details = include('config.php');
       echo 'Host: ' . $details['host'] . 
            ' Database: ' . $details['database'];
    ?>
    ```

*   **输出:**
    ![window2](img/175e7c5416796308ef8659620586affc.png)
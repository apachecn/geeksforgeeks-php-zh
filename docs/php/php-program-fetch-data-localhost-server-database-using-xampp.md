# 使用 XAMPP

从本地主机服务器数据库获取数据的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-fetch-data-localhost-server-database-using-xampp/](https://www.geeksforgeeks.org/php-program-fetch-data-localhost-server-database-using-xampp/)

**[XAMPP](https://en.wikipedia.org/wiki/XAMPP)**是由 Apache 开发的免费开源跨平台 Web 服务器解决方案堆栈软件包，允许在本地 Web 服务器上轻松测试 Web 应用程序。 在这里，我们可以手动创建[关系数据库](http://searchsqlserver.techtarget.com/definition/relational-database)，并通过转到[这个](http://localhost/phpmyadmin/)链接以表格形式存储数据。 但要在本地主机上操作或存储数据，我们必须首先从 XAMPP 控制面板启动 Apache 和 MySQL。

例如，数据库名为*server*，表名为*user_info*，列名为*ID*，*First Name*，*UserName*和*Password*，我们必须获取存储在那里的数据。 因此，下面是任务是获取数据的 PHP 程序。

```php
<?php
// this php script is for connecting with database
// data have to fetched from local server
$mysql_host = 'localhost';

// user name is root
$mysql_user = 'root';

// function to connect with database having 
// argument host and user name
if (!@mysql_connect ($mysql_host, $mysql_user))
{
    die('Cannot connect to database');
}
else
{
    // database name is server
    if (@mysql_select_db('server'))
    {
        echo "Connection Success";
    }
    else
    {
        die('Cannot connect to database');
    }
}
?>
```

产出：

```php
Connection Success

```

让上面的脚本以名称*database ase.php*保存在 XAMPP 安装的 htdocs 文件夹中。

```php
<?php
// going to use above code
require 'database.php';

// printing column name above the data
echo 'ID'.' '.'Name'.' '.'User'.' '.'Pass'.'<br>';

// sql query to fetch all the data
$query = "SELECT * FROM `user_info`";
// mysql_query will execute the query to fetch data
if ($is_query_run = mysql_query($query))
{
    // echo "Query Executed";
    // loop will iterate until all data is fetched
    while ($query_executed = mysql_fetch_assoc ($is_query_run))
    {
        // these four line is for four column
        echo $query_executed['ID'].' ';
        echo $query_executed['First Name'].' ';
        echo $query_executed['Username'].' ';
        echo $query_executed['Password'].'<br>';
    }
}
else
{
    echo "Error in execution";
}
?>
```

帖子主题：Re：Колибри

有关安装和使用 XAMPP 的信息，请参考[此](https://www.youtube.com/watch?v=3lfWcIWrHtc&list=PLS1QulWo1RIZc4GM_E04HCPEd_xpcaQgg&index=2)链接。

本文由[Aditya Kumar](https://www.linkedin.com/in/aditya-kumar-837315100/)贡献。 如果你喜欢 GeeksforGeek 并想投稿，你也可以使用[Contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章，或者把你的文章邮寄到 Contribute@geeksforgeeks.org。 看看你的文章出现在 GeeksforGeek 主页上，并帮助其他 Geek。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的主题的信息，请写下评论。
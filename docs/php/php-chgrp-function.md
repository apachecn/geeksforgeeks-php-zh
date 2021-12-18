# PHP | chgrp()函数

> 原文:[https://www.geeksforgeeks.org/php-chgrp-function/](https://www.geeksforgeeks.org/php-chgrp-function/)

PHP 中的 chgrp()函数是一个内置函数，用于更改指定文件的用户组。成功时返回真，失败时返回假。只有超级用户有权任意改变文件的组。

**语法:**

```
bool chgrp ( $filename, $group )
```

**参数:**PHP 中的 chgrp()函数接受两个参数，即文件名和用户。

1.  **$filename** :指定要更改用户组的文件。
2.  **$group** :指定新的用户组。它可以是组名或号码。

**返回值:**chgrp()函数成功返回真，失败返回假。
**错误和异常** :

1.  PHP 中的 chgrp()函数不适用于远程文件。它只对服务器文件系统可访问的文件起作用。
2.  当启用安全模式时，PHP 检查正在操作的文件或目录是否与正在执行的脚本拥有相同的所有者。

**例:**

```
Input : chgrp("gfg.txt", "administrator")
Output :true

Input : $filename = "/user/Desktop/geeksforgeeks/gfg.txt";
        chgrp( $filename, "guest" );
Output :true

```

以下程序说明了 chgrp()功能:
**程序 1** :

```
<?php

// changes the file group to administrator
chgrp("gfg.txt", "administrator")

?>
```

输出:

```
true
```

**节目 2** :

```
<?php

// Changes the file group to guest
$filename = "/user/Desktop/geeksforgeeks/gfg.txt";

chgrp ( $filename, "guest" );

chown($path, $user_name); 

?>
```

输出:

```
true

```

**参考:**T2[http://php.net/manual/en/function.chgrp.php](http://php.net/manual/en/function.chgrp.php)
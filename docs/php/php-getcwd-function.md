# PHP|getcwd()函数

> Original: [https://www.geeksforgeeks.org/php-getcwd-function/](https://www.geeksforgeeks.org/php-getcwd-function/)

PHP 中的 getcwd()函数是一个内置函数，用于返回当前工作目录。 此函数不接受任何参数，函数调用成功时返回当前工作目录，调用失败时返回 False。

**语法：**

```php
getcwd()
```

**参数**：此函数不接受任何参数。

**返回值：**函数调用成功时返回当前工作目录，函数调用失败时返回 False。

**错误和异常**：

1.  如果父目录中的任何一个没有设置可读或搜索模式，则在某些 Unix 变体上，getcwd()将返回 False。
2.  如果您尝试在符号链接的目录中使用 getcwd()，则 getcwd()会提供该链接的目标。

以下程序说明了 getcwd()函数：

**程序 1：**

```php
<?php

//current directory
$cur_dir = getcwd();

// displaying current directory
echo $cur_dir ; 
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
//current directory
 $cur_dir = getcwd();

echo("Current Directory is " . $cur_dir);

echo "<br>" ;

//changing current directory
$flag = chdir("user/home/articles");

if($flag == true) 
{ 
$cur_dir = getcwd();
echo("Directory Has Been Successfully Changed to " . $cur_dir);
}
else
{
echo("Failed to Change Directory.");
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.getcwd.php](http://php.net/manual/en/function.getcwd.php)
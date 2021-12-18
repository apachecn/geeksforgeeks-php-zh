# PHP|rmdir()函数

> Original: [https://www.geeksforgeeks.org/php-rmdir-function/](https://www.geeksforgeeks.org/php-rmdir-function/)

PHP 中的 rmdir()函数是一个内置函数，用于删除空目录。 该目录必须为空，并且必须具有删除该目录所需的相关权限。
要删除的目录作为参数发送给 rmdir()函数，成功时返回 True，失败时返回 False。

**语法：**

```php
rmdir(dirname, context)
```

**使用的参数：**
PHP 中的 rmdir()函数接受两个参数。

1.  **目录名称：**这是一个必选参数，指定要删除的目录。
2.  **上下文：**这是一个可选参数，指定流的行为。

**返回值：**
成功时返回 True，失败时返回 False。

**错误和异常**

1.  函数的作用是：在失败时生成 E_WARNING 级别的错误。
2.  在使用 rmdir()函数之前，必须关闭 opendir()，否则会出现权限被拒绝错误。
3.  PHP 检查运行脚本的目录是否与处于安全模式时执行的脚本具有相同的 UID(所有者)。

例如：

```php
Input : mkdir('gfg');
        $dirname= "gfg";
        rmdir($dirname);
Output : 1

Input : $dirname = "gfg";
        if(rmdir($dirname))
        {
          echo ("$dirname successfully removed");
        }
        else
        {
          echo ("$dirname couldn't be removed"); 
        }
Output : gfg successfully removed

```

下面的程序说明了 rmdir()函数。

**程序 1**

```php
<?php
// creating a directory named gfg
mkdir('gfg');
$dirname= "gfg";

// removing directory using rmdir()
rmdir($dirname);
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2**

```php
<?php
// creating a directory named gfg
 $dirname = "gfg";

// removing directory using rmdir()
if(rmdir($dirname))
{
  echo ("$dirname successfully removed");
}
else
{
 echo ($dirname . "couldn't be removed"); 
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg successfully removed
```

**引用：**
[http://php.net/manual/en/function.rmdir.php](http://php.net/manual/en/function.rmdir.php)
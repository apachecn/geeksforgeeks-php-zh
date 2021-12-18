# PHP|mkdir()函数

> Original: [https://www.geeksforgeeks.org/php-mkdir-function/](https://www.geeksforgeeks.org/php-mkdir-function/)

Mkdir()创建一个具有指定路径名的新目录。 路径和模式作为参数发送给 mkdir()函数，成功时返回 TRUE，失败时返回 FALSE。
在 Windows 平台上忽略 mkdir()函数中的**mode**参数。

**语法：**

```php
mkdir(path, mode, recursive, context)
```

**使用的参数：**
PHP 中的 mkdir()函数接受四个参数。

1.  **路径：**必选参数，指定路径。
2.  **mode :** It is an optional parameter which specifies permission.
    The mode parameter consists of four numbers:
    *   第一个数字始终为零。
    *   第二个数字指定所有者的权限。
    *   第三个数字指定所有者的用户组的权限。
    *   第四个数字指定其他所有人的权限。

    可能的值集包括：

    *   1=执行权限
    *   2=写入权限
    *   4=读取权限

    通过将以下数字相加，可以设置多个权限。

3.  **递归：**可选参数，用于设置递归模式。
4.  **上下文：**这是一个可选参数，指定流的行为。

**返回值：**
成功返回 TRUE，失败返回 FALSE。

**错误和异常：**

1.  Mkdir()函数中的模式参数必须以八进制表示形式指定，使其以零开头。
2.  如果目录已存在，则会生成 E_WARNING 级别错误。
3.  如果相关权限阻止创建目录，则会生成 E_WARNING 级别错误。

例如：

```php
Input : mkdir("/documents/gfg/articles/");
Output : 1

Input : mkdir("/documents/gfg/articles/", 0770)
Output : 1

Input : $nest = './node1/node2/node3/';
        if (!mkdir($nest, 0777, true)) 
        {
          echo('Folders cannot be created recursively');
        }
        else
        {
          echo('Folders created recursively');
        }

Output : Folders created recursively

```

下面的程序演示了 mkdir()函数。

**程序 1**

```php
<?php 
// making a directory with default mode i.e 0777
mkdir("/documents/gfg/articles/");
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2**

```php
<?php 
// making a directory with the provision of all
// permissions to the owner and the owner's user group
mkdir("/documents/gfg/articles/", 0770)
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 3**

```php
<?php 
$nest = './node1/node2/node3/';
// creating a nested structure directory
if (!mkdir($nest, 0777, true)) 
  {
     echo('Folders cannot be created recursively');
  }
else
  {
     echo('Folders created recursively');
  }
?>
```

发帖主题：Re：Колибри0.7.0

```php
Folders created recursively
```

相关文章：[PHP|rmdir()函数](https://www.geeksforgeeks.org/php-rmdir-function/)

**引用：**
[http://php.net/manual/en/function.mkdir.php](http://php.net/manual/en/function.mkdir.php)
# PHP|link()函数

> Original: [https://www.geeksforgeeks.org/php-link-function/](https://www.geeksforgeeks.org/php-link-function/)

Link()为指定目标创建[硬链接](https://www.geeksforgeeks.org/soft-hard-links-unixlinux/)。 目标和链接作为参数传递给 link()函数，成功时返回 TRUE，失败时返回 FALSE。
**语法：**

```php
link(target, link)
```

> **使用的参数：**和
> PHP 中的 link()函数接受两个参数。
> 
> 1.  **目标：**指定目标的必选参数。
> 2.  **link：**它是指定链接名称的必选参数。
> 
> **返回值：**和
> 成功时返回 TRUE，失败时返回 FALSE。

**错误和异常：**

1.  Link()函数对远程文件无效，因为要检查的文件必须可以通过服务器的文件系统访问。
2.  Link()函数创建的链接不是 HTML 链接，而是文件系统中的链接。
3.  在 Linux 中，不允许硬链接到目录。

**示例：**

```php
Input : $targetfile = 'gfg.txt.'; 
        $linkname = 'gfglink';
        link($targetfile, $linkname);
Output : 1

Input : $targetfile = 'gfg.txt.'; 
        $linkname = 'gfglink';

        if(!link($targetfile, $linkname))
        {
           echo('Link has been created!');
        }
        else
        {
          echo('Link cannot be created!');
        }
Output : Link has been created!
```

下面的程序说明了 link()函数。
**程序 1**

## PHP

```php
<?php
// target file
$targetfile = 'gfg.txt';

// name of the link
$linkname = 'gfglink';

// creating a symbolic link for the target file
link($targetfile, $linkname);
?>
```

**输出：**

```php
1
```

**程序 2**

## PHP

```php
<?php

// target file
$targetfile = 'gfg.txt';

// name of the link
$linkname = 'gfglink';

// creating a symbolic link for the target file
if(!link($targetfile, $linkname))
 {
    echo('Link has been created!');
 }
else
 {
    echo('Link cannot be created!');
 }
?>
```

**输出：**

```php
Link has been created!
```

**相关文章：**[php|symlink()函数](https://www.geeksforgeeks.org/php-symlink-function/)
**参考：**http://php.net/manual/en/function.link.php
# PHP|pasinfo()函数

> Original: [https://www.geeksforgeeks.org/php-pathinfo-function/](https://www.geeksforgeeks.org/php-pathinfo-function/)

Pasinfo()是一个内置函数，用于使用关联数组或字符串返回有关路径的信息。
返回的数组或字符串包含以下信息：

*   **目录名**
*   **基名**
*   **扩展**

路径和选项作为参数发送给 pasinfo()函数，如果没有传递**Options 参数**，它将返回一个包含以下元素目录名、基名和扩展名的关联数组。
**语法：**

```php
pathinfo(path, options)
```

**使用的参数：**和
PHP 中的 pasinfo()函数接受两个参数。

1.  **路径：**必选参数，指定文件的路径。
2.  **选项：**这是一个可选参数，可用于限制 pasinfo()函数返回的元素。 默认情况下，它返回所有可能的值，包括目录名、基本名称、扩展名。
    可能的值可以使用以下命令进行限制：
    *   PATHINFO_DIRNAME-仅返回目录名
    *   PATHINFO_BASENAME-仅返回基本名称
    *   PATHINFO_EXTENSION-仅返回扩展

**返回值：**或
如果未传递 Options 参数，则返回包含以下元素的关联数组：目录名、基名、扩展名。
**错误和异常：**

1.  如果路径有多个扩展名，则 PATHINFO_EXTENSION 只返回最后一个扩展名。
2.  如果路径没有扩展名，则不返回扩展名元素。
3.  如果路径的基名以点开头，则以下字符将被解释为扩展名，并且文件名为空。

例如：

```php
Input : print_r(pathinfo("/documents/gfg.txt"));
Output : Array
         (
          [dirname] => /documents
          [basename] => gfg.txt
          [extension] => txt
         )

Input : print_r(pathinfo("/documents/gfg.txt", PATHINFO_DIRNAME));
Output : /documents

Input : print_r(pathinfo("/documents/gfg.txt", PATHINFO_EXTENSION));
Output : txt

Input : print_r(pathinfo("/documents/gfg.txt", PATHINFO_BASENAME));
Output : gfg.txt
```

下面的程序演示了 pathinfo()函数。
假设有一个名为“gfg.txt”
**程序 1**的文件

## PHP

```php
<?php
// returning information about
// the path using pathinfo() function
print_r(pathinfo("/documents/gfg.txt"));
?>
```

**输出：**

```php
 Array
         (
          [dirname] => /documents
          [basename] => gfg.txt
          [extension] => txt
         )
```

**程序 2**

## PHP

```php
<?php
  // returning information about
  // the directoryname path using pathinfo() function
  print_r(pathinfo("/documents/gfg.txt", PATHINFO_DIRNAME));
?>
```

**输出：**

```php
 /documents 
```

**程序 3**

## PHP

```php
<?php

  // returning information about
  // the extension of path using pathinfo() function
  print_r(pathinfo("/documents/gfg.txt", PATHINFO_EXTENSION));
?>
```

**输出：**

```php
 txt 
```

**程序 4**

## PHP

```php
<?php
  // returning information about
  // the basename of path using pathinfo() function
  print_r(pathinfo("/documents/gfg.txt", PATHINFO_BASENAME));
?>
```

**输出：**

```php
 gfg.txt 
```

**引用：**和
[http://php.net/manual/en/function.pathinfo.php](http://php.net/manual/en/function.pathinfo.php)
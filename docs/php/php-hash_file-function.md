# PHP|hash_file()函数

> Original: [https://www.geeksforgeeks.org/php-hash_file-function/](https://www.geeksforgeeks.org/php-hash_file-function/)

Hash_file()函数是 PHP 中的一个内置函数，用于使用给定文件的内容生成散列值。

**语法：**

```
*string* hash_file( $algo, $file, $raw_opt )
```

**参数：**此函数接受上述三个参数，如下所述。

*   **$algo：**它是指定所选散列算法的必需参数。
*   **$file：**此参数用于保存要散列的文件 url。
*   **$RAW_OPT：**如果参数设置为 TRUE，则输出将为原始二进制数据，如果参数设置为 FALSE，则输出将为小写十六进制。

**返回值：**此函数以小写十六进制返回包含计算出的消息摘要的字符串。

以下程序使用文件*gfg.txt*，该文件的内容如下：

> GeeksforGeek
> 极客的计算机科学门户

以下程序说明了 PHP 中的 hash_file()函数：
**程序 1：**

```
<?php

// PHP program to illustrate
//  hash_file function

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'GFG');

// Display Result
echo hash_file('md5', 'gfg.txt') . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```
083de2341fd19dce0de9e60f3e9a8e0d

```

**程序 2：**

```
<?php

// PHP program to illustrate
//  hash_file function

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'SUDO PLACEMENT');

// Display Result
echo hash_file('md5', 'gfg.txt') . "</br>";

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'GCET');

// Display Result
echo hash_file('sha1', 'gfg.txt');
?>
```

发帖主题：Re：Колибри0.7.0

```
083de2341fd19dce0de9e60f3e9a8e0d
a287a6ac47afec4140253a10b8a4c9c1e4f7a45e

```

**引用：**[http://php.net/manual/en/function.hash-file.php](http://php.net/manual/en/function.hash-file.php)
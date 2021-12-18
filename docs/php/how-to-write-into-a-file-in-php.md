# 如何用 PHP 写文件？

> 原文:[https://www . geesforgeks . org/如何在 php 中写入文件/](https://www.geeksforgeeks.org/how-to-write-into-a-file-in-php/)

在本文中，我们将讨论如何使用 PHP 内置的[**【fwrite()】**](https://www.geeksforgeeks.org/php-fwrite-function/)**函数写入文本文件。**

***fwrite()* 函数用于写入给定文件。它会在文件的末尾或达到作为参数传递的指定长度时停止，以先到者为准。**

****语法:****

```php
fwrite(file_name, string)
```

 ***   **File name:** Enter the name of the file.
*   **String:** What to write.

**返回值:**成功时返回写入字节数，失败时返回 false。

**例 1 :**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// Open a file named geeks_data in write mode
$data = fopen("geeks_data.txt", "w");

// writing content to a file using fwrite() function
echo fwrite($data, "This data is added as extra");

// closing the file
fclose($data);
?>
```

**输出:**

```php
27
```

**例 2:**

## PHP

```php
<?php
// Open a file named geeks_data in write mode
$data = fopen("geeks_data.txt", "w");

// writing content to a file using fwrite() function
echo fwrite($data, "This data is added as extra 
                    along with previous data");

// closing the file
fclose($data);
?>
```

**输出:**

```php
52
```**
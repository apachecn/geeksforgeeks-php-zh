# 如何在 PHP 中将一个图像转换为 base64 编码？

> 原文:[https://www . geesforgeks . org/如何将图像转换为 base64 编码 php/](https://www.geeksforgeeks.org/how-to-convert-an-image-to-base64-encoding-in-php/)

base64_encode()函数是 PHP 中的一个内置函数，用于将任何数据转换为 base64 编码。为了将图像转换为 base64 编码，首先需要获取文件的内容。这可以借助 PHP 的 *file_get_contents()* 功能来完成。然后将此原始数据传递给 base64_encode()函数进行编码。

**所需功能:**

*   **[base64_encode()函数](https://www.geeksforgeeks.org/php-base64_encode-function/)**base64 _ encode()函数是 PHP 中的一个内置函数，用来用 MIME base64 编码数据。MIME(多用途互联网邮件扩展)base64 用于对 base64 中的字符串进行编码。base64 编码数据占用的空间比原始数据多 33%。
*   **[file_get_contents()函数](https://www.geeksforgeeks.org/php-file_get_contents-function/)**PHP 中的 file_get_contents()函数是一个内置函数，用于将文件读入字符串。该函数使用服务器支持的内存映射技术，因此提高了性能，使其成为读取文件内容的首选方式。

**输入图像:**
![](img/579b4c0ccb2ef881d5627abefe188387.png)

**程序:**

```php
<?php 

// Get the image and convert into string
$img = file_get_contents(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-22.png');

// Encode the image string data into base64
$data = base64_encode($img);

// Display the output
echo $data;
?>
```

**输出:**

```php
iVBORw0KGgoAAAANSUhEUgAAApsAAAC4CAYAAACsNSfVAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJ
cEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJdhfdsglgklAEFkb2JlIEltYWdlUmVhZHlxyWqwrwtwefd
...
TeUsalQKBQKhUKhsBvK2FQoFAqFQqFQ2A1lbCoUCoVCoVAo7IYyNhUKhUKhUCgUdkMZmwqFQKBQKO0H0fxpZ1bfc

```

**参考:**

*   [http://php.net/manual/en/function.base64-encode.php](http://php.net/manual/en/function.base64-encode.php)
*   [http://php.net/manual/en/function.file-get-contents.php](http://php.net/manual/en/function.file-get-contents.php)

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
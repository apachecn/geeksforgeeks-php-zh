# PHP|exif_read_data()函数

> Original: [https://www.geeksforgeeks.org/php-exif_read_data-function/](https://www.geeksforgeeks.org/php-exif_read_data-function/)

**EXIF_READ_DATA()函数**是 PHP 中的一个内置函数，用于从图像文件中读取 EXIF 头。

**语法：**

```php
*array* exif_read_data( *mixed* $stream, *string* $sections,
                          *bool* $arrays, *bool* $thumbnail )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$stream:** it specifies the image file.
*   **$sections (optional):** it specifies a comma-separated list of sections.
*   **$array (optional):** it specifies whether each section is displayed as an array.
*   **$Thumble value (optional):** specifies whether to read thumbnails.

**返回值：**此函数成功时返回关联数组，失败时返回 False。

下面的示例说明了 PHP 中的**exif_read_data()函数**：

**示例 1：**

```php
<?php

// Open a the file from local folder
$fp = fopen('./geeksforgeeks.jpg', 'rb');

// Read the exif headers
$headers = exif_read_data($fp);

// Print the headers
echo 'EXIF Headers:' . '<br>';

print("<pre>".print_r($headers, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php   

// Create an Imagick Object 
$image = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg'); 

// Add comment to the image  
$image->commentImage("GeeksforGeeks"); 

// Save the file to local image
$image->writeImage('geeksforgeeks.jpg');

// Open a the same file
$fp = fopen('./geeksforgeeks.jpg', 'rb');

// Read the exif headers
$headers = exif_read_data($fp, 'COMMENT', true, true);

// Print the headers
echo 'EXIF Headers:' . '<br>';

print("<pre>".print_r($headers['COMMENT'], true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.exif-read-data.php](https://www.php.net/manual/en/function.exif-read-data.php)
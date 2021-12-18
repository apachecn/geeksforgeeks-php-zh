# 如何使用 PHP 将文件从一个目录复制到另一个目录？

> 原文:[https://www . geesforgeks . org/如何使用 php 将文件从一个目录复制到另一个目录/](https://www.geeksforgeeks.org/how-to-copy-a-file-from-one-directory-to-another-using-php/)

PHP 中的 [copy()函数](https://www.geeksforgeeks.org/php-copy-function/)用于将文件从源目录复制到目标目录或目的目录。它将源文件复制到目标文件，如果目标文件已经存在，它将被覆盖。copy()函数在成功时返回 true，在失败时返回 false。

**语法:**

```php
*bool* copy( *string* $source, *string* $destination, *resource* $context )
```

**参数:**该函数使用三个参数来源、目的地和上下文，如下所示:

*   **$ Source:** It specifies the path of the source file.
*   **$ destination:** It specifies the path of the target file or folder.
*   **$ context:** Specify the context resource created by the stream_context_create () function. It is an optional parameter.

**返回:**它返回一个布尔值，要么为真(成功时)，要么为假(失败时)。

**举例:**

```php
Input : $source = 'Source_file_location'
        $destination = 'Destination_file_location'
        copy( $source, $destination )

Output: true

```

```php
<?php 

// Copy the file from /user/desktop/geek.txt 
// to user/Downloads/geeksforgeeks.txt'
// directory

// Store the path of source file
$source = '/user/Desktop/geek.txt'; 

// Store the path of destination file
$destination = 'user/Downloads/geeksforgeeks.txt'; 

// Copy the file from /user/desktop/geek.txt 
// to user/Downloads/geeksforgeeks.txt'
// directory
if( !copy($source, $destination) ) { 
    echo "File can't be copied! \n"; 
} 
else { 
    echo "File has been copied! \n"; 
} 

?> 
```

**输出:**

```php
File has been copied!
```

**参考:**T2】https://www.php.net/manual/en/function.copy.php
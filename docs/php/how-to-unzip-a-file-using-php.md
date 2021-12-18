# 如何用 PHP 解压文件？

> 原文:[https://www . geesforgeks . org/如何使用-php 解压缩文件/](https://www.geeksforgeeks.org/how-to-unzip-a-file-using-php/)

要用 PHP 解压一个文件，我们可以使用 ZipArchive 类。ZipArchive 是一个简单的实用程序类，用于压缩和解压缩文件。我们不需要任何额外的插件来处理 zip 文件。ZipArchive 类为我们提供了创建 zip 文件或提取现有 zip 文件的工具。ZipArchive 类有一个名为 extractTo 的方法，用于将整个归档或给定文件的内容提取到指定的目标。ZipArchive 类还有很多其他方法和属性来帮助您在提取所有内容之前获得更多关于归档的信息。

**语法:**

```php
*bool* ZipArchive::extractTo( *string* $destination, *mixed* $entries )
```

**参数:**

*   **Destination:** You can use the $destination parameter to specify the extraction location of the file.
*   **Entry:** You can use the $entries parameter to specify a single file name to be extracted, or you can use it to pass an array of files.

**示例 1:** 本示例从特定文件夹中解压缩所有文件。

```php
<?php

$zip = new ZipArchive;

// Zip File Name
if ($zip->open('GeeksforGeeks.zip') === TRUE) {

    // Unzip Path
    $zip->extractTo('/Destination/Directory/');
    $zip->close();
    echo 'Unzipped Process Successful!';
} else {
    echo 'Unzipped Process failed';
}
?>
```

**描述:**创建一个 ZipArchive 类的对象，并使用$zip- > open()方法打开一个给定的 zip 文件。

如果返回真，则使用 extractTo()方法将文件提取到指定的路径，方法是在其中传递路径地址作为参数。

**示例 2:** 本示例从文件夹中解压缩特定文件。

```php
<?php

$zip = new ZipArchive;

// Zip File Name
$res = $zip->open('GeeksForGeeks.zip');

if ($res === TRUE) {

    // Unzip Path 
    $zip->extractTo('/Destination/Directory/',
        array('H_W.gif', 'helloworld.php'));

    $zip->close();
    echo 'Unzipped Process Successful!';
} else {
    echo 'Unzipped Process failed';
}
```

**描述:**使用文件元素，可以选择想要提取的 zip 文件。如果所选文件有效，则传递到 open()方法，并使用 extractTo()方法将其提取到指定路径。
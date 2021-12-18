# 如果一个文件夹在 PHP 中不存在，如何创建？

> 原文:[https://www . geesforgeks . org/如何在 php 中创建一个不存在的文件夹/](https://www.geeksforgeeks.org/how-to-create-a-folder-if-it-doesnt-exist-in-php/)

我们可以很容易地在 PHP 中创建一个文件夹，但是在此之前，您必须检查该文件夹或目录是否已经存在。因此，在本文中，您将学习在 PHP 中检查和创建文件夹或目录。

**方法:**

1.  [**【file _ exists()】**](https://www.geeksforgeeks.org/php-file_exists-function/)**:**是一个内置功能，用于检查文件或目录是否存在。
2.  [**is_dir()**](https://www.geeksforgeeks.org/php-is_dir-function/) **:也用于检查文件或目录是否存在。**
3.  [**【mkdir():**](https://www.geeksforgeeks.org/php-mkdir-function/)**此功能创建一个目录。**

****方法一:使用 file_exists()函数:**使用 **file_exists()** 函数检查文件或目录是否存在。**

****语法:****

```
file_exists( $path )
```

****参数:**PHP 中的 file_exists()函数只接受一个参数$path。它指定要检查的文件或目录的路径。**

****返回值:**成功返回真，失败返回假。**

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?PHP

// Checking whether file exists or not
$file_path = '/user01/work/gfg.txt';

if (file_exists($file_path)) {
    echo "The Given file already exists in GEEKSFORGEEKS directory";
}
else {
    echo "The file path does't exists in GeeksforGeeks directory";
}

?>
```

****Output**

```
The file path does't exists in GeeksforGeeks directory
```** 

****方法二:使用 **is_dir()** 函数:**is _ dir()函数用于检查指定文件是否为目录。**

****语法:****

```
is_dir( $file )
```

****参数:**PHP 中的 is_dir()函数只接受一个参数。它指定要检查的文件或目录的路径。**

****返回值:**如果文件是目录，则返回真，否则返回假。**

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

$gfg_directory = "https://www.geeksforgeeks.org";

// Checking whether a file is directory or not
if (is_dir($gfg_directory))
    echo ("Given $gfg_directory exists in GeeksforGeeks Portal");
else
    echo ("Given $gfg_directory doesn't exists in GeeksforGeeks Portal");

?>
```

****Output**

```
Given https://www.geeksforgeeks.org doesn't exists in GeeksforGeeks Portal
```** 

****方法 3:使用 **mkdir()** 函数:**mkdir()用指定的路径名创建一个新目录。**

****语法:****

```
mkdir(path, mode, recursive, context)
```

****参数:****

*   ****路径:**是指定路径的强制参数。**
*   ****模式:**是指定权限的可选参数。模式参数由四个数字组成，默认情况下，模式为 0777。

    *   第一个数字总是零。
    *   第二个数字指定所有者的权限。
    *   第三个数字指定所有者用户组的权限。
    *   第四个数字指定其他人的权限。** 
*   ****递归:**是可选参数，可用于设置递归模式。**
*   ****context:** It is an optional parameter that specifies the behavior of the stream.

    **返回值:**成功返回**真**失败返回**假**。

    **示例:**

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?PHP

    // Making a directory with the provision
    // of all permissions to the owner and 
    // the owner's user group
    mkdir("/documents/gfg/articles/", 0770, true)

    ?>
    ```

    **输出:**

    ```
    1
    ```

    **示例:**本示例检查文件是否存在，如果文件不存在，则使用 mkdir()函数创建一个新文件。

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?php

    $file_path = '/user01/work/gfg.txt';

    // Checking whether file exists or not
    if (!file_exists($file_path)) {

        // Create a new file or direcotry
        mkdir($file_path, 0777, true);
    }
    else {
        echo "The Given file path already exists";
    }
    ?>
    ```

    **输出:**

    ```
    1
    ```**
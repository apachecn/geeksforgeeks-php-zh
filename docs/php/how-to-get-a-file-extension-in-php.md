# 如何在 PHP 中获取文件扩展名？

> 原文:[https://www . geesforgeks . org/如何获取文件扩展名 php/](https://www.geeksforgeeks.org/how-to-get-a-file-extension-in-php/)

在本文中，我们将学习如何在 PHP 中获取当前的文件扩展名。

```php
Input  : c:/xampp/htdocs/project/home
Output : ""

Input  : c:/xampp/htdocs/project/index.php
Output : ".php"

Input  : c:/xampp/htdocs/project/style.min.css
Output : ".css"
```

**使用$_SERVER['SCRIPT_NAME']:**

$_SERVER 是存储信息的数组，如头、路径和脚本位置。这些条目由 web 服务器创建。没有其他方法可以让每个网络服务器都提供这些信息。

**语法:**

```php
 $_SERVER[‘SCRIPT_NAME’]
```

*   “SCRIPT_NAME”给出了从根目录到包含目录名的路径。

**方法 1:** 以下方法使用 [**strpos()**](https://www.geeksforgeeks.org/php-strpos-stripos-functions/) 和 [**substr()**](https://www.geeksforgeeks.org/php-substr-function/) 方法打印最后一次出现的值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
function fileExtension($s) {
  // strrpos() function returns the position
  // of the last occurrence of a string inside
  // another string.
  $n = strrpos($s,".");

  // The substr() function returns a part of a string.
  if($n===false) 
    return "";
  else
    return substr($s,$n+1);
}

// To Get the Current Filename.
$currentPage= $_SERVER['SCRIPT_NAME'];

//Function Call
echo fileExtension($currentPage);
?>
```

**Output**

```php
php
```

**方法 2:** 以下方法使用预定义函数 [pathinfo()](https://www.geeksforgeeks.org/php-pathinfo-function/) 。在输出中，“名称:”显示文件的名称，“扩展名:”显示文件的扩展名。

**PHP 代码:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php   

// To Get the Current Filename.
$path= $_SERVER['SCRIPT_NAME'];

// path info function is used to get info
// of The File Directory

// PATHINFO_FILENAME parameter in
// pathinfo() gives File Name
$name = pathinfo($path, PATHINFO_FILENAME);

// PATHINFO_EXTENSION parameter in pathinfo()
// gives File Extension
$ext  = pathinfo($path, PATHINFO_EXTENSION);

echo " Name: ", $name;
echo "\n Extension: ", $ext;

?>
```

**Output**

```php
 Name: 001510d47316b41e63f337e33f4aaea4
 Extension: php
```

**方法 3:** 下面的代码使用预定义函数 [parse_url()](https://www.geeksforgeeks.org/php-parse_url-function/) 和 [pathinfo()](https://www.geeksforgeeks.org/php-pathinfo-function/) 来获取 url。

**PHP 代码:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  // This is sample url
  $url =
"http://www.xyz.com/dir/file.index.php?Something+is+wrong=hello";

  // Here parse_url is used to return the
  // components of a URL
  $url = parse_url($url);

  // path info function is used to get info
  // of The File Directory

  // PATHINFO_FILENAME parameter in pathinfo()
  // gives File Name
  $name = pathinfo($url['path'], PATHINFO_FILENAME);

  // PATHINFO_EXTENSION parameter in pathinfo()
  // gives File Extension
  $ext  = pathinfo($url['path'], PATHINFO_EXTENSION);

  echo " Name: ", $name;
  echo "\n Extension: ", $ext;
?>
```

**Output**

```php
 Name: file.index
 Extension: php
```
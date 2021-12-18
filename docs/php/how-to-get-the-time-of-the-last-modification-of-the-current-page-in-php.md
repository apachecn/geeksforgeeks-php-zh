# PHP 中如何获取当前页面最后一次修改的时间？

> 原文:[https://www . geesforgeks . org/如何获取 php 中当前页面的最后修改时间/](https://www.geeksforgeeks.org/how-to-get-the-time-of-the-last-modification-of-the-current-page-in-php/)

有时候，为了不同的用途，我们需要在 PHP 中获取当前页面的最后修改时间。既然我们用的是 PHP，那么使用 **getlastmod()** PHP 函数就可以很容易的得到当前页面的最后修改时间。

**使用 getlastmod()函数:**getlastmod()函数用于获取当前页面的最后修改时间。这个功能简单而强大。

**语法:**

> $ Last _ modification = " Last modified on:"。日期(“F d Y H:i:s .，getlastmod())；

**示例:**以下是获取并显示当前页面上次修改时间的完整代码。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// To Get the last modification time.
$last_modification="Last modified: " . date ("F d Y H:i:s.", getlastmod());

// To Show the last modification time.
echo $last_modification;

?>
```

**Output**

```php
Last modified: February 25 2021 12:40:34.
```

**注:**我们可以直接使用如下。

```php
echo "Last modified: " . date ("F d Y H:i:s.", getlastmod());
```

**使用 [filemtime()函数:](https://www.geeksforgeeks.org/php-filemtime-function/)**PHP 中的 filemtime()函数是一个内置函数，用于返回指定文件内容被修改时的最后时间。

**示例:**

## PHP

```php
<?php 

// checking last time the contents 
// of a file were changed 
echo filemtime("index.html.txt"); 

// checking last time the contents of 
// a file were changed and formatting 
// the output of the date  
echo "Last modified: ".date("F d Y H:i:s.",  
                      filemtime("index.html")); 
?> 
```

**输出:**

```php
Last modified: February 13 2021 13:01:35.
```
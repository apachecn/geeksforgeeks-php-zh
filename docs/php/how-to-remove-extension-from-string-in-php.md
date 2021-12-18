# PHP 中如何去除字符串中的扩展名？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中删除扩展名/](https://www.geeksforgeeks.org/how-to-remove-extension-from-string-in-php/)

从字符串中删除扩展名有三种方法。它们如下

*   使用内置函数 pathinfo
*   使用内置函数 basename
*   使用字符串函数 substr 和 strrpos

**使用 [pathinfo()函数:](https://www.geeksforgeeks.org/php-pathinfo-function/)**path info()函数返回一个包含目录名、基名、扩展名和文件名的数组。

**语法:**

> 路径信息 （ $path， $options = PATHINFO_DIRNAME|PATHINFO_BASENAME|PATHINFO_EXTENSION|PATHINFO_FILENAME ）

或者，如果只有一个 PATHINFO_ constants 作为参数传递，它只返回完整文件名的那部分。

**示例:**

```php
<?php

// Initializing a variable with filename
$file = 'filename.html';

// Extracting only filename using constants
$x = pathinfo($file, PATHINFO_FILENAME);

// Printing the result
echo $x;

?>
```

**Output:**

```php
filename

```

**注意:**如果文件名包含完整路径，则只返回不带扩展名的文件名。

**使用 [basename()函数:](https://www.geeksforgeeks.org/php-basename-function/)**base name()函数用于以字符串形式返回路径的尾随名称组件。basename()对输入字符串进行天真的操作，不知道实际的文件系统或路径组件，如“..”
**语法:**

```php
basename ( $path, $suffix )
```

当文件的扩展名已知时，它可以作为参数传递给 basename 函数，告诉它从文件名中删除该扩展名。

**示例:**

```php
<?php

// Initializing a variable
// with filename
$file = 'filename.txt';

// Suffix is passed as second
// parameter
$x = basename($file, '.txt');

// Printing the result
echo $x;

?>
```

**Output:**

```php
filename

```

**使用 [substr()](https://www.geeksforgeeks.org/php-substr-function/) 和[str pos()](https://www.geeksforgeeks.org/php-strrpos-strripos-functions/)函数:**从文件名中删除扩展名的另一种方法是使用字符串函数 substr 和 str pos。substr()函数返回字符串的一部分，而 strrpos()函数查找字符串中最后一个子字符串的位置。

**语法:**

```php
substr ( $string, $start, $length )
```

**示例:**

```php
<?php

// Initializing a variable
// with filename
$file = 'filename.txt';

// Using substr 
$x = substr($file, 0, strrpos($file, '.'));

// Display the filename
echo $x;

?>
```

**Output:**

```php
filename

```

**注意:**如果文件名包含完整路径，则返回完整路径和不带扩展名的文件名。